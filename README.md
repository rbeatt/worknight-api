# Worknight API

Worknight API is a lightweight backend service used to manage job roles and related data (capabilities, competencies, banding, etc.). Built during the Kainos Academy programme as part of a small team.

## Problem statement
There was no single source of truth for job roles and the related metadata (job descriptions, capabilities, competencies, banding). This made it time-consuming and error-prone for employees and recruitment admins to find or update role information.

## Vision
Provide a lightweight RESTful backend that lets Kainos employees and recruitment administrators retrieve, create and update job roles and their associated information through a single API.

## Project context
- Programme: Kainos Academy (7-week cohort)
- Delivery: this repository contains the backend work delivered across 3 weekly sprints over 3 weeks

## Key features
- CRUD operations for job roles (create, read, update, delete)
- Capability and banding lookups
- Authentication (login + token generation)
- Validation and error handling

## Running the application
1. Build and run with Maven or your preferred IDE; the main class is `trueApplication`.
2. The application exposes REST endpoints; a Swagger UI is available at the deployed service (if enabled locally).

Common commands:
- `mvn clean package`
- `mvn test`

## Deployment
This repository previously included CI and deployment configuration for AWS; those files have been removed for public sharing. The application can still be containerised and deployed using the included Dockerfile template (removed) and existing build scripts if reconfigured.

## Testing
- Unit and integration tests are implemented with JUnit and Mockito.
- Run tests locally with `mvn test`.

## Linting
- Code formatting is enforced using Maven Spotless.
- Husky Git hooks were used in development to enforce formatting; hooks were removed for public sharing.

## Personal contributions
I contributed the following areas in this project:
- Adding and viewing job roles: implemented endpoints and business logic to create and retrieve job roles, including request validation and persistence integration.
- Authentication: implemented login flow and token generation used by the API to protect sensitive endpoints.

These contributions include work across controller, service, validator and DAO layers and were delivered during the sprint-based development cycle.

## Repository cleanup for sharing
This repository has been prepared for public review. CI workflows, deployment configuration and any files that contained account-specific settings or secrets were removed to protect credentials and third-party accounts.

## Notes for reviewers
- See `src/main/java` for the implementation and `test/` for unit and integration tests.
- SQL migration and test data are available in the `scripts/` folder.
