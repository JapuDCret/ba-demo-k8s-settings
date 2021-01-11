# Kubernetes Configuration

## localization-svc

Create

    kubectl apply -f localization-deployment.yaml
	
	minikube service localization-svc-entrypoint

Delete

    kubectl delete -f localization-deployment.yaml

Restart Deployment

	kubectl rollout restart deployment/localization-svc

# Misc Command

    kubectl get services

    kubectl get deployments
	
    kubectl get pods --output=wide
	
	kubectl describe deployments localization-svc
	
	kubectl describe services localization-svc