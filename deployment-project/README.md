### Run 

uv run uvicorn app:app --reload --port 8000

### docker 

docker build -f deployment-project/Containerfile -t gsoc-pr-tests/deployment-project .
docker run -p 8000:8000 gsoc-pr-tests/deployment-project

### Test

curl -X POST http://localhost:8000/predict \
    -H "Content-Type: application/json" \
    -d '{"text": "NASA launched a new rocket"}'

### minikube and kubectl
kind create cluster
kubectl apply -f k8s/