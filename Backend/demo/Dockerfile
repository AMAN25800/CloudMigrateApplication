# Use official Java 17 JDK as base image
FROM eclipse-temurin:17-jdk

# Set the working directory inside the container
WORKDIR /app

# Copy only the built jar file into the container
COPY target/*.jar app.jar

# Render dynamically assigns a port, so expose 8080 and use PORT variable
EXPOSE 8081

# Run the app
ENTRYPOINT ["sh", "-c", "java -jar app.jar --server.port=$PORT"]
