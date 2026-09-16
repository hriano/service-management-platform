# Service Management Platform

## Product Overview

The Service Management Platform is a business operations platform for small and medium-sized service-based businesses. It centralizes the management of customers, participants, staff, services, resources, schedules, sessions, and bookings so that businesses can manage their daily operations through a connected operational platform instead of relying on disconnected tools.

The platform is designed for businesses whose primary value is delivered through services performed by people, usually involving scheduled time, customers or participants, staff, and shared resources. Booking is a capability of the platform, not the definition of the product.

The initial reference domain is a dance studio, but the product is intentionally designed as a multi-industry service management platform rather than a dance-studio-specific system. It models reusable service-business concepts while using the reference domain to validate them.

The product aims to reduce operational complexity, improve visibility into daily operations, support better use of resources, and provide a foundation that can evolve with the business. Long term, it may evolve from an operational management platform into a more intelligent platform capable of supporting and executing workflows under business-defined rules.

**Mission:** Help service-based businesses operate with confidence by making their daily operations simple, connected, and accessible.

## Problem

Small and medium-sized service-based businesses often manage their daily operations using multiple disconnected tools such as calendars, spreadsheets, messaging applications, and specialized systems. Operational information becomes fragmented across these tools, making it difficult to maintain a consistent view of customers, participants, staff, services, schedules, bookings, and shared resources.

As the business grows, this fragmentation increases operational complexity and can lead to:

- duplicated or inconsistent information;
- scheduling and resource conflicts;
- repetitive administrative work;
- reduced visibility into daily operations;
- greater risk of operational errors; and
- difficulty obtaining the information needed to make timely decisions.

Many existing tools address isolated parts of the operation rather than the business operation as a connected whole. The product addresses this problem by providing an integrated operational platform where the information and processes required for daily service delivery can be managed together.

## Target Market

The primary target market is small and medium-sized service-based businesses that manage scheduled services involving customers or participants, staff, and shared resources.

These businesses commonly have:

- services delivered at scheduled times;
- staff members or specialists responsible for service delivery;
- customers and, when applicable, distinct service participants;
- shared or limited resources such as rooms, spaces, or equipment;
- recurring appointments, sessions, courses, or programs;
- a need to coordinate availability, capacity, and bookings;
- operational information distributed across multiple tools; and
- increasing administrative complexity as the business grows.

Representative industries include dance studios; fitness, yoga, and Pilates businesses; martial arts and sports academies; music schools; education and training providers; beauty and barber businesses; wellness and healthcare service providers; and photography and other appointment-based professional services.

These industries are examples of the target domain rather than product-specific verticals. The platform models the common operational concepts shared across service businesses instead of being designed around one industry.

The initial target does not include businesses whose primary operation is manufacturing, retail-only or e-commerce, logistics, inventory-centered operations, financial services, or general-purpose ERP replacement.

## Product Principles

### Reduce Operational Complexity

Every feature should reduce operational complexity instead of increasing it. The platform should simplify how businesses operate rather than merely digitizing existing complexity.

### Simple and Predictable Workflows

Operational workflows should be simple, intuitive, and predictable for the people who use them.

### Information Available for Decisions

Operational information should be available when it is needed to support day-to-day decisions.

### Solve the Most Important Operational Problems First

The Operational MVP should address the most important operational problems before attempting to replace every existing tool or supporting process.

## Domain Overview

The platform operates in the domain of service business operations. Its central domain concept is a **Service**: what the business offers and delivers to its customers or participants. A Service defines what is delivered and may describe characteristics such as its purpose, duration, price, requirements, level, or other relevant attributes.

A **Session** is a specific scheduled occurrence of a Service. It determines when and where the Service is delivered, who is responsible for delivering it, and the operational conditions under which it occurs.

A **Booking** is a commitment that reserves participation or capacity for a Customer or Participant in a Service or Session.

An **Enrollment** represents participation in a Service that normally extends across multiple Sessions, such as a course or program.

**Customer** and **Participant** are distinct concepts. A Customer is the person or entity responsible for the relationship with the business and may be responsible for bookings, enrollments, or payments. A Participant is the person who receives or participates in the Service. The same person may act as both Customer and Participant.

**Staff** are the people involved in operating the business, including specialists or instructors who deliver Services and other supporting roles.

**Resources** are limited assets required for service delivery, such as rooms, spaces, equipment, or other assignable assets.

**Availability** represents whether a Staff member or Resource can be assigned during a given period without violating scheduling or operational constraints.

The core operational relationship is:

**Service → Session → Booking / Enrollment → Attendance / Service Delivery**

The dance studio is the initial reference domain. Examples include classes, private lessons, workshops, instructors, students, guardians, rooms, levels, capacity, attendance, and progression. These examples validate the domain model but do not redefine the core concepts in a dance-studio-specific way.

## Business Capabilities

The platform is organized around business capabilities rather than software features or technical components.

### Core Capabilities

- **Service Management:** Manage what the business offers and delivers as services.
- **Customer Management:** Manage the people or entities that maintain the commercial or operational relationship with the business.
- **Participant Management:** Manage the people who receive or participate in services.
- **Session Management:** Manage scheduled occurrences of services, including their time, capacity, assigned staff, and required resources.
- **Booking Management:** Manage commitments that reserve participation or capacity in services or sessions.

### Supporting Capabilities

- **Staff Management:** Manage the people involved in delivering or supporting business operations.
- **Resource Management:** Manage limited assets required for service delivery, such as rooms, spaces, or equipment.
- **Availability Management:** Determine and manage when staff and resources can be assigned without conflicting with operational constraints.
- **Enrollment Management:** Manage participation in services that extend across multiple sessions, such as courses or programs.
- **Attendance Management:** Track whether participants attend scheduled service delivery.

### Strategic Capabilities

- **Operational Monitoring:** Provide visibility into the current state of business operations.
- **Reporting:** Provide structured information about operational activity and results.
- **Analytics:** Support analysis of operational data to identify patterns, performance, and opportunities for improvement.

## Operational MVP

The first release is an Operational MVP. Its purpose is to validate that a service-based business can use the platform as its primary tool for managing its essential daily operations, while some supporting or advanced processes may continue to use external tools.

The MVP is not intended to replace every existing business tool or implement every platform capability.

### MVP Hypothesis

Service-based businesses are willing to adopt a platform that centralizes their daily operations, even if some supporting processes continue to be managed with external tools during the initial stages.

### Included Capabilities

The Operational MVP includes:

- Participant Management
- Session Management
- Booking Management
- Enrollment Management
- Basic Availability Validation

These capabilities define the initial product scope. Their detailed functional requirements, business rules, scenarios, and acceptance criteria will be defined progressively through feature specifications.

### Deferred Capabilities

The following are intentionally deferred beyond the initial Operational MVP:

- Advanced Service Management
- Advanced Staff Management
- Advanced Resource Management
- Operational Monitoring
- Reporting
- Analytics
- Advanced Availability Management
- Workflow Automation
- Notifications
- Business Configuration Enhancements

Deferred capabilities are not excluded from the product; they are not required to validate the initial Operational MVP.

### MVP Success

The Operational MVP is successful when a target service-based business can manage an entire day of essential operations using the platform as its primary operational tool, while relying on external tools only for non-critical supporting activities.
