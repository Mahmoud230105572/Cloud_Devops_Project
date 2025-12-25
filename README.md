# # Container Vulnerability Scanner

A Microservices-based application to scan Docker images for vulnerabilities using Trivy, running on Kubernetes.

## Architecture
- **API:** FastAPI service to receive scan requests.
- **Worker:** Background service to perform scans using Trivy.
- **Database:** PostgreSQL to store results.
- **Dashboard:** Web interface to view vulnerabilities.

## How to Run
1. Apply Kubernetes manifests:
   ```bash
   kubectl apply -f .
2. Access Dashboard:
   kubectl port-forward svc/dashboard 5000:5000 
3. Access API:
   kubectl port-forward svc/vuln-api 8000:8000
