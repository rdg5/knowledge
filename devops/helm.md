# Helm

## Notes

- Works like a wrapper around Kubernetes clusters. Has its own artifact repository, you can pull charts and change them similar to docker

### Charts

- Templates are basically the Kubernetes services and deployments. 

- 
```
apiVersion: v1 kind: Service metadata:
name: {{•Release.Name }}-svc
spec:
type: NodePort ports:
- port: 80
targetPort: http protocol: TCP
name: http selector:
app: hello-world
```

- 

```
apiVersion: apps/v1
kind: Deployment metadata:
name:
{{•Release. Name }}-nginx
spec:
replicas: 2 selector:
matchLabels:
app: hello-world template:
metadata: labels:
app: hello-world spec:
containers:
- name: hello-world image: nginx ports:
- name: http containerPort:
80
protocol: TCP
```
- `{{ Release.Name }}` is basically Go templating
- You can create a `values.yaml` file and in that you can define dictionaries for making the namings easier:
```
replicaCount: 2
image:
repository: nginx 
pullPolicy: IfNotPresent
tag: "1.16.0"
```

In this case you can just say `{{Values.repository}}`


- `helm lint ./nginx-chart` is linting the chart same as Terraform does it
## Links
