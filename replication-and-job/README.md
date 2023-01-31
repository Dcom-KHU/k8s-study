---
### 실습 전 참고사항

- hello-go-pod.yaml과 hello-go-pod.yaml은 first-step-of-k8s에서 만들었던 hello-go:1.0을 필요로 합니다.
- 다른 이미지를 사용하고 싶으신 분들은 yaml 내부의 `image: hello-go:1.0`부분을 원하는 이미지 파일 이름으로 수정하시면 됩니다.
---

### 파일을 이용해서 리소스 생성하기

```bash
$ kubectl apply -f hello-go-rs.yaml
```

### Replica Set과 Pod 정보 확인

```bash
$ kubectl get rs,pod
```

### Pod의 label을 포함한 정보 확인

```bash
$ kubectl get rs,pod --show-labels
```

### 실행중인 Pod 삭제하기

```bash
$ kubectl delete pod hello-go-rs-xxxxx
```

### Pod의 spec 수정하기

```bash
$ kubectl edit pod hello-go-rs-xxxxx
```

### Pod의 label 추가하기

```bash
$ kubectl label pod hello-go-rs-xxxxx name=hello-go
```

### Pod의 label 수정하기

```bash
$ kubectl label pod hello-go-rs-xxxxx app=hello --overwrite
```

### Replica Set이 유지할 복제본 개수 바꾸기

```bash
$ kubectl scale rs hello-go-rs --replicas=5
```

### Pod는 남겨두고 Replica Set만 삭제하기

```bash
$ kubectl delete rs hello-go-rs --cascade=orphan
```

### Replica Set과 Replica Set이 관리하는 Pod 모두 삭제하기

```bash
$ kubectl delete rs hello-go-rs
```
