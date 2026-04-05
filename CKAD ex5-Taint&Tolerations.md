# CKAD ex5-Taint&Tolerations

> **Tasks**:
>
> 1. Taint a node with key=value:NoSchedule.
> 2. Create a pod that tolerates the taint.

1. **Taint a Node:**
  ```bash
  # Taint node (replace NODE_NAME with your node)
  k taint nodes NODE_NAME key=value:NoSchedule
  ```
2. **Tolerate a pod with the taint**  
create a pod:
  ```
  vim nginx-resource.yaml
  -----------------------------------------
  apiVersion: v1
  kind: Pod
  metadata:
    name: pod-toleration
  spec:
    containers:
      - name: nginx
        image: nginx
    tolerations:
      - key: "key"
        operator: "Equal"
        value: "value"
        effect: "NoSchedule"
  ```
  ```
  k apply -f pod-with-toleration.yaml
  ```

 

 