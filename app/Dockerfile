# Dockerfile for Java Application

# Use an official Maven runtime as a parent image
FROM maven:3.8.1-openjdk-11

# Set the working directory in the container
WORKDIR /usr/src/app

# Add a volume pointing to /tmp because that is where spring boot creates working directories for Tomcat by default
VOLUME /tmp

# The application's jar file
ARG JAR_FILE=target/myapp-0.0.1-SNAPSHOT.jar

# Add the application's jar to the container
ADD ${JAR_FILE} app.jar

# Run the jar file 
ENTRYPOINT ["java","-jar","/app.jar"]
