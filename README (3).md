# InterviewVerse AI

### AI Powered Smart Interview Assessment: A Multi-Modal Framework for Automated Candidate Evaluation

InterviewVerse AI is an AI-assisted interview assessment platform
designed to connect key stages of candidate evaluation in one workflow.
The project combines a React frontend, a Spring Boot application
backend, a Python FastAPI AI-processing layer, and PostgreSQL
persistence.

> **Project focus:** system-level integration of assessment capabilities
> through service interfaces and a shared candidate workflow. The
> project does not claim to invent the underlying AI models.

## Problem Statement

Recruitment commonly involves resume screening, interviews, coding
assessments, and candidate feedback. When these stages use disconnected
tools, candidate information can become fragmented, evaluation may
require substantial manual effort, and feedback may be delayed.

InterviewVerse AI aims to organize these activities into a connected
workflow with candidate-specific records and consolidated assessment
results.

## Proposed Solution

The React frontend communicates with application services. Spring Boot
manages business workflows such as candidate profiles, interview
sessions, answers, and assessment records. The FastAPI layer exposes
configured AI-processing capabilities, while PostgreSQL stores
persistent application data.

The main contribution is the integration of assessment capabilities
through service interfaces and a shared candidate workflow.

## Key Features

-   **Resume and job-role matching:** resume analysis against a selected
    role where configured.
-   **Interview workflow:** interview sessions, question delivery,
    answer submission, and assessment completion.
-   **AI-assisted answer evaluation:** evaluation using configured
    AI-processing components.
-   **Speech analysis:** speech-to-text or audio analysis where the
    required model and endpoint are configured.
-   **Coding assessment:** programming-task workflow where enabled.
-   **Candidate history and reports:** organized assessment records and
    results for review.
-   **Skill-oriented feedback:** feedback and recommendations as
    corresponding functionality is implemented and validated.

Feature availability depends on the current application configuration.
Do not present optional or planned capabilities as fully implemented
unless verified in the running build.

## Architecture

``` text
                   Candidate / Recruiter
                            |
                            v
                     React Frontend
                            |
                       REST / HTTP
                            |
                            v
                   Spring Boot Backend
                    |               |
                    |               +------> PostgreSQL
                    |
                    | AI service requests
                    v
                   Python FastAPI
                    |
                    v
          Configured AI models / APIs
```

  -----------------------------------------------------------------------
  Component                           Responsibility
  ----------------------------------- -----------------------------------
  React frontend                      Candidate interface and result
                                      presentation

  Spring Boot backend                 Application workflows, API
                                      endpoints, interview/session
                                      handling, and integration

  Python FastAPI service              Configured AI-processing endpoints

  PostgreSQL                          Persistent application and
                                      assessment data

  REST APIs                           Communication between application
                                      components
  -----------------------------------------------------------------------

**Architecture note:** Spring Cloud Gateway, Eureka service discovery,
Prometheus/Grafana monitoring, Docker deployment, and automated CI/CD
should be listed as implemented only if configured and verified in the
submitted build.

## Technology Stack

  -----------------------------------------------------------------------
  Area                                Technology
  ----------------------------------- -----------------------------------
  Frontend                            React, JavaScript, Vite

  Application backend                 Java, Spring Boot, Maven

  AI service                          Python, FastAPI

  Database                            PostgreSQL

  API communication                   REST / HTTP

  Version control                     Git, GitHub

  Optional tools                      Docker, Docker Compose, GitHub
                                      Actions, subject to configuration
  -----------------------------------------------------------------------

List AI libraries and external models only if they are configured in the
repository.

## Course Outcome Mapping

### CO1 --- Architecture Design and Service Implementation

-   Explain the frontend, Spring Boot backend, FastAPI AI service, and
    database responsibilities.
-   Demonstrate REST API communication and the end-to-end workflow.
-   Show how service boundaries support modular development.

### CO2 --- Microservices Security and Observability

-   Demonstrate authentication, authorization, input validation,
    logging, and error handling that exist in the running
    implementation.
-   Protect candidate-specific records and keep credentials out of
    source control.
-   Do not claim JWT, service-to-service security, or monitoring
    dashboards unless configured and demonstrated.

### CO3 --- Service Discovery, Routing, and Database Integration

-   Demonstrate API routes and requests between the backend and AI
    service.
-   Show PostgreSQL persistence for supported candidate and assessment
    data.
-   Treat API Gateway and Eureka as future extensions unless running and
    tested.

### CO4 --- Testing, CI/CD, and Final Demonstration

-   Run available endpoint, unit, integration, or manual API tests and
    record outcomes.
-   Demonstrate the candidate workflow from input to assessment result.
-   Show a CI/CD pipeline or Docker deployment only if configured and
    working.

## Getting Started

Exact commands and environment variables depend on the repository
version. Use the repository configuration and service-specific
instructions as the source of truth.

### Prerequisites

-   Git
-   Node.js and npm for the React frontend
-   Java and Maven for the Spring Boot backend
-   Python and pip for the FastAPI AI service
-   PostgreSQL
-   API credentials or model files required by configured AI components

### Setup outline

1.  Clone the repository:

    ``` bash
    git clone https://github.com/mahathi30093/InterviewVerse-AI.git
    cd InterviewVerse-AI
    ```

2.  Inspect the repository structure and service-specific configuration
    files.

3.  Configure the PostgreSQL connection using the project's
    configuration mechanism.

4.  Install frontend dependencies in the frontend directory using its
    package manifest.

5.  Build and run the Spring Boot service using its Maven configuration.

6.  Install Python dependencies and run FastAPI using the entry point
    defined in the repository.

7.  Start the frontend and verify its API base URL.

8.  Test the documented API endpoints and complete a candidate workflow.

> This README does not invent environment variable names, credentials,
> ports, or commands that must be confirmed from the repository. Never
> commit passwords, API keys, or signing secrets.

## Demonstration Flow

1.  Open the application and enter the candidate workflow.
2.  Select a target job role, where available.
3.  Upload a resume and inspect the analysis.
4.  Start an interview session and submit an answer.
5.  Show the evaluation response and supported speech or coding
    assessment.
6.  Open the candidate result/history view and verify persisted records.
7.  Show API documentation or test evidence and explain the
    architecture.

Demonstrate only features that work in the version being evaluated.
Identify incomplete components as planned work.

## Security and Responsible Assessment

-   Use environment variables or a secrets manager for credentials and
    API keys.
-   Validate user inputs and handle service errors safely.
-   Restrict access to candidate profiles, recordings, and reports.
-   Collect only necessary assessment data and handle it responsibly.
-   Treat observable assessment events as signals for review, not
    definitive proof of misconduct.
-   Keep human review in consequential hiring decisions; AI-generated
    scores should not be the sole basis for rejection.

## Current Scope and Future Work

-   Complete and validate service boundaries and API contracts.
-   Add and test API Gateway routing and Eureka discovery if required.
-   Expand automated unit, integration, and end-to-end tests.
-   Configure Docker Compose and CI/CD after verifying service
    configuration.
-   Add structured logs and monitoring if monitoring infrastructure is
    deployed.
-   Evaluate answer scoring with documented test cases and human review.
-   Improve explainability, accessibility, privacy, and fairness
    evaluation.

Performance or accuracy claims should be added only when supported by
documented experiments and reproducible results.

## Team

  Name                  Roll Number   Role
  --------------------- ------------- -------------
  Vanjari Sai Dhanush   2420030162    Team Lead
  Bandi Srihitha        2420030099    Team Member
  Emani Mahathi         2420030093    Team Member

## Repository

[InterviewVerse-AI on
GitHub](https://github.com/mahathi30093/InterviewVerse-AI)

------------------------------------------------------------------------

*InterviewVerse AI --- integrating assessment workflows for structured,
transparent, and candidate-focused evaluation.*
