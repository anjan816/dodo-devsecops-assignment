<!-- =========================== -->
<!-- Task 1 README Explanation -->
<!-- =========================== -->

<h1 align="center">🛡️ Task 1 – Kubernetes Application Hardening</h1>

<p align="center">
This task focuses on securing a Kubernetes-based microservice application by implementing security best practices.
The objective is to reduce the attack surface, enforce least-privilege access, protect sensitive information,
and ensure workloads follow Kubernetes security recommendations.
</p>

<hr>

<h2>📌 Objective</h2>

<p>
The primary objective of this task is to transform an insecure Kubernetes deployment into a secure production-ready deployment.
This includes protecting application containers, limiting privileges, encrypting sensitive data, and enforcing secure communication between services.
The implementation follows Kubernetes security best practices together with cloud-native security principles.
</p>

<hr>

<h2>🏗 Application Overview</h2>

<p>
The application consists of multiple microservices deployed inside a Kubernetes cluster.
Each service communicates internally using Kubernetes Services while configuration data is stored separately using ConfigMaps and Secrets.
Security controls are added to protect the workloads without affecting application functionality.
</p>

<hr>

<h2>🔒 Security Hardening Implemented</h2>

<h3>1. Security Context</h3>

<p>
Every container is configured with a restricted security context to prevent privilege escalation.
Containers run as non-root users and unnecessary Linux capabilities are removed.
The root filesystem is mounted as read-only wherever possible to prevent runtime modification.
</p>

<ul>
<li>Run containers as non-root users</li>
<li>Disable privilege escalation</li>
<li>Drop unnecessary Linux capabilities</li>
<li>Read-only root filesystem</li>
<li>Runtime protection using Kubernetes SecurityContext</li>
</ul>

<hr>

<h3>2. Resource Management</h3>

<p>
CPU and memory requests and limits are configured for every workload.
This prevents resource exhaustion attacks and ensures fair scheduling across cluster nodes.
Proper resource allocation also improves application stability during high load.
</p>

<ul>
<li>CPU Requests</li>
<li>CPU Limits</li>
<li>Memory Requests</li>
<li>Memory Limits</li>
</ul>

<hr>

<h3>3. Secret Management</h3>

<p>
Sensitive information is not stored inside application manifests.
Secrets are encrypted before deployment using Kubernetes secret encryption techniques.
Applications consume secrets securely through environment variables or mounted volumes.
</p>

<ul>
<li>Encrypted Secret manifests</li>
<li>No plaintext credentials</li>
<li>Separate configuration from code</li>
</ul>

<hr>

<h3>4. ConfigMap Usage</h3>

<p>
Application configuration is externalized using Kubernetes ConfigMaps.
This enables configuration changes without rebuilding application images and follows cloud-native deployment practices.
</p>

<hr>

<h3>5. Service Accounts</h3>

<p>
Dedicated ServiceAccounts are created for application workloads instead of using the default Kubernetes ServiceAccount.
This minimizes cluster permissions and supports the Principle of Least Privilege (PoLP).
</p>

<hr>

<h3>6. Network Isolation</h3>

<p>
Only required network communication is allowed between workloads.
Kubernetes Services expose only necessary ports while unnecessary external exposure is avoided.
Additional Network Policies are introduced in later tasks for fine-grained traffic control.
</p>

<hr>

<h2>📂 Kubernetes Resources Created</h2>

<table border="1" cellpadding="8">
<tr>
<th>Resource</th>
<th>Purpose</th>
</tr>

<tr>
<td>Deployment</td>
<td>Runs application containers with secure configuration.</td>
</tr>

<tr>
<td>Service</td>
<td>Provides internal service discovery.</td>
</tr>

<tr>
<td>ConfigMap</td>
<td>Stores application configuration.</td>
</tr>

<tr>
<td>Secret</td>
<td>Stores encrypted sensitive information.</td>
</tr>

<tr>
<td>ServiceAccount</td>
<td>Provides dedicated workload identity.</td>
</tr>

<tr>
<td>Ingress</td>
<td>Controls external application access.</td>
</tr>

</table>

<hr>

<h2>⚙ Deployment Process</h2>

<ol>

<li>Create the Kubernetes namespace.</li>

<li>Deploy ConfigMaps and Secrets.</li>

<li>Create dedicated ServiceAccounts.</li>

<li>Deploy application workloads.</li>

<li>Create Kubernetes Services.</li>

<li>Expose the application using Ingress.</li>

<li>Verify workload health.</li>

<li>Validate Kubernetes resources.</li>

</ol>

<hr>

<h2>✅ Validation</h2>

<p>
After deployment, multiple verification steps were performed to ensure that the application remained functional while enforcing the configured security controls.
The application pods started successfully, Services were reachable, and Kubernetes resources were validated using kubectl commands.
</p>

<hr>

<h2>📸 Evidence</h2>

<ul>

<li>Secure Deployment</li>

<li>Encrypted Secret</li>

<li>ConfigMap</li>

<li>ServiceAccount</li>

<li>Application Pods</li>

<li>Kubernetes Services</li>

<li>Ingress</li>

</ul>

<hr>

<h2>🎯 Key Learnings</h2>

<ul>

<li>How Kubernetes SecurityContext protects workloads.</li>

<li>Importance of running containers as non-root.</li>

<li>Benefits of ConfigMaps and Secrets.</li>

<li>Resource management using requests and limits.</li>

<li>Implementing least privilege with ServiceAccounts.</li>

<li>Building production-ready Kubernetes deployments.</li>

</ul>

<hr>

<h2>📖 Conclusion</h2>

<p>
This task successfully transformed a basic Kubernetes deployment into a hardened and production-oriented environment.
Security best practices including non-root execution, encrypted secrets, dedicated ServiceAccounts, resource constraints,
and secure workload configuration significantly improved the overall security posture while maintaining application functionality.
These controls provide the foundation for implementing advanced service mesh security and GitOps workflows in the subsequent tasks.
</p>


