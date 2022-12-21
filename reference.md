# Kubernetes Tutorials
Link: https://kubernetes.io/docs/tutorials/hello-minikube/


## Declarative vs Imperative examples

### Declarative Example
```
kubectl apply -f application/simple_deployment.yaml 
```

application/simple_deployment.yaml 

```yaml
apiVersion: apps/v1

kind: Deployment

metadata:
  name: nginx-deployment

spec:
  selector:
    matchLabels:
      app: nginx

  minReadySeconds: 5

  template:
    metadata:
      labels:
        app: nginx

    spec:
      containers:
        - name: nginx

          image: nginx:1.14.2

          ports:
            - containerPort: 80
```


### Imperative Example
```
kubectl run myapp --image myrepo:mytag --replicas 2
```

# Create deployment
kubectl create deployment hello-node --image=registry.k8s.io/e2e-test-images/agnhost:2.39 -- /agnhost netexec --http-port=8080

