<h1 align="center">🛡️ Task 3 – Istio Service Mesh Security</h1>

<p align="center">
This task focuses on implementing Zero Trust networking using Istio Service Mesh.
The application is secured using automatic sidecar injection, mutual TLS,
authorization policies, and Kubernetes Network Policies.
</p>

<hr>

<h2>📌 Objective</h2>

<p>
The objective is to secure communication between Kubernetes microservices by enforcing encrypted traffic,
identity-based authentication, and fine-grained authorization policies.
Only explicitly authorized workloads are allowed to communicate.
</p>

<hr>

<h2>🔒 Security Features</h2>

<h3>Automatic Sidecar Injection</h3>

<p>
Istio automatically injects Envoy proxy sidecars into application pods.
These sidecars intercept all inbound and outbound traffic,
enabling observability, traffic control, and security enforcement.
</p>

<h3>Mutual TLS (mTLS)</h3>

<p>
Strict mutual TLS is enabled for the namespace.
Every service authenticates itself using X.509 certificates issued by Istio,
ensuring encrypted and authenticated service-to-service communication.
</p>

<h3>Authorization Policies</h3>

<p>
AuthorizationPolicy resources define which workloads are permitted to access specific services.
Unauthorized requests are rejected automatically with HTTP 403 responses.
</p>

<h3>Network Policies</h3>

<p>
Kubernetes Network Policies provide an additional layer of network isolation by restricting pod communication
to only approved traffic flows.
</p>

<h3>Workload Identity</h3>

<p>
Each workload receives a unique SPIFFE identity through Istio.
Identity-based communication eliminates reliance on IP addresses and supports Zero Trust architecture.
</p>

<hr>

<h2>⚙ Components Used</h2>

<ul>

<li>Istio Control Plane</li>

<li>Envoy Sidecars</li>

<li>PeerAuthentication</li>

<li>AuthorizationPolicy</li>

<li>DestinationRule</li>

<li>NetworkPolicy</li>

<li>Kubernetes Services</li>

</ul>

<hr>

<h2>📸 Evidence</h2>

<ul>

<li>Istio Installation</li>

<li>Sidecar Injection</li>

<li>Proxy Status</li>

<li>Strict mTLS</li>

<li>Plaintext Request Rejected</li>

<li>Authorization Success</li>

<li>Authorization Failure (403)</li>

<li>Workload Certificates</li>

<li>Network Policies</li>

<li>Istio Analyze</li>

</ul>

<hr>

<h2>🎯 Key Learnings</h2>

<ul>

<li>Zero Trust Architecture</li>

<li>Mutual TLS</li>

<li>Identity-based Authentication</li>

<li>Service Mesh Security</li>

<li>Policy-based Access Control</li>

</ul>

<hr>

<h2>📖 Conclusion</h2>

<p>
Istio Service Mesh significantly improves Kubernetes security by encrypting all service communication,
authenticating workloads using certificates, and enforcing authorization policies.
Combined with Kubernetes Network Policies, the solution provides a strong Zero Trust security model.
</p>



                    Istio Service Mesh
