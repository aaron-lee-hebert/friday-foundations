# Friday Foundations — 26-Week CISSP Roadmap

## Domain 1 — Security and Risk Management (Weeks 1–4)

- [ ] **Week 1 — The CIA Triad: Confidentiality, Integrity, Availability** — The three properties every security control is trying to protect; how to evaluate any system decision against all three, not just the one that feels most obvious.
- [ ] **Week 2 — Risk management vocabulary: threats, vulnerabilities, and controls** — The precise meaning of threat vs. vulnerability vs. risk, and how a risk register works as a living document rather than a compliance checkbox.
- [ ] **Week 3 — Security governance and policy frameworks** — How organizational security policy flows from business objectives downward into standards, guidelines, and procedures; why developers are often policy consumers without realizing it.
- [ ] **Week 4 — Legal and regulatory landscape: GDPR, HIPAA, SOX, and banking compliance** — The compliance obligations that govern community banking SaaS, what they require of software, and how a security breach becomes a legal event.

---

## Domain 2 — Asset Security (Weeks 5–7)

- [ ] **Week 5 — Data classification and handling** — Confidential vs. internal vs. public; how classification drives encryption requirements, access controls, and retention policies in a multi-tenant SaaS context.
- [ ] **Week 6 — Data ownership and custodianship** — The distinction between who owns data (the business) and who handles it (developers, DBAs, vendors); why this matters for liability and for designing access controls.
- [ ] **Week 7 — Data retention, destruction, and the right to erasure** — Secure deletion vs. simple deletion, how GDPR's right to erasure applies to relational databases with audit logs and backups, and what "sanitization" means for SQL Server.

---

## Domain 3 — Security Architecture and Engineering (Weeks 8–12)

- [ ] **Week 8 — Security design principles: least privilege, defense in depth, and fail-safe defaults** — The small set of principles that underlie most good security decisions; how they translate into concrete choices in ASP.NET Core middleware and SQL Server permissions.
- [ ] **Week 9 — Cryptography fundamentals: symmetric, asymmetric, and hashing** — What AES, RSA, and SHA-256 actually do (without the math); when to use each, and why "we encrypt it" is not a complete security statement.
- [ ] **Week 10 — PKI and certificate management** — How TLS certificates work, what a certificate chain of trust means, and what happens when a cert expires in a production banking SaaS environment.
- [ ] **Week 11 — Secure software design: threat modeling** — STRIDE as a structured way to think about what can go wrong in a system before you build it; walking through a threat model for a feature like vendor access control.
- [ ] **Week 12 — Security models: Bell-LaPadula, Biba, and their real-world echoes** — The theoretical access control models that underpin modern role-based and mandatory access control systems; why understanding the theory makes the implementation choices clearer.

---

## Domain 4 — Communication and Network Security (Weeks 13–15)

- [ ] **Week 13 — Network fundamentals for security: OSI model, TCP/IP, and common protocols** — How data actually moves across a network, where it can be intercepted at each layer, and what TLS protects vs. what it doesn't.
- [ ] **Week 14 — Firewalls, proxies, and network segmentation** — How perimeter and internal network controls work, what a DMZ is, and how Azure Virtual Networks and NSGs implement these concepts in the cloud.
- [ ] **Week 15 — Wireless and remote access security: VPNs, MFA, and Zero Trust** — How remote access risks differ from on-premises, what Zero Trust means as an architecture (not just a marketing term), and why MFA alone isn't sufficient.

---

## Domain 5 — Identity and Access Management (Weeks 16–18)

- [ ] **Week 16 — Authentication vs. authorization: a security lens** — Revisiting the distinction from ASP.NET Core through the CISSP frame: authentication factors, the weakness of passwords, and how multi-factor authentication addresses them.
- [ ] **Week 17 — Identity federation and SSO: SAML, OAuth 2.0, and OIDC** — How single sign-on actually works across organizational boundaries, what trust relationships exist between identity providers and service providers, and how this maps to Azure AD in a banking context.
- [ ] **Week 18 — Privileged access management and the principle of least privilege** — Why admin accounts are the highest-value target in any breach, how PAM solutions manage them, and how this principle applies to SQL Server service accounts and API keys in your SaaS stack.

---

## Domain 6 — Security Assessment and Testing (Weeks 19–21)

- [ ] **Week 19 — Vulnerability assessment vs. penetration testing** — The difference between scanning for known weaknesses and actively exploiting them; what each produces, and what it means for a development team when a pentest report lands.
- [ ] **Week 20 — Code review as a security activity: OWASP Top 10** — The ten most critical web application vulnerabilities, how each manifests in C#/ASP.NET Core, and what a security-focused code review looks for beyond correctness.
- [ ] **Week 21 — Log review, audit trails, and security monitoring** — What a useful audit log contains vs. what most audit logs actually contain; how to design logging in .NET that serves a forensic purpose, not just a debugging one.

---

## Domain 7 — Security Operations (Weeks 22–24)

- [ ] **Week 22 — Incident response: preparation, detection, containment, and recovery** — The six phases of incident response, what a development team's role is when a breach occurs, and why the playbook needs to exist before the incident.
- [ ] **Week 23 — Business continuity and disaster recovery** — RTO vs. RPO as concrete design constraints, how they drive backup strategies and database failover decisions, and what "highly available" actually requires in Azure SQL.
- [ ] **Week 24 — Change management as a security control** — Why undocumented changes are a security risk, how formal change management processes (like those in Azure DevOps) reduce attack surface, and the connection between CI/CD pipelines and change traceability.

---

## Domain 8 — Software Development Security (Weeks 25–26)

- [ ] **Week 25 — Secure SDLC: security at every phase** — Where security activities belong in a development lifecycle (requirements, design, code, test, deploy, operate), and how shifting left on security changes what developers are responsible for.
- [ ] **Week 26 — Supply chain security and third-party risk in software** — NuGet packages, third-party APIs, and vendor SDKs as attack surface; what SBOMs are, why Log4Shell made supply chain a boardroom topic, and how to evaluate the security posture of a dependency.