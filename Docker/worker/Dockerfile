FROM maven:3.9.6-eclipse-temurin-21-alpine AS builder
WORKDIR /app_worker

COPY pom.xml ./
RUN mvn dependency:resolve
COPY src ./src
RUN mvn package

FROM eclipse-temurin:21-jre-alpine
WORKDIR /app_worker

COPY --from=builder /app_worker/target/worker-jar-with-dependencies.jar ./
CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]