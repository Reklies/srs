# srs
Software Requirement Specification for new-age Online examination system


## Table of Contents

## Software Engineering Practices and Process Models

 Chosen Process Model: Agile with XP (Extreme Programming) Practices
Why Agile?

The system requires iterative refinement (e.g., adapting AI models, improving proctoring UX).

Feedback from stakeholders (teachers, students) is essential.

Continuous updates for security and cheating detection.

XP Practices Used:

Pair Programming (for critical AI components)

Test-Driven Development (TDD)

Continuous Integration (CI)

Refactoring (especially for scalability and modularity)

🔹 Agile Ceremonies & Artifacts
Sprint Duration: 2 weeks

Daily Standups: 15 minutes

Sprint Planning: Backlog grooming + defining sprint goals

Retrospectives: Improve process each iteration

Artifacts: Product Backlog, Sprint Backlog, Burn-down Charts

# 1. Introduction
## 1.1 Purpose
To define the requirements of an Online Examination System (OES) with integrated remote proctoring and AI-based cheating detection.

## 1.2 Scope
This system enables institutes to conduct online exams with the following features:

Exam creation & scheduling

Secure login/authentication

Live remote proctoring

AI-based cheating detection using webcam, mic, screen, and behavior analysis

Result processing and analytics

## 1.3 Definitions, Acronyms, Abbreviations

OES: Online Examination System

AI: Artificial Intelligence

SRS: Software Requirement Specification

## 1.4 References

## 2. Overall Description
## 2.1 Product Perspective

A web-based SaaS application

Modules: Admin, Examiner, Student, AI Monitoring Service

## 2.2 Product Functions

Create/manage tests

Real-time monitoring (live and AI-assisted)

Identity verification

Audio/Video analysis

Cheating alerts/report generation

## 2.3 User Classes and Characteristics

Admin: Setup roles, permissions

Examiner: Create/grade exams

Students: Take exams under surveillance

AI Engine: Background service for cheating detection

## 2.4 Operating Environment

Frontend: React.js or Angular

Backend: Node.js/Django

Database: PostgreSQL or MongoDB

AI Services: Python, TensorFlow

Supported Platforms: Chrome, Firefox, Safari

## 2.5 Constraints

Stable internet required for remote proctoring

Ethical/legal constraints in video/audio monitoring

GDPR/FERPA compliance

 ## 3. Specific Requirements
## Functional Requirements:

FR1: The system shall allow examiners to create time-bound exams.

FR2: The system shall authenticate students via OTP + facial recognition.

FR3: The AI engine shall detect cheating behaviors (e.g., multiple faces, screen switching).

FR4: The system shall alert the proctor in case of suspicious activity.

FR5: The system shall auto-generate cheating reports post-exam.

## Non-Functional Requirements:

NFR1: The system shall have 99.9% uptime during exams.

NFR2: All video/audio data shall be encrypted in transit and at rest.

NFR3: The system shall support 1000+ concurrent users.

NFR4: The system shall comply with accessibility standards (WCAG 2.1).

## 4. External Interface Requirements
UI Requirements: Clean dashboard with test timers, webcam view, and minimal distraction.

API Requirements: RESTful APIs for all data transactions (e.g., /login, /startExam)

Hardware Interface: Web camera, microphone, speakers

Software Interface: Browser, AI module (separate Python microservice)

 ## 5. Appendices
Use case diagrams

Data flow diagrams

Glossary of technical terms

Sample cheating detection AI output (log)
