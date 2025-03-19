FROM maven:3.8.4-jdk-11-slim AS builder
ADD . .
RUN mvn dependency:resolve
RUN mvn package

FROM openjdk:11-jre-slim
WORKDIR /target
ADD --from=builder /target .
CMD java -jar worker-jar-with-dependencies.jar