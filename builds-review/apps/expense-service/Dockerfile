FROM ubi8/openjdk-17

USER 1001

COPY pom.xml .
RUN mvn dependency:go-offline

COPY src src
RUN mvn clean package

EXPOSE 8080

CMD ["java", "-jar", "target/expense-service-1.0.0-SNAPSHOT-runner.jar"]
