FROM openjdk:21-jdk

WORKDIR /app

COPY target/PersonaBACKEND-0.0.1-SNAPSHOT.jar app.jar

EXPOSE 8080


ENV SPRING_DATASOURCE_URL=jdbc:postgresql://localhost:5433/persona-db
ENV SPRING_DATASOURCE_USERNAME=postgres
ENV SPRING_DATASOURCE_PASSWORD=postgres

ENTRYPOINT ["java", "-jar", "app.jar"]
