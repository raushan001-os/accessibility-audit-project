# Full-Stack Accessibility Audit --- Architecture

## Project purpose

This repository is a maintainable full-stack foundation created from an
accessibility and architecture review of a public-facing service
website.

## Repository boundaries

``` text
accessibility-audit-project/
├── client/                 # Browser UI
│   └── src/                # React/application source
├── server/                 # Backend/API boundary
│   └── src/                # Routes, controllers, services
├── docs/                   # Audit and architecture documentation
│   ├── screenshots/
│   ├── accessibility-audit.csv
│   └── audit-report.md
├── tests/                  # Cross-layer/e2e test plans
└── README.md
```

### Client

The client owns presentation, user interaction, accessible form
controls, validation feedback, keyboard behavior, and API calls.
Accessibility behavior should be tested at the component level and in
the browser.

### Server

The server owns API routes, request validation, business logic, and
persistence integration. Client-side validation must not be treated as
the only validation boundary.

### Docs

`docs/` contains audit evidence, findings, screenshots, and architecture
notes. Audit evidence is kept separate from application source code.

### Tests

`tests/` is reserved for integration/end-to-end checks, including
keyboard navigation and critical form flows.

## Local setup

The skeleton is intentionally setup-ready rather than a finished
application.

Typical setup after adding the selected framework/tooling:

``` bash
git clone <repository-url>
cd accessibility-audit-project

# client
cd client
npm install
npm run dev

# server
cd ../server
npm install
npm run dev
```

## First vertical feature slice

The first feature should be a small accessible form flow:

``` text
Accessible React form
        ↓
Client validation + visible error
        ↓
HTTP request
        ↓
Server route
        ↓
Request validation
        ↓
Service layer
        ↓
Response
        ↓
Accessible success/error status
```

### Definition of done

-   Every interactive control is keyboard reachable.
-   Focus is visible.
-   Inputs have explicit accessible names.
-   Validation errors are associated with their fields.
-   Dynamic status/error changes are announced appropriately.
-   Server validates incoming data independently.
-   The flow has at least one automated test.
