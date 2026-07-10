# Backend Architecture

## Overview

The Choloo Jaai backend is built using a modular architecture based on NestJS.

The backend follows a layered architecture:

Client
 |
Controller Layer
 |
Service Layer
 |
Repository Layer
 |
Database


## Technology Stack

| Component | Technology |
|---|---|
| Framework | NestJS |
| Language | TypeScript |
| ORM | TypeORM |
| Database | PostgreSQL 16 |
| Cache | Redis 7 |
| Runtime | Node.js |
| Containerization | Docker |


## Backend Folder Structure


src
|
├── common
│ ├── decorators
│ ├── filters
│ ├── guards
│ ├── interceptors
│ └── utils
│
├── config
│
├── database
│
└── modules
|
└── users
|
├── dto
├── entities
├── users.controller.ts
├── users.service.ts
└── users.module.ts



## Module Architecture

Each business feature is implemented as an independent module.

Example:

Users Module


UsersController
|
|
UsersService
|
|
TypeORM Repository
|
|
PostgreSQL



## Current Implemented Modules

| Module | Status |
|---|---|
| Database Module | Completed |
| Users Module | Completed |
| Authentication Module | Pending |
| Events Module | Pending |
| Booking Module | Pending |
| Invoice Module | Pending |