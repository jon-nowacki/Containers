start docker

```
sudo systemctl start docker
```

Show docker processes

```
docker ps
```

Start minkube

```
minikube start
```

Check docker processes

```
docker ps
```

This step may not be necessary, it depends on if you get a warning

```
systemctl enable kubelet.service
```

Show the number of pods that already exist.

```
kubectl get pods
```

Cd into the directory

```
cd k8s-proj/
```
Create an empty yaml file
```
touch deployment.yaml
```
Open VS Code
```
code .
```
Create a deployment

```
kubectl apply -f deployement.yaml
```
See if there are pods created.  In this instance 2 pods should be listed.  This matches the yaml file.
```
kubectl get pod
```
Much higher level detail of pod status.
 - Port
 - Image ID
 - Port
 - Host port
 - State
 - Ready
 - Restart Count
 - Environment
 - Mounts
```
kubectl describe pod
```