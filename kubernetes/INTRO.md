Kubernetes is a tool to manage containerised workloads and services.

cluster - a set of node machines that are running containerised applications in pods


Kube Schedule - Assign pods to nodes according to available resources in a logical structure
- more: making sure that Pods are matched to Nodes so that Kubelet can run them


role of Kubelet inside a worker node - Is the primary node agent and takes instructions from the pod-spec and applies them to the pods
 - F allows us to expose the pod to the outside world


Kubelet, Container runtime, and Kube-proxy. - True

node can store a maximum of one pod. - false

labels/selectors - key/value pairs used to group objects like pods so Kubernetes knows what to target for future operations

argetPortshould match the open containerPort - True

