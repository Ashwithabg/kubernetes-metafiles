
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
- get logs `kubectl describe pod pod-name`

*Service & endpoint*
- get services `kubectl get svc -o wide`
- get endpoints `kubectl get endpoints -o wide`
- describe `kubectl describe svc metadatasvc`
- describe endpoints `kubectl describe endpoints metadata-svc-np`

*Metafile*
- apply metafile `kubectl apply -f serviceWithNodePort.yaml`
- delete metafile `kubectl delete -f serviceWithNodePort.yaml` 


***CURL***
```
curl http://node-ip:node-port/actuator/info
curl http://node-ip:node-port/actuator/health
```

*For the Latest version of minikube*
```
minikube start --cpus=4 --memory=8g --driver=hyperkit
```

*deployments*
`kubectl rollout history deployment metadata-service-test`
`kubectl rollout undo deployment metadata-service-test`