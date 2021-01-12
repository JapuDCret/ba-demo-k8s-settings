# Kubernetes Configuration

## **Complete** Deployment

Start

    kubectl apply -f localization-deployment.yaml
    kubectl apply -f address-validation-deployment.yaml
    kubectl apply -f cart-deployment.yaml
    kubectl apply -f order-deployment.yaml
    kubectl apply -f backend4frontend-deployment.yaml

Stop

    kubectl delete -f localization-deployment.yaml
    kubectl delete -f address-validation-deployment.yaml
    kubectl delete -f cart-deployment.yaml
    kubectl delete -f order-deployment.yaml
    kubectl delete -f backend4frontend-deployment.yaml

Quick&Dirty Log Check

    kubectl logs localization-svc-001
    kubectl logs localization-svc-002
    kubectl logs localization-svc-003
    kubectl logs localization-svc-004
    kubectl logs address-validation-svc
    kubectl logs cart-svc
    kubectl logs order-svc
    kubectl logs backend4frontend

### K8S Deployment Diagram

![full-k8s-deployment.png](full-k8s-deployment.png)

## localization-svc

Create

    kubectl apply -f localization-deployment.yaml
    
    minikube service localization-svc

Delete

    kubectl delete -f localization-deployment.yaml

## address-validation-svc

Create

    kubectl apply -f address-validation-deployment.yaml
    
    minikube service address-validation-svc

Delete

    kubectl delete -f address-validation-deployment.yaml

## cart-svc

Create

    kubectl apply -f cart-deployment.yaml
    
    minikube service cart-svc

Delete

    kubectl delete -f cart-deployment.yaml

## order-svc

Create

    kubectl apply -f order-deployment.yaml
    
    minikube service order-svc

Delete

    kubectl delete -f order-deployment.yaml
    
## backend4frontend

Create

    kubectl apply -f backend4frontend-deployment.yaml
    
    minikube service backend4frontend

Delete

    kubectl delete -f backend4frontend-deployment.yaml

## Misc Commands

    kubectl get services
    
    kubectl get deployments
    
    kubectl get pods --output=wide
    
    kubectl describe deployments localization-svc
    
    kubectl describe services localization-svc
    
# Minikube

Start

    minikube start --cpus 4 --memory 16384

Stop

    minikube stop

Start Services

    minikube service localization-svc
    minikube service address-validation-svc
    minikube service cart-svc
    minikube service order-svc
    minikube service backend4frontend