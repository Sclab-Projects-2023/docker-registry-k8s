### Deployment

1. create a namespace
```
kubectl apply -f namespace.yaml  
```
2. create a PVC
```
kubectl apply -f pvc.yaml  
```
3. deploy
```
kubectl apply -f deployment.yaml  
```

### Run

1. port forwarding 5000
```
kubectl port-forward svc/docker-registry-svc -n docker-registry 5000:5000
```
2. test push to localhost
```
docker pull ubuntu
docker tag ubuntu localhost:5000/ubuntu
docker push localhost:5000/ubuntu
```

