# Banking System Configuration Repository

This repository contains external configuration files for the **Banking System Microservices** project.

## 📋 Overview

This repository serves as the external configuration source for the microservices architecture described in the main project: [https://github.com/en-atul/banking-system](https://github.com/en-atul/banking-system)

## 🏗️ Architecture

The banking system follows a microservices architecture with the following services:

- **API Gateway** - Central entry point with JWT authentication
- **Auth Service** - User authentication and authorization
- **Account Service** - Account management
- **Customer Service** - Customer information management
- **Transaction Service** - Financial transaction processing
- **Ledger Service** - Ledger entries (Admin only)
- **Notification Service** - Asynchronous notifications via Kafka

## 📁 Configuration Files

This repository contains configuration properties for different environments:

### Development Environment
- `account-service-dev.properties`
- `auth-service-dev.properties`
- `customer-service-dev.properties`
- `ledge-service-dev.properties`
- `notification-service-dev.properties`
- `transaction-service-dev.properties`

### Production Environment
- `auth-service-prod.properties`

### Default Configuration
- `account-service.properties`
- `auth-service.properties`
- `customer-service.properties`
- `ledger-service.properties`
- `notification-service.properties`
- `transaction-service.properties`

## 🔧 Usage

The Spring Cloud Config Server in the main banking system project fetches these configuration files to provide centralized configuration management across all microservices.

### Configuration Server
- **URL**: `http://localhost:8888`
- **Repository**: This repository serves as the configuration source
- **Profile Support**: Supports different profiles (dev, prod) for environment-specific configurations

## 🚀 Quick Start

1. **Clone the main banking system repository**:
   ```bash
   git clone https://github.com/en-atul/banking-system.git
   ```

2. **Start the infrastructure services**:
   ```bash
   cd banking-system
   docker-compose -f docker-compose.yml -f docker-compose.dev.yml up
   ```

3. **Start the Config Server** (it will fetch configurations from this repository):
   ```bash
   cd config-server
   mvn spring-boot:run
   ```
 For more read  **[banking-system-README](https://github.com/en-atul/banking-system/blob/master/README.md)**

4. **Start other microservices** - they will automatically fetch their configurations from the Config Server

## 📖 Documentation

For detailed information about the banking system architecture, API endpoints, and usage instructions, please refer to the main project repository:

**[https://github.com/en-atul/banking-system](https://github.com/en-atul/banking-system)**

## 🔗 Related Repositories

- **Main Banking System**: [https://github.com/en-atul/banking-system](https://github.com/en-atul/banking-system) - Complete microservices implementation
- **This Repository**: Configuration files for the banking system microservices

## 📝 License

This configuration repository is part of the Banking System Microservices project. Please refer to the main repository for licensing information. 