# 🏦 EquityStream-Stock Brokerage Platform

Welcome to the **Stock Brokerage Platform**! This project is a comprehensive solution designed to manage various aspects of stock trading, from market data retrieval to order management, user management, and risk assessment. The platform is built using a **microservices architecture**, ensuring scalability and maintainability.


## 📋 Table of Contents
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Microservices Overview](#microservices-overview)
  - [Client Service](#client-service)
  - [Exchange Connector Service](#exchange-connector-service)
  - [Market Data Service](#market-data-service)
  - [Order History Service](#order-history-service)
  - [Order Management Service](#order-management-service)
  - [Risk Management Service](#risk-management-service)
  - [Stock Exchange Service](#stock-exchange-service)
  - [User Management Service](#user-management-service)
  - [Watchlist Service](#watchlist-service)

## ✨ Features

- **Market Data Retrieval**: Real-time market data integration with WebSocket and REST APIs.
- **Order Management**: Place, retrieve, and manage orders via integration with Upstox API.
- **Risk Management**: Assess and validate orders based on user funds.
- **User Management**: Handle user data, including watchlists and funds.
- **Watchlist Management**: Create and manage stock watchlists.
- **Historical Data Access**: Query historical stock prices, company information, and user portfolios.
- **Microservices Architecture**: Each service operates independently, ensuring scalability and ease of maintenance.
- **GraphQL API**: For querying stock-related data efficiently.
- **MongoDB Integration**: For user and watchlist data persistence.
- **gRPC Integration**: Used for risk management operations.

## 🛠️ Tech Stack

- **Frontend**: React, Zustand, Tailwind CSS
- **Backend**: Node.js, Express.js, GraphQL, gRPC
- **Database**: MongoDB, Prisma ORM (for PostgreSQL)
- **APIs**: Upstox API for market data and order management
- **WebSockets**: For real-time data streaming
- **Docker**: Containerization of microservices

## 🧩 Microservices Overview

### 🖥️ Client Service
- **Location**: `client/`
- **Description**: This service provides the frontend interface for users, built with React. It includes features like viewing stock charts, managing watchlists, and querying historical data using GraphQL.

### 🔗 Exchange Connector Service
- **Location**: `exchange_connector/`
- **Description**: This service handles the registration and triggering of webhooks, facilitating communication between the stock exchange and the platform.

### 📊 Market Data Service
- **Location**: `market_data_service/`
- **Description**: This service integrates with external market data APIs (e.g., Upstox) to fetch real-time and historical market data. It also processes CSV files for market data analysis.

### 🗃️ Order History Service
- **Location**: `order_history_service/`
- **Description**: Exposes a GraphQL API to retrieve historical stock prices, company information, and user portfolios. It serves mock data to simulate real trading environments.

### 📑 Order Management Service
- **Location**: `order_mgr_service/`
- **Description**: Manages user orders by interacting with the database and the Upstox API to place, retrieve, and cancel orders.

### 🛡️ Risk Management Service
- **Location**: `risk_management_service/`
- **Description**: A gRPC-based service that validates orders against user funds, ensuring that all trades are within financial limits.

### 📈 Stock Exchange Service
- **Location**: `stock_exchange/`
- **Description**: Facilitates communication with the stock exchange, handling the registration of webhooks and triggering events.

### 👥 User Management Service
- **Location**: `user_mgr_service/`
- **Description**: Manages user information, including the creation of users, retrieval of user data, and integration with Upstox for fund management.

### 🔍 Watchlist Service
- **Location**: `watchlist_service/`
- **Description**: Handles the creation and management of stock watchlists, allowing users to keep track of their favorite stocks.
