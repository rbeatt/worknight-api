# as-team1-api

Short backend service used to manage job roles and related data (capabilities, competencies, banding, etc.). Built during the Kainos Academy programme as part of a small team.

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
2. The application exposes REST endpoints; a Swagger UI is available at the deployed service (see below) or locally if Swagger is enabled.

Common commands:
- mvn clean package
- mvn test

## Deployment
The repository includes a GitHub Actions workflow that builds a Docker image and deploys the service to Amazon ECS.

## Live service
A deployed instance of the service (read-only) is available at:
https://ebbxsctpj8.eu-west-1.awsapprunner.com/swagger#/Commit%20Connoisseurs%20API/getAllJobRoles

## Testing
- Unit and integration tests are implemented with JUnit and Mockito.
- Run tests locally with `mvn test`.

## Linting
- Code formatting is enforced using Maven Spotless.
- Husky Git hooks run Spotless on commit to ensure formatting consistency.

## Personal contributions
I contributed the following areas in this project:
- Adding and viewing job roles: implemented endpoints and business logic to create and retrieve job roles, including request validation and persistence integration.
- Authentication: implemented login flow and token generation used by the API to protect sensitive endpoints.

These contributions include work across controller, service, validator and DAO layers and were delivered during the sprint-based development cycle.

## Notes for reviewers
- See `src/main/java` for the implementation and `test/` for unit and integration tests.
- SQL migration and test data are available in the `scripts/` folder.

## Repository cleanup for sharing
This repository has been prepared for public review. CI workflows, deployment configuration and any files that contained account-specific settings or secrets have been removed or redacted to protect credentials and third-party accounts. The codebase retains application logic, tests and supporting scripts useful for reviewers.

If you want a fully clean history (no prior commits or author metadata), you can remove the Git history and reinitialize the repository before pushing to a new account — see the steps in this README or ask me to perform that for you.

License: (add license if desired)
