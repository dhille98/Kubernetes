### helm package management pratices

links on online [Refer Here](https://helm-playground.com/)
* [Refer Here](https://helm-playground.com/cheatsheet.html) chet sheet


```yaml
---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: example-deploy
spec:
  replicas: 4
  selector: 
    matchlables:
      app: nginx
      version: "1.0"
  template:
    metadata:
      labels:
        app: nginx
        version: 1.0
    
    spec:
      containers:
      - name: example-con
        image: nginx:1.27
        ports:
        - containerPort: 80
        resources: 
          limits:
            cpu: 100m
            memory: 64Mi
          requests:
            cpu: 200m
            memory: 128Mi
```