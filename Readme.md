
***Kubernetes Metafiles***
-

***Minikube commands***

- Installation	`brew install minikube`
- run `minikube start --memory 6000 --cpus=4 `
- ssh `minikube ssh`

***Kubectl Commands:***

- installation `brew install kubectl `
- context `kubectl config get-contexts`
- get pods: `kubectl get pods -A -o wide`
- ssh `kubectl exec -it metadata-service-01 -- /bin/bash`
- delete pods `kubectl delete pod pod-name`
- get replica sets `kubectl get rs`
- delete repclica set `kubectl delete rs replica-set-name`
 


