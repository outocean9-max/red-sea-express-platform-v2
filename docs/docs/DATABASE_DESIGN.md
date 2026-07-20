# Red Sea Express Database Design

## Overview

The Red Sea Express platform uses a scalable relational database to manage users, companies, logistics operations, marketplace activities, payments, and AI services.

Database Technology:

- PostgreSQL
- Prisma ORM

---

# Core Database Entities

## Users Table

Stores platform users.

Fields:

- id
- name
- email
- phone
- password
- role
- country
- status
- created_at

---

## Companies Table

Stores registered companies.

Fields:

- id
- company_name
- company_type
- country
- verification_status
- created_at

---

## Roles and Permissions

Controls access to platform features.

Roles:

- Importer
- Exporter
- Manufacturer
- Buyer
- Shipping Company
- Logistics Provider
- Customs Broker
- Insurance Provider
- Admin

---

# Trade Hub Tables

## Import Requests

Stores buyer/import requirements.

Fields:

- id
- user_id
- product
- quantity
- origin_country
- destination_country
- status

---

## Export Offers

Stores supplier/export offers.

Fields:

- id
- company_id
- product
- price
- availability
- status

---

# Logistics Tables

## Shipments

Stores shipment information.

Fields:

- id
- booking_id
- container_id
- origin_port
- destination_port
- tracking_status

---

## Containers

Stores container information.

Fields:

- id
- container_number
- type
- size
- availability_status

---

# Financial Tables

## Wallets

Stores user balances.

Fields:

- id
- user_id
- balance
- currency

---

## Transactions

Stores all financial operations.

Fields:

- id
- wallet_id
- amount
- type
- status
- created_at

---

# AI Assistant Data

## AI Conversations

Stores Aisha AI interactions.

Fields:

- id
- user_id
- message
- response
- created_at

---

# Security Requirements

- Encrypted sensitive data
- Role based access control
- Database backups
- Audit logs
- Data validation

---

# Future Expansion

Database supports:

- More countries
- More logistics services
- External API integrations
- Advanced AI analytics
