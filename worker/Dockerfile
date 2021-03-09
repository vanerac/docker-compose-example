FROM maven:3.5-jdk-8-alpine
COPY . /app
WORKDIR /app
RUN mvn dependency:resolve
RUN mvn package
RUN ls -al
RUN ls -al target/

FROM openjdk:8-jre-alpine
COPY --from=0 /app /app
WORKDIR /app/target
RUN ls
CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]
