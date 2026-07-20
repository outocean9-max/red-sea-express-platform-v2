# Red Sea Express API Design

## Overview

The API is the communication layer between the frontend, backend, database, AI assistant, and external logistics systems.

The platform uses an API-first architecture.

## Authentication APIs

### Register User

POST /api/auth/register

Creates a new user account.

Data:
- Name
- Email
- Phone
- Password
- Country
- Role


### Login

POST /api/auth/login

Authenticates users and creates a secure session.

---

# Trade Hub APIs

## Import Request

POST /api/import-requests

Creates a new import requirement.

Information:
- Product
- Quantity
- Origin country
- Destination country


## Export Offer

POST /api/export-offers

Creates supplier offers.


## Matching Engine

GET /api/matching

Finds suitable matches between buyers and suppliers.

---

# Logistics APIs

## Freight Calculator

POST /api/freight/calculate

Calculates container shipping cost.

Inputs:
- Origin port
- Destination port
- Container size
- Cargo information


## Tracking

GET /api/shipment/tracking

Provides shipment status.

---

# Wallet APIs

GET /api/wallet

Shows wallet balance.


POST /api/payment

Creates payment transactions.

---

# AI Assistant API

POST /api/ai/chat

Connects users with Aisha AI Assistant.

Functions:
- User guidance
- Request creation
- Recommendations
- Logistics support


# Security

API protection:

- Authentication
- Permissions
- Data validation
- Rate limiting
- Audit logs
