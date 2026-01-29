# Todo Project

This repository is the central hub for the Todo application.

## Repositories
- Frontend: https://github.com/Jayli58/todo-app-frontend
- Backend: https://github.com/Jayli58/todo-app-backend
- Infrastructure (CDK): https://github.com/Jayli58/todo-app-infra

## Architecture
Authentication:
User authentication and authorization are handled via Amazon Cognito,
with the frontend integrating Cognito-hosted authentication and the backend
secured using JWT validation.

Client flow:
React → API Gateway → Lambda → DynamoDB

Event-driven flow:
DynamoDB TTL → DynamoDB Streams → Reminder Lambda → Email service

The system combines synchronous API-based interactions with asynchronous,
event-driven processing for scheduled reminders.

Deployed using AWS CDK.

## CI/CD
- Frontend pipeline: S3 + CloudFront
- Backend pipeline: Lambda + API Gateway
