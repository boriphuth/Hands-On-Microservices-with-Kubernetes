## Setup minikube
$ minikube start -h
$ minikube start --memory 4096 --kubernetes-version v1.13.0
$ curl -O https://storage.googleapis.com/kubernetes-release/release/v1.13.0/bin/darwin/amd64/kubectl
$ chmod +x ./kubectl
$ sudo mv ./kubectl /usr/local/bin/kubectl
$ kubectl version
$ kubectl port-forward -n kube-system svc/kubernetes-dashboard 9090:80

$ kubectl apply -f 1.nginx-deployment.yaml
$ kubectl apply -f 2.nginx-service.yaml