# Service Management Platform

## 1. Product

Service Management Platform is a software platform for small and medium-sized service-based businesses.

Its purpose is to reduce the operational complexity involved in managing the core elements of a service business, including customers, staff, services, resources, memberships, pricing, scheduling, and bookings.

Booking is a capability of the platform, not the definition of the product.

A dance studio will be used as the initial validation domain because it provides a realistic combination of customers, staff, rooms, schedules, memberships, pricing, and bookings.

However, the platform must be designed around reusable service-business concepts rather than dance-studio-specific assumptions.

The architecture and domain model should support expansion to other service-based businesses with minimal structural refactoring, while avoiding premature generalization.

---

## 2. Problem

Service-based businesses often coordinate their operations through a combination of manual processes, spreadsheets, messaging applications, calendars, and disconnected software tools.

As the business grows, managing customers, staff availability, services, resources, pricing, memberships, schedules, and bookings becomes increasingly complex.

The platform aims to centralize these operational capabilities and reduce the effort required to manage them without introducing unnecessary complexity.

---

## 3. Scope

The platform may support business capabilities including:

- Customer management
- Staff and specialist management
- Service management
- Resource and room management
- Membership management
- Pricing
- Scheduling
- Booking management

This list defines the general product domain, not the MVP.

Individual capabilities and features must be introduced through specifications based on actual product requirements.

---

## 4. Engineering Vision

The project will be developed as a real, production-oriented software system rather than as a collection of isolated learning exercises.

The engineering approach is backend-centered while covering the complete delivery lifecycle of the product.

The system is expected to progressively include:

- C# and .NET backend development
- HTTP and REST APIs
- Relational database persistence
- Authentication and authorization
- Automated unit, integration, API, and end-to-end testing where appropriate
- A frontend consuming the backend API
- Containerization
- CI/CD
- Deployment
- Observability
- AI-assisted software engineering

Architecture, patterns, libraries, and infrastructure technologies must be selected based on actual requirements and justified engineering decisions rather than predetermined for learning purposes.

---

## 5. Learning & Professional Objectives

This project has two simultaneous outcomes:

1. Build a useful, production-oriented software product.
2. Develop and demonstrate professional software engineering capability.

The project will be used to develop practical experience in:

- Backend engineering with C# and .NET
- Software architecture and system design
- Automated testing and SDET practices
- Git and GitHub engineering workflows
- Spec-Driven Development
- CI/CD and software delivery
- Code review
- Technical decision-making
- AI-assisted software engineering
- Context engineering for AI systems
- Coding-agent supervision and orchestration

AI agents may generate a significant portion of the implementation when appropriate.

However, AI is used to accelerate engineering work, not to replace engineering understanding.

Manual implementation may be intentionally used when it provides meaningful learning value. In selected cases, the same problem may be implemented manually and with an AI agent to compare approaches and deepen technical understanding.

---

## 6. Engineering Principles

### Reduce operational complexity

Every feature should reduce operational complexity instead of increasing it.

### Technical ownership

Never merge a solution that the engineer cannot technically defend.

The engineer must be able to explain the relevant design decisions, implementation logic, abstractions, transactions, tests, failure scenarios, trade-offs, and the impact of changing requirements.

### Simplicity

Prefer the simplest solution that satisfies the actual requirements.

Avoid unnecessary abstraction, premature generalization, and process bureaucracy.

### Requirements drive architecture

Architecture must emerge from actual product and quality requirements.

Patterns and technologies must solve identified problems rather than be introduced only because they are considered best practices.

### Generalize from real needs

Use the dance studio as the first concrete validation domain, but model reusable service-business concepts whenever the evidence supports them.

Avoid both domain-specific coupling and premature abstraction.

### AI does not lower engineering standards

AI-generated code must be reviewed, tested, understood, and evaluated using the same engineering standards as human-written code.
