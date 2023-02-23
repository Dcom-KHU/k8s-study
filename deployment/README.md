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


### Reference
- https://subicura.com/k8s/guide/deployment.html#deployment-%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5