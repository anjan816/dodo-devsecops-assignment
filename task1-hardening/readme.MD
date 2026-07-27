The workload receives a dedicated ServiceAccount but no RoleBinding because the application has no requirement to access the Kubernetes API. Granting an empty or unnecessary Role solely to demonstrate RBAC would violate least privilege.

