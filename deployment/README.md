### Practice for k8s deployment.

### Make deployment
```bash
kubectl apply -f nginx-deploy-v1.yml
```

### Update deployment
```bash
kubectl apply -f nginx-deploy-v2.yml
```

### Check k8s resources
```bash
kubectl get po,rs,deploy
```

### Get status of deployment
```bash
kubectl describe deploy/nginx
```

### Control pod version
```bash
kubectl rollout history deploy/nginx
```



