# Security Policy

## Reporting a vulnerability

If you believe you have discovered a security vulnerability in the
ClientCasa TypeScript SDK, please report it privately so we can fix it
before it's exploited.

**Email:** [security@clientcasa.com](mailto:security@clientcasa.com)

Please include:

- A clear description of the vulnerability
- Steps to reproduce
- The version of `@clientcasa/sdk` affected
- Any proof-of-concept code or logs

We aim to acknowledge reports within **1 business day** and to deliver a
fix or mitigation within **14 days** for critical issues.

**Do not file public GitHub issues for security reports.** Public issues
make exploitation easier before a fix is available.

## Scope

This policy covers vulnerabilities in the published `@clientcasa/sdk` npm
package and its source code in this repository — for example:

- Credential leaks through SDK behavior
- Improper request signing
- Dependency vulnerabilities

For vulnerabilities in the **ClientCasa API itself** (the REST endpoints
this SDK calls), please report through the same channel and we'll route
internally.

For vulnerabilities in **third-party dependencies**, please also report
upstream to the dependency maintainer.

## Disclosure

Once a fix is shipped, we'll publish a GitHub Security Advisory and a
patched npm release. With your permission, we'll credit you in the
advisory.

We do not currently run a paid bug bounty program. We're happy to send
ClientCasa swag and a thank-you to researchers who report responsibly.
