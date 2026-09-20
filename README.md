# Accessibility Audit & Full-Stack Foundation

This repository contains the accessibility baseline audit, evidence, and
a setup-ready full-stack project skeleton.

## Contents

-   `docs/audit-report.md` --- audit methodology and five findings
-   `docs/accessibility-audit.csv` --- structured issue register
-   `docs/screenshots/` --- Lighthouse evidence
-   `client/` --- frontend boundary
-   `server/` --- backend boundary
-   `tests/` --- testing boundary

## Audit target

DigiLocker public sign-up/login page.

The captured Lighthouse run has an Accessibility score of 71/100.

## Next implementation step

Implement the first accessible form vertical slice, then add automated
coverage for keyboard navigation, labels, validation errors, and the API
boundary.
