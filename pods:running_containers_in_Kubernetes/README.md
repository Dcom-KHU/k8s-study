---

### Pod 생성하기

```bash
$ kubectl apply -f simple-pod.yaml
```

### Pod 정보 확인

```bash
$ kubectl get pod
```

```bash
$ kubectl describe -f simple-pod.yaml
```

### 실행중인 Pod 삭제하기

####### Pod 지정 삭제
```bash
$ kubectl delete pod -f simple-pod.yaml
```
###### 귀찮으면 이걸로 (모든 Resource 삭제)
```bash
$ kubectl delete all --all
```

### Namespace 정보 확인하기

```bash
$ kubectl get ns
```
### Namespace 생성하기

###### namespace 생성 후 생성된 namespace를 사용하는 Pod 추가
```bash
$ kubectl create -f custom-ns.yaml #custom-namespace 생성
$ kubectl create -f simple-pod.yaml -n custom-namespace #pod를 custom-namespace에 추가
```

###### 생성된  namespace 비교하기
```bash
$ kubectl get po --namespace default
$ kubectl get po --namespace custom-namespace
$ kubectl get po
```

### Init Container 생성하기

###### 초기화 컨테이너 생성
```bash
$ kubectl apply -f myapp.yaml
$ kubectl get -f myapp.yaml #STATUS 확인해보기
```

###### 초기화 컨테이너 로그 찍어보기 (ERROR 뜨는게 정상 - 컨테이너 생성 이후 다시 로그 찍어보세요)
```bash
$ kubectl logs myapp-pod -c init-mydb
$ kubectl logs myapp-pod -c init-myservic
```
###### 컨테이너 생성
```bash
$ kubectl apply -f services.yaml
```
