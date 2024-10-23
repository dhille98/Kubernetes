### deployment process

* after that change image version tags `1.0`/ `2.0`
* check that on `kubectl rollout status deployment <deployment_name>`
* uses commands 
```Bash
kubectl get pods /all
kubectl rollout status deployment <deployment_name>
kubectl rollout undo deployment <deployment_name> --to-revision=<number>
```

