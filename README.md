# Spring Cloud Config Repository

This is the configuration repository for Spring Cloud Config, used for centralized configuration management in a microservices architecture.

## Directory Structure

- `application.yml`: Global configuration file containing shared configurations for all services
- `api-gateway.yml`: API Gateway service configuration
- `service-consumer.yml`: Service consumer configuration
- `service-provider.yml`: Service provider configuration

## Configuration Details

### Global Configuration (application.yml)

Contains the following main configurations:

- Spring Cloud Config settings
- Load balancer configuration
- Management endpoints configuration
- Eureka client configuration

### Service Configurations

Each service has its own configuration file that can be customized as needed.

## Usage Guide

1. Ensure the Config Server is properly configured and running
2. Reference the configuration in your services using:
   ```yaml
   spring:
     cloud:
       config:
         uri: http://localhost:8888
         fail-fast: true
   ```

## Configuration Updates

When making configuration changes:

1. Commit changes to the configuration repository
2. Refresh the configuration (via Actuator refresh endpoint or service restart)

## Important Notes

- Ensure correct YAML formatting in configuration files
- Use encryption for sensitive information
- Use version control to manage configuration changes
