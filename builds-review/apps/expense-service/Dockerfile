FROM registry.access.redhat.com/ubi8/openjdk-17@sha256:7016a0c5ce878211a8b82fbeb6619f82a97a35acdba6773be1c5f92f4e85aec8

USER 1001

COPY pom.xml .
RUN mvn dependency:go-offline

COPY src src
RUN mvn clean package

EXPOSE 8080

CMD ["java", "-jar", "target/expense-service-1.0.0-SNAPSHOT-runner.jar"]
