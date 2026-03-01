### Build and push Docker image

### TODO: React Frontend
- Scaffold React app with Vite in `frontend/`
- Simple form with 4 inputs (sepal length, sepal width, petal length, petal width)
- Submit button that POSTs to backend `/predict`, displays predicted class name
- Use `VITE_API_URL` env var for backend URL
- Multi-stage Dockerfile: Node build + nginx to serve
- nginx config to proxy `/api/*` to backend service (avoids CORS)
- `k8s/frontend-deployment.yaml` — 2 replicas
- `k8s/frontend-service.yaml` — LoadBalancer on port 80
- Change backend `k8s/service.yaml` from LoadBalancer to ClusterIP (only frontend needs external access)
