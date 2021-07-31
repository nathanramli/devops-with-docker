FROM openjdk:8-alpine

WORKDIR /usr/src/app

# Expose app port
EXPOSE 8080

# Copy the project
COPY . .

# Build 
RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]