FROM eclipse-temurin:21-jre-alpine
WORKDIR /app

# Create a non-root user for security best practice
RUN addgroup -S appgroup && adduser -S appuser -G appgroup
USER appuser

# Copy pre-built application JAR
COPY build/libs/*.jar app.jar

# Expose backend service port
EXPOSE 8080

# Run Spring Boot application
ENTRYPOINT ["java", "-jar", "app.jar"]
