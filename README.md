# PopcornTime API - Backend 🍿

The PopcornTime API is a backend service engineered to deliver cinematic entertainment data with high performance and scalability. Built upon the principles of Clean Architecture and SOLID, this API serves as the core processing engine for streaming applications and movie catalogs.

## Architecture & Engineering
Moving beyond trivial implementations, this project was architected for enterprise-grade environments, focusing on:

- Hexagonal Architecture (Ports & Adapters): Ensures that business logic remains independent of frameworks, databases, or external agents.
  
- Domain-Driven Design (DDD): Code structuring focused on the problem domain, significantly enhancing maintainability and testability.

- Enterprise Standards: Implementation of professional patterns such as Gateways, Mappers, and global Error Handlers to ensure consistency across the entire application.

## Tech Tools

- Node.js 25.0.9
- TypeScript 5.9.3
- Prisma 7.2.0
- MongoDB 8.2.3
- Docker 4.57.0
- Zod 4.3.5

## Project Structure

``` bash
src/
├── domain/                       
│   ├── models/                    <-- Entities
│   └── errors/                    <-- Custom Domain Exceptions
│
├── application/                  
│   ├── use-cases/                 <-- Business rule implementations
│   └── repositories/              <-- Port definitions
│
└── infrastructure/               
    ├── http/
    │   ├── controllers/           <-- Driving Adapters (REST)
    │   ├── routes/                <-- Route definitions
    │   ├── middlewares/           <-- Global Error Handling and Zod validation
    │   └── schemas/               <-- Declarative Zod validation rules
    ├── repositories/              <-- Driven Adapters
    └── generated/                 <-- Generated Prisma Client types
```

## How to Start

Ensure Docker Desktop is running and execute:

```bash
docker-compose up --build
```

The API will be available at `http://localhost:3001`