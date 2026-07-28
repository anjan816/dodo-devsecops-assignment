Semgrep

Critical:
Hard block

High:
Hard block when confirmed exploitable/relevant

Medium:
Security review required

Low:
Informational / backlog


# CI/CD Security Gate Policy

## Secrets

Tool: Gitleaks

Confirmed credential:
BLOCK

Reason:
Secrets must never enter source control or build artifacts.


## SAST

Tool: Semgrep

Critical:
BLOCK

High:
BLOCK after validation

Medium:
Review

Low:
Informational


## Dependency vulnerabilities

Tool: Trivy

Critical + fix:
BLOCK

High + fix:
BLOCK

Critical/High without fix:
Risk review required.


## Container vulnerabilities

Tool: Trivy

Critical + fix:
BLOCK

High + fix:
BLOCK


## Unfixed CVEs

An unfixed CVE requires:

- documented vulnerability
- affected component
- exploitability analysis
- compensating controls
- named owner
- review/expiry date
- upgrade plan


## Container signature

Unsigned production image:
BLOCK


## Provenance

Missing release provenance:
BLOCK release promotion.