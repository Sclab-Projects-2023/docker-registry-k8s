this is a local docker registry deployment configuration for k8s


### Deployment

```
kubectl apply -f deployment.yaml  
```

### Run
this docker-registry can be accessed thro localhost:31313 by default

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

