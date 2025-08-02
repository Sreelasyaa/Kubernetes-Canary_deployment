minikube start
docker build -t orgpulse:v1 ./Orgpulse
docker build -t orgpulse:v2 ./Orgpulse-v2
kubectl rollout restart deployment orgpulse-v1
kubectl rollout restart deployment orgpulse-v2
minikube service orgpulse-service
kubectl apply -f filename
