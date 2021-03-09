FROM maven:3.5-jdk-8-alpine
COPY . /app
WORKDIR /app
RUN mvn dependency:resolve
RUN mvn package

FROM openjdk:8-jre-alpine
COPY --from=0 /app /app
WORKDIR /app/target
CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]
