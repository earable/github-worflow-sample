FROM maven:3.8.4-openjdk-11-slim as build
WORKDIR /usr/src/app
COPY pom.xml /usr/src/app
RUN mvn clean package
COPY . .
RUN mvn clean package install -DskipTests
EXPOSE 80
FROM adoptopenjdk/openjdk11:jre-11.0.6_10-alpine
COPY --from=build /usr/src/app/target/earable-xxxxxx-service-*.jar ./earable-xxxxxx-service.jar
CMD java $JAVA_OPTIONS -jar earable-xxxxxx-service.jar
