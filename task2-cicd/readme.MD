Source repository
       │
       ▼
commit SHA
       │
       ▼
GitHub workflow
       │
       ▼
build
       │
       ▼
container digest

Provenance helps answer:

Where did this exact container come from?

It does not automatically mean the container is vulnerability-free. GitHub explicitly notes that attestations establish origin/build information, not that an artifact is inherently secure.

Trivy scans the application dependencies and resulting OCI image before publication. Critical and high vulnerabilities with available fixes block publication, preventing known vulnerable artifacts from entering GHCR.

Images are signed using GitHub Actions OIDC and Cosign keyless signing. This avoids maintaining a long-lived signing private key and allows admission controls to verify that an image originated from the trusted GitHub workflow.

# Task 2 — Secure CI/CD & Supply Chain

## Objective

## Architecture

## Threat Model

## Pipeline

## Secret Scanning
Gitleaks

## Static Analysis
Semgrep

## Dependency Scanning
Trivy

## Container Scanning
Trivy

## Container Registry
GHCR

## Immutable Image Strategy

## Image Signing
Cosign Keyless

## Provenance
GitHub Artifact Attestations

## Security Gate Policy

## CVE Exception Policy

## GitOps
Argo CD

## Drift Detection

## Self Healing

## Admission Verification

## Evidence

## Security Decisions

## Limitations




                  Developer
                      │
                      ▼
                    GitHub
                      │
                      ▼
              GitHub Actions
                      │
       ┌──────────────┼──────────────┐
       │              │              │
       ▼              ▼              ▼
    Gitleaks       Semgrep         Trivy
    secrets         SAST       dependency
       │              │              │
       └──────────────┼──────────────┘
                      │
                      ▼
                 Docker Build
                      │
                      ▼
                 Trivy Image
                      │
                PASS / FAIL
                      │
                    PASS
                      │
                      ▼
                     GHCR
                      │
              ┌───────┴────────┐
              ▼                ▼
           Cosign          Provenance
           keyless         attestation
              │                │
              └───────┬────────┘
                      │
                      ▼
               GitOps manifest
                      │
                      ▼
                    GitHub
                      │
                      ▼
                   Argo CD
                      │
                      ▼
                   Kyverno
                      │
                signature OK?
                 /         \
               YES          NO
                │            │
                ▼            ▼
            Kubernetes      DENY
                │
                ▼
            ledger-api