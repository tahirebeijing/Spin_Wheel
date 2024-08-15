
# Spin Wheel Project Documentation

## Introduction
This project implements a spin wheel feature allowing users to earn rewards and manage spins. Users can have a set number of free spins daily and buy additional spins using their wallet balance.

## Features
- Users can spin the wheel a limited number of times daily.
- Users can buy additional spins.
- Transactions are recorded for each spin and purchase.

## Installation

### Prerequisites
- PHP 8.0+
- Composer
- Laravel 9.x
- MySQL or any other database



# API Documentation

## Endpoints

### 1. Spin
- **URL**: `/api/retailer/spin`
- **Method**: `POST`
- **Description**: Allows a retailer to spin the wheel.
- **Headers**: `Authorization: Bearer {token}`
- **Request Body**: None
- **Response**: `{ "message": "Spin successful", "amount_won": 100 }`
- **Errors**:
  - `403 Forbidden`: No free spins left.

### 2. Buy Spin
- **URL**: `/api/retailer/buy-spin`
- **Method**: `POST`
- **Description**: Allows a retailer to buy additional spins.
- **Headers**: `Authorization: Bearer {token}`
- **Request Body**: None
- **Response**: `{ "message": "Spin successful", "amount_won": 100 }`
- **Errors**:
  - `403 Forbidden`: Insufficient balance.

### 3. Register User
- **URL**: `/api/register`
- **Method**: `POST`
- **Description**:  Register a new user with the given details.
- **Headers**: `Content-Type: application/json`
- **Request Body**: None
- **Response**: `{ "message": "User registered successfully"}`
- **Errors**:
  - `422 Unprocessable Entity

### 4. Login User
- **URL**: `/api/login`
- **Method**: `POST`
- **Description**:   Authenticate a user and return an access token.
- **Headers**: `Content-Type: application/json`
- **Request Body**: None
- **Response**: `{ "message": "User login successfully"}`
- **Errors**:
  - `401 Unauthorized: Invalid credentials.`


