# Screenshots

This directory contains visual evidence for the API Troubleshooting Lab. The screenshots are intended to support the main project documentation by showing the lab running, key request/response scenarios, and test results.

The screenshots are not the primary source of truth for the project. The source code, tests, Postman collection, and service documentation remain authoritative. These images provide quick visual context for reviewers, recruiters, and portfolio visitors.

## Directory Layout

```text
screenshots/
├── postman/
├── terminal/
└── test-output/
```

## `postman/`

This folder contains representative API request and response screenshots from the canonical Postman collection.

These screenshots demonstrate the main troubleshooting scenarios exposed through the gateway, including successful requests, authentication failures, validation errors, simulated backend failures, timeout handling, and rate limiting.

## `terminal/`

This folder contains screenshots showing the local services running from the command line.

These images provide context for how the Flask backend and FastAPI gateway are started during local development and testing.

## `test-output/`

This folder contains screenshots of test runs for the backend and gateway services.

These screenshots are included as supporting evidence only. The actual pytest test suites in the backend and gateway repositories should be treated as the authoritative test evidence.

## Notes

The screenshot set is intentionally selective. It is designed to show a useful spread of behaviours without duplicating every scenario already covered by the Postman collection and automated tests.
