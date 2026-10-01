# Security Policy

AetherKube takes the security of cloud-native infrastructure and autonomous remediation workflows very seriously. We appreciate the responsible disclosure of security vulnerabilities by security researchers and the community.

## Supported Versions

Only the latest release branch of AetherKube receives security patches and vulnerability fixes.

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |

## Reporting a Vulnerability

If you identify a security vulnerability or suspect an issue related to:
- Remote command execution (RCE) or shell escape vectors
- RBAC or authorization bypass
- Authentication spoofing or token tampering
- Denial of service or unauthenticated resource exhaustion
- Information leakage or secret exposure

**Please DO NOT open a public GitHub issue.**

### Coordinated Disclosure Process

1. **Email Reports:** Send vulnerability details directly to **security@aetherkube.io** (or create a private GitHub Security Advisory at [Security Advisories](https://github.com/HARSHALJETHWA19/aetherkube-releases/security/advisories/new)).
2. **Include in Report:**
   - Detailed description of the vulnerability.
   - Proof of concept (PoC) or step-by-step reproduction instructions.
   - Affected components (`k8s-ai-service`, `k8s-platform-frontend`, `k8s-agent`).
   - Any suggested mitigations or patches if available.
3. **Response Timeline:**
   - **Initial Acknowledgement:** Within 24-48 hours.
   - **Triage & Assessment:** Within 5 business days.
   - **Patch & Advisory Release:** Within 30 days depending on severity.

## Security Architecture & Best Practices

AetherKube is engineered with defense-in-depth security principles:
- **Local-First & Zero Inbound Telemetry:** All diagnostics and remediation execution run strictly on your local host or private cluster.
- **Least Privilege Execution:** All microservices run under dedicated non-root users (`UID 10001`).
- **Strict Role-Based Access Control (RBAC):** Read-only roles (`viewer`, `security_auditor`, `finops_lead`) cannot perform cluster mutating actions.
- **Hardened Input Sanitization:** Command arguments adhere to RFC1123 DNS subdomains and shell metacharacter rejection filters.
- **Supply Chain Security:** SHA-256 verification on all released binaries and automated dependency audits.
