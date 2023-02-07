### Pod, PV, PVC 생성하기
```
$ kubectl apply -f {해당하는 Yaml 파일명}
```

### Pod 속 Container Shell 열기
```
$ kubectl exec it {해당하는 Pod명} --container {해당하는 Container명} /bin/bash
```

### PV 조회하기
```
$ kubectl get pv
```

### PVC 조회하기
```
$ kubectl get pvc
```

### PV 삭제하기
```
$ kubectl delete pv {PV 이름}
```

### PVC 삭제하기
```
$ kubectl delete pvc {PVC 이름}
```
