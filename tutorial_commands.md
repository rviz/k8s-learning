# Hello Minikube

### **01. Open Dashboard with URL**
```sh
minikube dashboard --url
```

### **02. Create a Deployment**
```sh
kubectl create deployment hello-node --image=registry.k8s.io/e2e-test-images/agnhost:2.39 -- /agnhost netexec --http-port=8080

kubectl get deployments

kubectl get pods

kubectl get events

kubectl config view
```

### **03. Create a Service**
```sh
kubectl expose deployment hello-node --type=LoadBalancer --port=8080

kubectl get services

minikube service hello-node
```