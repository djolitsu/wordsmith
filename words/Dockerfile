FROM maven:3.6.3-openjdk-8 as build
COPY ./pom.xml ./pom.xml
COPY ./src ./src
RUN mvn verify

FROM openjdk:8u265-jre-slim
COPY --from=build target .
EXPOSE 8080
CMD ["java","-Xmx8m","-Xms8m","-jar","./words.jar"]
