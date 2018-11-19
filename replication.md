---
description: >-
  Replication involves sharing information so as to ensure consistency between
  redundant resources, such as software or hardware components, to improve
  reliability, fault-tolerance, or accessibility.
---

# Replication

## Create

What ? Why ? How ? CLI replicaset = rs

#### Exercise n°1

Scale the nginx pod in the namespace app-demo to 5 with the command line.

```text
kubectl scale --replicas=5 -n app-demo nginx
```

#### Exercise n°2

Update the nginx pod YAML file to downscale the nginx pod in the namespace app-demo to 1.

```text
apiVersion: v1
kind: Pod
metadata:
  name: mynginx
  labels:
    env: formation
spec:
  replicas: 1
  containers:
  - name: nginx
    image: nginx
```

```text
kubectl apply -f nginx.yaml
```

## List

What ? Why ? How ?

#### Exercise n°1

List the replicaset created in the namespace app-demo

```text
kubectl get replicaset -n app-demo
```

## Describe

What ? Why ? How ?

#### Exercise n°1

Describe the replicaset of the nginx pod in the namespace app-demo.

```text
kubectl describe replicaset nginx -n app-demo
```

## Delete

What ? Why ? How ?

#### Exercise n°1

Delete the replicaset of the nginx pod in the namespace app-demo

```text
kubectl delete replicaset nginx -n app-demo
```
