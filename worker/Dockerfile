FROM maven:3.5-jdk-8-alpine
COPY . /app
WORKDIR /app
RUN mvn dependency:resolve

FROM openjdk:8-jre-alpine
# todo fix jar name
CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]
