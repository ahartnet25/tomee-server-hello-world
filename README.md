# TomEE Sample Project

This is a simple Maven project that runs a JAX-RS endpoint on Apache TomEE using the TomEE Embedded Maven Plugin.

## Prerequisites
- Java 8+
- Maven 3.6+

## Project Structure
- `src/main/java/com/example/HelloResource.java`: A JAX-RS resource with a `/hello` endpoint.
- `src/main/webapp/WEB-INF/web.xml`: Minimal web.xml for WAR configuration.
- `pom.xml`: Maven configuration with TomEE plugin.

## Running the Application
1. Clone or set up the project directory.
2. Ensure Maven is installed (`mvn --version`).
3. Run the following command to build and start the embedded TomEE server:
   ```bash
   mvn clean package org.apache.tomee.maven:tomee-embedded-maven-plugin:7.0.5:run -Dtomee-embedded-plugin.http=8081

## Accessing the Endpoint
   ```bash
   curl http://localhost:8081/myapp/hello
