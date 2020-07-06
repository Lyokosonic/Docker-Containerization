FROM maven:3.5-jdk-8-alpine AS builder
RUN mkdir -p /usr/src/worker/
WORKDIR /usr/src/worker
COPY pom.xml /usr/src/worker
RUN mvn dependency:resolve
COPY . /usr/src/worker/
RUN mvn package

FROM openjdk:8-jre-alpine
ADD .env /
COPY --from=builder /usr/src/worker/target/worker-jar-with-dependencies.jar .
CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]