---
applyTo: '**/*.java'
---
# GitHub Copilot Instructions
# Project: Personal AI Assistant Agent

## 1. Project Overview

We are building a Personal AI Assistant Agent
using Java, Spring Boot, Spring AI and Google Gemini.

This is a real AI Agent project, not just a chatbot.

The application should eventually support:
- Intelligent conversations
- AI tool calling
- Agent decision-making
- Multi-step task execution
- Conversation memory
- Long-term memory
- External API integrations
- Personal task management
- Context-aware responses
- PostgreSQL persistence

## 2. Technology Stack

Backend:
- Java 21
- Spring Boot
- Maven
- Spring Web
- Spring AI

AI:
- Google Gemini API
- Spring AI ChatClient
- Tool Calling
- Prompt Engineering
- Agent Orchestration

Database:
- PostgreSQL
- Spring Data JPA
- Hibernate

Frontend:
- React.js
- Vite
- Tailwind CSS
- Axios

Testing:
- JUnit 5
- Mockito
- Spring Boot Test
- Postman

DevOps:
- Git
- GitHub
- Docker
- Docker Compose

Use compatible stable dependency versions.
Never assume dependency versions without verification.

## 3. Architecture Guidelines

Follow layered architecture and separation of concerns.

Use the following package structure:

com.personalassistant.agent
|
|-- config
|-- controller
|-- service
|-- dto
|-- entity
|-- repository
|-- agent
|-- tools
|-- memory
|-- exception
|-- enums
|-- util

Responsibilities:

Controller:
- Handle HTTP requests.
- Validate request input.
- Return appropriate responses.
- Keep business logic out of controllers.

Service:
- Implement business logic.
- Coordinate application operations.

Agent:
- Handle agent orchestration.
- Manage LLM interactions.
- Coordinate reasoning and execution.

Tools:
- Implement Java methods exposed to the LLM.
- Keep each tool focused on a specific responsibility.

Memory:
- Manage conversation context.
- Manage short-term and long-term memory.

Repository:
- Handle database access.

DTO:
- Separate API request and response models.

Config:
- Manage application configuration and beans.

Exception:
- Centralize exception handling.

## 4. Java Coding Standards

- Follow SOLID principles.
- Follow clean code practices.
- Use meaningful names.
- Use constructor injection.
- Avoid field injection.
- Prefer immutable objects where appropriate.
- Use Java records for simple DTOs when suitable.
- Avoid unnecessary abstraction.
- Avoid duplicate code.
- Use proper exception handling.
- Write maintainable and testable code.
- Keep methods focused and small.

## 5. AI Agent Development Rules

The agent should follow this workflow:

User Request
    |
    v
Understand Intent
    |
    v
Select Appropriate Tool
    |
    v
Execute Tool
    |
    v
Observe Result
    |
    v
Decide Next Action
    |
    v
Return Final Response

Important rules:

- Use Google Gemini as the primary LLM.
- Use Spring AI for LLM integration.
- Implement tool calling through Java methods.
- Separate agent orchestration from business logic.
- Maintain controlled execution loops.
- Limit the maximum number of tool calls.
- Handle failed tool executions.
- Never trust LLM output blindly.
- Require confirmation for sensitive operations.
- Never claim an action succeeded without verification.

## 6. Database Guidelines

Use PostgreSQL for persistent storage.

Use:
- Spring Data JPA
- Hibernate
- Proper entity relationships
- Repository interfaces
- Database migrations when appropriate

Do not put database logic inside controllers.

Keep database credentials outside source code.

## 7. API Development Standards

- Follow REST API conventions.
- Use appropriate HTTP methods.
- Use meaningful endpoint names.
- Use DTOs for request and response bodies.
- Validate incoming requests.
- Return correct HTTP status codes.
- Implement centralized exception handling.
- Avoid exposing internal implementation details.

## 8. Security Guidelines

- Never hardcode API keys.
- Use environment variables.
- Never commit secrets.
- Validate user inputs.
- Protect sensitive operations.
- Prevent arbitrary command execution.
- Handle authentication and authorization
  when user accounts are introduced.
- Keep individual user data isolated.

## 9. Testing Guidelines

- Write unit tests using JUnit 5.
- Use Mockito for mocking dependencies.
- Test service business logic.
- Test REST controllers.
- Test error scenarios.
- Test tool execution.
- Verify that generated code compiles.
- Run Maven tests after significant changes.

Do not claim tests passed unless they were executed.

## 10. Git and GitHub Guidelines

- Use meaningful commit messages.
- Keep commits focused on one feature.
- Never commit credentials or secrets.
- Maintain a clean .gitignore.
- Do not push changes without user approval.
- Update README when project functionality changes.

## 11. GitHub Copilot Working Instructions

Act as a senior Java engineer and AI architect.

When working on this project:

1. Understand the existing code before changing it.
2. Follow the established project architecture.
3. Never rewrite working code unnecessarily.
4. Do not create duplicate classes.
5. Do not introduce unnecessary dependencies.
6. Explain important architectural decisions.
7. Keep implementation modular.
8. Identify all files affected by changes.
9. Implement only the requested feature.
10. Run tests after implementation.
11. Fix compilation errors.
12. Do not skip required development phases.

Before implementing a major feature:
- Analyze the requirements.
- Explain the proposed approach.
- Identify affected files.
- Identify dependencies.
- Present an implementation plan.

Do not proceed with unrelated features.

## 12. Development Roadmap

Build the application in these phases:

Phase 1:
Project setup and Gemini integration.

Phase 2:
Chat API and conversation management.

Phase 3:
AI tool calling.

Phase 4:
Agent orchestration and execution loop.

Phase 5:
Conversation memory.

Phase 6:
PostgreSQL persistence.

Phase 7:
Personal assistant capabilities.

Phase 8:
React frontend.

Phase 9:
Testing, Docker and deployment.

Only implement the phase requested by the user.

## 13. Most Important Rule

Prioritize:
- Correctness
- Clean architecture
- Security
- Maintainability
- Performance
- Testability

Explain code in a way that helps the developer
understand the implementation.

Do not blindly generate code.

Always think about production-quality
software engineering.
