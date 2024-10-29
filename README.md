# k8s-cheat-sheet

## Basic Configuration

- Set Configuration Context:

```bash
kubectl config use-context <context-name>
```

- View All Configurations:

```bash
kubectl config view
```

- List All Contexts:

```bash
kubectl config get-contexts
```

## Working with Clusters

- Get Cluster Information:

```bash
kubectl cluster-info
```

- List Nodes:

```bash
kubectl get nodes
```

## Managing Resources

- List All Pods in All Namespaces:

```bash
kubectl get pods --all-namespaces
```

- List Resources in Specific Namespace:

```bash
kubectl get <resource> -n <namespace>
```
`<resource>` can be pods, services, deployments, etc.

## Creating and Managing Pods

- Create a Resource from a File:

```bash
kubectl create -f <filename.yaml>
```

- Get Detailed Information About a Pod:

```bash
kubectl describe pod <pod-name>
```

- Delete a Pod:

```bash
kubectl delete pod <pod-name>
```

## Managing Deployments

- Create a Deployment:

```bash
kubectl create deployment <deployment-name> --image=<image-name>
```

- Get Deployments:

```bash
kubectl get deployments
```

- Update a Deployment:

```bash
kubectl set image deployment/<deployment-name> <container-name>=<new-image>:<tag>
```

## Debugging and Logs

- Fetch Logs of a Pod:

```bash
kubectl logs <pod-name>
```

- Execute Commands in a Container:

```bash
kubectl exec -it <pod-name> -- <command>
```

## Advanced Commands

Port Forwarding to Local Machine:

```bash
kubectl port-forward <pod-name> <local-port>:<pod-port>
```

- Label a Pod:

```bash
kubectl label pods <pod-name> <label-key>=<label-value>
```

- Get API Resources:

```bash
kubectl api-resources
```

## Aliases and Shortcuts

- Short forms for Resources:
1.  Pods: `po`
2.  Services: `svc`
3.  Deployments: `deploy`

 ```bash
kubectl get po/svc/deploy
```

- Useful Aliases:

```bash
alias k='kubectl'
alias kgp='kubectl get pods'
```
