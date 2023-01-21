### Docker Image Build & run

```bash
$ docker build -t hello-go:1.0 ./go-server
$ docker run --name hello-go-server -p 8000:8000 -d hello-go:1.0
```

### Docker Container Shell

```bash
$ docker exec -it hello-go-server bash
```

### Docker Container Stop & Remove

```bash
$ docker stop hello-go-server
$ docker rm hello-go-server
```

### Minikube Start

```bash
$ minikube start
$ minikube dashboard
```

### Local Image to Minikube

```bash
$ minikube image load hello-go:1.0
```

### kubectl Get Nodes

```bash
$ kubectl get nodes
```

### kubectl Deployment

```bash
$ kubectl create deployment hello-k8s --image=hello-go:1.0 
$ kubectl expose deployment hello-k8s --type=LoadBalancer --port=8000
```

### kubectl Get Pods

```bash
$ kubectl get pods
```

### kubectl Get All

```bash
$ kubectl get all
```

### minikube service on & port-forward

```bash
$ minikube service hello-k8s
$ kubectl port-forward service/hello-k8s 8000:8000
```

### Scale-out Deployment

```bash
$ kubectl scale deployment/hello-k8s --replicas=3
$ kubectl scale deployment/hello-k8s --replicas=2
```

### Remove Deployment & Service

```bash
$ kubectl delete deployment hello-k8s
$ kubectl delete service hello-k8s
```

### Minikube Stop

```bash
$ minikube stop
```