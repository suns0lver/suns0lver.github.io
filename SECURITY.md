# Security Policy

## Reporting a Vulnerability

If you discover a security issue in the Suns0lver infrastructure, please report it responsibly.

### What Qualifies as a Security Issue

- Code execution vulnerabilities
- Authentication/authorization bypass
- Data exposure or privacy violations
- Dependency vulnerabilities with exploits
- Infrastructure misconfigurations that enable attacks
- Violations of stated structural guarantees (extraction, coercion, surveillance)

### How to Report

**DO NOT** open a public GitHub issue for security vulnerabilities.

Instead, use one of these channels:

1. **GitHub Security Advisories** (preferred)
   - Navigate to the Security tab
   - Click "Report a vulnerability"
   - Provide detailed information

2. **Private disclosure**
   - Email: [security contact will be added]
   - PGP key: [if applicable]

### What to Include

Please provide:
- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Suggested remediation (if known)
- Your preferred attribution (if you want credit)

### Response Timeline

- **Acknowledgment:** Within 48 hours
- **Initial assessment:** Within 1 week
- **Status update:** Every 2 weeks until resolved
- **Resolution:** Depends on severity and complexity

### Safe Harbor

If you:
- Report in good faith
- Do not exploit the vulnerability beyond verification
- Do not access or modify data beyond what's necessary to demonstrate the issue
- Give us reasonable time to fix before public disclosure

Then we will:
- Not pursue legal action
- Work with you on disclosure timing
- Credit you publicly (if desired)

### Scope

This policy covers:
- suns0lver.github.io and all subdomains
- Official Suns0lver repositories
- Infrastructure components under Suns0lver control

Out of scope:
- Social engineering
- Physical attacks
- Third-party services (report to them directly)

### Disclosure Policy

- **Coordinated disclosure preferred:** We'll work with you on timing
- **Default timeline:** 90 days from report to public disclosure
- **Critical issues:** May be disclosed sooner with mutual agreement
- **Credit:** Public acknowledgment unless you prefer anonymity

---

## Security Hardening

Current measures:
- Static site (no backend attack surface)
- Cloudflare DDoS protection
- HTTPS enforced
- CSP headers configured
- Signed commits (GPG)
- Branch protection on main

See `/docs/constitutional-elements.html` for structural security guarantees.

---

**Thank you for helping keep Suns0lver secure and honest.**
