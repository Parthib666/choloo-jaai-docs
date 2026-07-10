# Users Database Design

## Purpose

The users table stores all system users including:

- Customers
- Corporate clients
- Event managers
- Administrators


## Table Name


users



## Schema

| Column | Type | Description |
|---|---|---|
| id | UUID | Primary identifier |
| firstName | varchar | User first name |
| lastName | varchar | User last name |
| email | varchar | Unique email |
| phone | varchar | Optional phone number |
| passwordHash | varchar | Encrypted password |
| role | enum | User access role |
| status | enum | Account status |
| createdAt | timestamp | Creation time |
| updatedAt | timestamp | Last update time |


## Primary Key


id UUID PRIMARY KEY


Generated automatically using:


uuid_generate_v4()



## Constraints

### Email

Email has a unique constraint.

Purpose:

- Prevent duplicate accounts
- Support authentication lookup


## User Roles

Current roles:


CUSTOMER
CLIENT
EVENT_MANAGER
ADMIN



## User Status

Current statuses:


ACTIVE
INACTIVE
SUSPENDED



## ORM Mapping

The entity is implemented using TypeORM:


User Entity
|
|
TypeORM
|
|
users table
