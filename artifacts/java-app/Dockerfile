FROM openjdk:16 as build
WORKDIR /app
ADD . .
RUN ./mvnw package

FROM openjdk:16
COPY --from=build /app/target/demo-2-0.0.1-SNAPSHOT.jar /app.jar
CMD java -jar /app.jar
