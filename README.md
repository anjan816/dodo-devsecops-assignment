<!-- ========================================================= -->

<!--                DODO DEVSECOPS ASSIGNMENT                  -->

<!-- ========================================================= -->

<h1 align="center">🚀 Dodo Payments – DevSecOps Assignment</h1>

<p align="center">
A complete DevSecOps implementation demonstrating Kubernetes Hardening,
Secure CI/CD, Istio Service Mesh Security, and Security Reconnaissance.
</p>

<hr>

<h2>📌 Project Overview</h2>

<p>
This repository contains the implementation of a secure cloud-native application
following DevSecOps best practices.
The project demonstrates workload hardening, supply-chain security,
GitOps deployment, service mesh security, and reconnaissance techniques.
</p>

<hr>



<hr>

<h1>🛡️ Task 1 – Kubernetes Hardening</h1>

<h2>Objective</h2>

<p>
Secure the application deployment using Kubernetes security best practices.
</p>

<h2>Implemented Controls</h2>

<ul>
<li>Dedicated <b>payments</b> namespace</li>
<li>Non-root container execution</li>
<li>Read-only root filesystem</li>
<li>Security Context</li>
<li>Resource Requests &amp; Limits</li>
<li>Liveness Probe</li>
<li>Readiness Probe</li>
<li>ServiceAccount</li>
<li>RBAC</li>
<li>Encrypted Secret</li>
<li>Ingress</li>
<li>Pod Security Admission</li>
<li>Kyverno Policy Enforcement</li>
</ul>

<h2>Evidence</h2>

<ul>
<li>Istio installation verification</li>
<li>Healthy application deployment</li>
<li>RBAC validation</li>
<li>Secret encryption</li>
<li>PodSecurity enforcement</li>
<li>Kyverno admission policies</li>
<li>Root container rejection</li>
<li>Secure deployment success</li>
</ul>

<hr>

<h1>🔐 Task 2 – Secure CI/CD &amp; GitOps</h1>

<h2>Objective</h2>

<p>
Build a secure software delivery pipeline with automated security scanning,
container signing, provenance generation, and GitOps deployment.
</p>

<h2>Pipeline Components</h2>

<ul>
<li>GitHub Actions</li>
<li>Gitleaks</li>
<li>Semgrep SAST</li>
<li>Trivy Filesystem Scan</li>
<li>Docker Image Build</li>
<li>Trivy Image Scan</li>
<li>GitHub Container Registry (GHCR)</li>
<li>Cosign Image Signing</li>
<li>Build Provenance</li>
<li>Artifact Attestation</li>
<li>Argo CD GitOps Deployment</li>
<li>Automatic Drift Detection</li>
<li>Self-Healing Deployment</li>
</ul>

<h2>Security Features</h2>

<ul>
<li>Secret Detection</li>
<li>Static Application Security Testing</li>
<li>Container Vulnerability Scanning</li>
<li>Supply Chain Security</li>
<li>Container Signing</li>
<li>Build Attestation</li>
<li>GitOps Continuous Deployment</li>
</ul>

<hr>

<h1>🕸️ Task 3 – Istio Service Mesh Security</h1>

<h2>Objective</h2>

<p>
Secure east-west traffic using Istio Service Mesh with mutual TLS,
authorization policies, and Kubernetes network policies.
</p>

<h2>Implemented Features</h2>

<ul>
<li>Istio Control Plane Installation</li>
<li>Automatic Sidecar Injection</li>
<li>STRICT Mutual TLS</li>
<li>AuthorizationPolicy</li>
<li>Default Deny Policy</li>
<li>Authorized Service Communication</li>
<li>Unauthorized Request Blocking</li>
<li>Workload Certificates</li>
<li>Network Policies</li>
<li>Configuration Validation using istioctl</li>
</ul>

<h2>Validation</h2>

<ul>
<li>Sidecar Injection Verified</li>
<li>Proxy Synchronization Verified</li>
<li>STRICT mTLS Enabled</li>
<li>Unauthorized Requests Blocked</li>
<li>Authorized Requests Allowed</li>
<li>Certificates Verified</li>
<li>Network Policies Enforced</li>
</ul>

<hr>

<h1>🔎 Task 4 – Security Reconnaissance</h1>

<h2>Objective</h2>

<p>
Perform passive and active reconnaissance against the authorized target
using industry-standard open-source security tools.
</p>

<h2>Reconnaissance Tools</h2>

<table border="1" cellpadding="8" cellspacing="0">

<tr>
<th>Tool</th>
<th>Purpose</th>
</tr>

<tr>
<td>Subfinder</td>
<td>Passive Subdomain Enumeration</td>
</tr>

<tr>
<td>Amass</td>
<td>Asset Discovery</td>
</tr>

<tr>
<td>Assetfinder</td>
<td>Subdomain Enumeration</td>
</tr>

<tr>
<td>httpx</td>
<td>Live Host Detection</td>
</tr>

<tr>
<td>WhatWeb</td>
<td>Technology Fingerprinting</td>
</tr>

<tr>
<td>ffuf</td>
<td>Content Discovery</td>
</tr>

<tr>
<td>sqlmap</td>
<td>SQL Injection Testing</td>
</tr>

</table>

<h2>Activities Performed</h2>

<ul>
<li>Subdomain Enumeration</li>
<li>Technology Fingerprinting</li>
<li>Endpoint Discovery</li>
<li>HTTP Enumeration</li>
<li>Directory Fuzzing</li>
<li>Basic SQL Injection Validation</li>
<li>Evidence Collection</li>
</ul>

<hr>

<h1>🛠️ Technology Stack</h1>

<table border="1" cellpadding="8" cellspacing="0">

<tr>
<th>Category</th>
<th>Technology</th>
</tr>

<tr>
<td>Containers</td>
<td>Docker</td>
</tr>

<tr>
<td>Orchestration</td>
<td>Kubernetes (kind)</td>
</tr>

<tr>
<td>Package Manager</td>
<td>Helm</td>
</tr>

<tr>
<td>GitOps</td>
<td>Argo CD</td>
</tr>

<tr>
<td>Service Mesh</td>
<td>Istio</td>
</tr>

<tr>
<td>Policy Engine</td>
<td>Kyverno</td>
</tr>

<tr>
<td>CI/CD</td>
<td>GitHub Actions</td>
</tr>

<tr>
<td>Registry</td>
<td>GitHub Container Registry (GHCR)</td>
</tr>

<tr>
<td>Container Signing</td>
<td>Cosign</td>
</tr>

<tr>
<td>Security Scanning</td>
<td>Trivy, Semgrep, Gitleaks</td>
</tr>

<tr>
<td>Reconnaissance</td>
<td>Subfinder, Amass, Assetfinder, WhatWeb, httpx, ffuf, sqlmap</td>
</tr>

</table>

<hr>

<h1>📸 Evidence</h1>

<p>
Each task contains an <b>evidence</b> directory with screenshots demonstrating
successful implementation and validation of the required security controls.
</p>

<hr>

<h1>✅ Conclusion</h1>

<p>
This project demonstrates the implementation of modern DevSecOps practices,
including Kubernetes workload hardening, secure CI/CD pipelines,
GitOps automation, service mesh security with Istio,
and reconnaissance using industry-standard security tools.
</p>

<hr>

<p align="center">
<b>Developed as part of the Dodo Payments DevSecOps Assignment</b>
</p>
