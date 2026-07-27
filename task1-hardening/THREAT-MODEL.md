Risk: container executes as root
Impact: increases impact of container compromise
Control: runAsNonRoot + explicit UID

Risk: writable root filesystem
Impact: attacker can modify runtime filesystem
Control: readOnlyRootFilesystem

Risk: Linux capabilities
Control: drop ALL

Risk: plaintext Kubernetes secret
Control: encrypted secret management

Risk: default ServiceAccount
Control: dedicated ServiceAccount

Risk: no resource boundaries
Control: requests + limits

Risk: mutable :latest image
Control: immutable tags/digests + admission policy
