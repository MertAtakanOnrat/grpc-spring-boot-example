# grpc-spring-boot-example
This project is a basic example showcasing the usage of gRPC with Spring Boot.

# Overview
The **'grpc-spring-boot-example'** project demonstrates how to set up a gRPC server using Spring Boot and implement a simple gRPC service for handling greetings.

The project consists of two modules:

+ **greeting-service**: This module represents the gRPC server application that exposes the **'GreetingService'** for handling greeting requests.

+ **greeting-common**: This module contains the shared code and protobuf message definitions used by the gRPC server and client.

# Usage
To run the project, follow these steps:

1. Build the project using Maven: mvn clean install

2. Start the gRPC server by running the GrpcSpringBootExampleApplication class in the greeting-service module.

3. Use a gRPC client tool, such as grpcurl, to interact with the gRPC server and make requests to the GreetingService.

+ Example command: grpcurl --plaintext -d '{"message": "How are you?"}' localhost:9090 com.atakan.grpc.GreetingService/greeting

+ This command sends a gRPC request to the server, passing a JSON payload with a message field.

4. The server responds with a greeting message, and the client displays the response.

# Dependencies
The project uses the following dependencies:

+ **Spring Boot**: The core framework for building the Spring Boot application.
+ **gRPC**: Provides the necessary libraries for implementing and consuming gRPC services.
+ **Protobuf**: Used for defining the service and message types using Protocol Buffers.
