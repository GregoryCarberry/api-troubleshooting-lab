
# API Troubleshooting Lab

A multi-repository lab environment designed to simulate and troubleshoot real-world API integration issues.  
The system models a common production architecture where requests flow through an **API gateway layer** before reaching a **backend processing service**.

This repository acts as the **hub and architectural overview** for the entire project.

---

## Architecture Overview

![API Troubleshooting Lab Architecture](diagrams/api-troubleshooting-lab-architecture.svg)

The architecture intentionally separates concerns between a gateway layer and a backend service to replicate real-world API environments.

**Flow:**

Client → API Gateway → Backend API → Response

---

## Repository Structure

This project is intentionally split across multiple repositories to model a realistic multi-service architecture.

| Repository | Purpose |
|------------|--------|
| **api-troubleshooting-lab** | Architecture overview and documentation (this repository) |
| **api-troubleshooting-lab-gateway** | Gateway service responsible for request authentication, rate limiting, and tracing |
| **api-troubleshooting-lab-backend** | Backend API responsible for XML payload processing, validation, and failure simulation |

Repositories:

- Gateway service: https://github.com/GregoryCarberry/api-troubleshooting-lab-gateway
- Backend service: https://github.com/GregoryCarberry/api-troubleshooting-lab-backend

---

## System Components

### API Client

Requests are issued using common API tooling such as:

- `curl`
- Postman
- automated test scripts

These tools simulate external consumers of the API.

---

### API Gateway (FastAPI)

The gateway acts as the **edge layer** controlling access to backend services.

Responsibilities:

- API key authentication
- rate limiting
- request tracing
- forwarding validated requests to the backend

This layer mirrors real-world API gateway behaviour used in production systems.

---

### Backend API (Flask)

The backend service processes incoming requests and intentionally exposes scenarios that commonly cause integration issues.

Responsibilities:

- XML payload handling
- request validation
- simulated integration failures for troubleshooting exercises

This enables the lab to reproduce realistic debugging situations.

---

## Request Flow

1. A client sends an API request.
2. The request reaches the **API Gateway**.
3. The gateway validates authentication and applies rate limits.
4. Valid requests are forwarded to the **Backend API**.
5. The backend processes the XML payload and returns a response.
6. The gateway returns the response to the client.

---

## Skills Demonstrated

This project demonstrates practical knowledge in:

- API gateway architecture
- request validation and tracing
- XML payload processing
- FastAPI service design
- Flask backend service development
- multi-repository project structure
- debugging and troubleshooting API integrations

---

## Repository Layout

```
api-troubleshooting-lab
├── diagrams/       # Architecture diagrams used across the project
├── docs/           # Detailed technical documentation
├── screenshots/    # Visual examples of system behaviour
└── README.md       # Project overview (this file)
```

System-level diagrams are stored here and referenced by the other repositories to avoid duplication.

---

## Purpose of the Lab

The goal of this project is to create a controlled environment for experimenting with:

- API gateway behaviour
- integration debugging
- payload validation failures
- realistic request/response flows

The lab is designed to grow over time as additional troubleshooting scenarios and tooling are introduced.

---

## Future Enhancements

Potential future additions include:

- containerised deployment of the services
- automated integration test scenarios
- structured logging and metrics
- distributed tracing
- infrastructure-as-code deployment examples

---

## License

This project is provided for educational and demonstration purposes.
