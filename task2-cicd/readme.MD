<h1 align="center">🚀 Task 2 – Secure CI/CD Pipeline</h1>

<p align="center">
This task implements a secure Continuous Integration and Continuous Deployment (CI/CD) pipeline for Kubernetes applications.
The pipeline automates code validation, container image creation, security scanning, artifact signing,
and GitOps-based deployment using modern DevSecOps practices.
</p>

<hr>

<h2>📌 Objective</h2>

<p>
The objective of this task is to build an automated CI/CD workflow that not only deploys applications but also integrates
security throughout the software delivery lifecycle. Every code change is automatically validated, scanned,
and deployed only after passing multiple security checks.
</p>

<hr>

<h2>⚙ Pipeline Workflow</h2>

<ol>

<li>Developer pushes source code to GitHub.</li>

<li>GitHub Actions automatically triggers the workflow.</li>

<li>Application source code is compiled.</li>

<li>Docker image is built.</li>

<li>Container image is scanned for vulnerabilities.</li>

<li>Software Bill of Materials (SBOM) is generated.</li>

<li>Container image is digitally signed.</li>

<li>Container image is pushed to the container registry.</li>

<li>GitOps repository is updated.</li>

<li>Argo CD automatically synchronizes Kubernetes deployments.</li>

</ol>

<hr>

<h2>🔒 Security Controls</h2>

<h3>Container Vulnerability Scanning</h3>

<p>
Container images are scanned using Trivy before deployment.
This ensures that critical, high, and medium vulnerabilities are identified early in the CI pipeline.
Deployments only proceed after security validation.
</p>

<h3>Software Bill of Materials (SBOM)</h3>

<p>
An SBOM is generated to provide complete visibility into application dependencies.
This improves software supply chain transparency and simplifies future vulnerability management.
</p>

<h3>Container Signing</h3>

<p>
Container images are digitally signed using Cosign.
Image signing guarantees integrity and allows Kubernetes clusters to verify that only trusted images are deployed.
</p>

<h3>GitHub Actions Automation</h3>

<p>
GitHub Actions automates every build, test, scan, and deployment step.
Automation reduces manual errors while ensuring repeatable and consistent deployments.
</p>

<h3>GitOps Deployment</h3>

<p>
Argo CD continuously monitors the Git repository and synchronizes the Kubernetes cluster whenever deployment manifests are updated.
Git becomes the single source of truth for infrastructure and application deployments.
</p>

<hr>

<h2>🛠 Technologies Used</h2>

<ul>

<li>GitHub Actions</li>

<li>Docker</li>

<li>Trivy</li>

<li>Syft</li>

<li>Cosign</li>

<li>GitHub Container Registry</li>

<li>Argo CD</li>

<li>Kubernetes</li>

</ul>

<hr>

<h2>📸 Evidence</h2>

<ul>

<li>GitHub Actions workflow execution</li>

<li>Docker image build</li>

<li>Trivy scan results</li>

<li>Generated SBOM</li>

<li>Cosign signature verification</li>

<li>GitOps repository update</li>

<li>Argo CD synchronization</li>

</ul>

<hr>

<h2>🎯 Key Learnings</h2>

<ul>

<li>Building secure CI/CD pipelines</li>

<li>Container vulnerability scanning</li>

<li>Software supply chain security</li>

<li>GitOps deployment strategy</li>

<li>Automated Kubernetes deployments</li>

</ul>

<hr>

<h2>📖 Conclusion</h2>

<p>
The secure CI/CD pipeline successfully integrates automation and security into the software delivery lifecycle.
Every deployment is validated through vulnerability scanning, dependency analysis,
digital signing, and GitOps synchronization, ensuring reliable and secure application releases.
</p>


<h1>ARCHITECTURE</h1>






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