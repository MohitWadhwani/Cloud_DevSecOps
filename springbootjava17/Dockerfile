# Use an official OpenJDK Alpine base image for Java 17
FROM openjdk:17-alpine

# Create a non-root user and group
RUN addgroup -S spring && adduser -S spring -G spring

# Set the working directory inside the container
WORKDIR /app

# Copy the generated JAR file from the target directory to the container's working directory
COPY target/springbootjava17.jar app.jar

# Expose the port that your Spring Boot application is configured to listen on
EXPOSE 9090

# Change ownership of the working directory to the non-root user
RUN chown -R spring:spring /app

# Switch to the non-root user
USER spring

# Command to run the Spring Boot application when the container starts
CMD ["java", "-jar", "app.jar"]