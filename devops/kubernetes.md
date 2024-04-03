# Kubernetes

## Notes

- Namespace is a logical grouping of resources. It isolates groups in a cluster
- `k` is an alias setup in my `.zshrc` for `kubectl`

- Good way of explaining it to students: `Operating System of the cloud`
- For generating a barebone yaml for a pod, the fastest way is: `k run nginx-yaml --image=nginx --dry-run=client -o yaml > nginx.yaml`
- To delete pods, we can use: `k delete pod ${nameOfPod}`
- To get into the pod we use: `k exec -it ${nameOfPod} -- /bin/bash`, same as docker containers
- Strategy `RollingUpdate` is the default, it's the strategy which waits for the update and then removes the old pods

## Links
