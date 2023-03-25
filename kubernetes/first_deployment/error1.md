This command:

```
minikube start 
```

Gets this error:
```
rhyme@ip-10-199-43-234:~$ minikube start
\U0001f604  minikube v1.23.0 on Ubuntu 18.04
\u2728  Using the docker driver based on existing profile
\U0001f44d  Starting control plane node minikube in cluster minikube
\U0001f69c  Pulling base image ...
\U0001f3c3  Updating the running docker "minikube" container ...
\U0001f433  Preparing Kubernetes v1.22.1 on Docker 20.10.8 ...
    \u25aa Generating certificates and keys ...
\U0001f4a2  initialization failed, will try again: wait: /bin/bash -c "sudo env PATH=/var/lib/minikube/binaries/v1.22.1:$PATH kubeadm init --config /var/tmp/minikube/kubeadm.yaml  --ignore-preflight-errors=DirAvailable--etc-kubernetes-manifests,DirAvailable--var-lib-minikube,DirAvailable--var-lib-minikube-etcd,FileAvailable--etc-kubernetes-manifests-kube-scheduler.yaml,FileAvailable--etc-kubernetes-manifests-kube-apiserver.yaml,FileAvailable--etc-kubernetes-manifests-kube-controller-manager.yaml,FileAvailable--etc-kubernetes-manifests-etcd.yaml,Port-10250,Swap,Mem,SystemVerification,FileContent--proc-sys-net-bridge-bridge-nf-call-iptables": Process exited with status 1
stdout:
[init] Using Kubernetes version: v1.22.1
[preflight] Running pre-flight checks
[preflight] The system verification failed. Printing the output from the verification:
KERNEL_VERSION: 5.3.0-1028-aws
DOCKER_VERSION: 20.10.8
DOCKER_GRAPH_DRIVER: overlay2
OS: Linux
CGROUPS_CPU: enabled
CGROUPS_CPUACCT: enabled
CGROUPS_CPUSET: enabled
CGROUPS_DEVICES: enabled
CGROUPS_FREEZER: enabled
CGROUPS_MEMORY: enabled
CGROUPS_PIDS: enabled
CGROUPS_HUGETLB: enabled
[preflight] Pulling images required for setting up a Kubernetes cluster
[preflight] This might take a minute or two, depending on the speed of your internet connection
[preflight] You can also perform this action in beforehand using 'kubeadm config images pull'
[certs] Using certificateDir folder "/var/lib/minikube/certs"
[certs] Using existing ca certificate authority

stderr:
	[WARNING SystemVerification]: failed to parse kernel config: unable to load kernel module: "configs", output: "modprobe: FATAL: Module configs not found in directory /lib/modules/5.3.0-1028-aws\n", err: exit status 1
	[WARNING Service-Kubelet]: kubelet service is not enabled, please run 'systemctl enable kubelet.service'
W0325 17:11:15.215031    1447 certs.go:489] WARNING: could not validate bounds for certificate apiserver: the certificate has expired: NotBefore: 2021-09-12 13:21:49 +0000 UTC, NotAfter: 2022-09-13 13:21:49 +0000 UTC
error execution phase certs/apiserver: [certs] certificate apiserver not signed by CA certificate ca: x509: certificate has expired or is not yet valid: current time 2023-03-25T17:11:15Z is after 2022-09-13T13:21:49Z
To see the stack trace of this error execute with --v=5 or higher


\u256d\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u256e
\u2502                                                                                           \u2502
\u2502    \U0001f63f  If the above advice does not help, please let us know:                             \u2502
\u2502    \U0001f449  https://github.com/kubernetes/minikube/issues/new/choose                           \u2502
\u2502                                                                                           \u2502
\u2502    Please run `minikube logs --file=logs.txt` and attach logs.txt to the GitHub issue.    \u2502
\u2502                                                                                           \u2502
\u2570\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u256f

\u274c  Exiting due to GUEST_START: wait: /bin/bash -c "sudo env PATH=/var/lib/minikube/binaries/v1.22.1:$PATH kubeadm init --config /var/tmp/minikube/kubeadm.yaml  --ignore-preflight-errors=DirAvailable--etc-kubernetes-manifests,DirAvailable--var-lib-minikube,DirAvailable--var-lib-minikube-etcd,FileAvailable--etc-kubernetes-manifests-kube-scheduler.yaml,FileAvailable--etc-kubernetes-manifests-kube-apiserver.yaml,FileAvailable--etc-kubernetes-manifests-kube-controller-manager.yaml,FileAvailable--etc-kubernetes-manifests-etcd.yaml,Port-10250,Swap,Mem,SystemVerification,FileContent--proc-sys-net-bridge-bridge-nf-call-iptables": Process exited with status 1
stdout:
[init] Using Kubernetes version: v1.22.1
[preflight] Running pre-flight checks
[preflight] The system verification failed. Printing the output from the verification:
KERNEL_VERSION: 5.3.0-1028-aws
DOCKER_VERSION: 20.10.8
DOCKER_GRAPH_DRIVER: overlay2
OS: Linux


stderr:
	[WARNING SystemVerification]: failed to parse kernel config: unable to load kernel module: "configs", output: "modprobe: FATAL: Module configs not found in directory /lib/modules/5.3.0-1028-aws\n", err: exit status 1
	[WARNING Service-Kubelet]: kubelet service is not enabled, please run 'systemctl enable kubelet.service'
W0325 17:11:15.215031    1447 certs.go:489] WARNING: could not validate bounds for certificate apiserver: the certificate has expired: NotBefore: 2021-09-12 13:21:49 +0000 UTC, NotAfter: 2022-09-13 13:21:49 +0000 UTC
error execution phase certs/apiserver: [certs] certificate apiserver not signed by CA certificate ca: x509: certificate has expired or is not yet valid: current time 2023-03-25T17:11:15Z is after 2022-09-13T13:21:49Z
To see the stack trace of this error execute with --v=5 or higher


\u256d\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u256e
\u2502                                                                                           \u2502
\u2502    \U0001f63f  If the above advice does not help, please let us know:                             \u2502
\u2502    \U0001f449  https://github.com/kubernetes/minikube/issues/new/choose                           \u2502
\u2502                                                                                           \u2502
\u2502    Please run `minikube logs --file=logs.txt` and attach logs.txt to the GitHub issue.    \u2502
\u2502                                                                                           \u2502
\u2570\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u256f

\u274c  Exiting due to GUEST_START: wait: /bin/bash -c "sudo env PATH=/var/lib/minikube/binaries/v1.22.1:$PATH kubeadm init --config /var/tmp/minikube/kubeadm.yaml  --ignore-preflight-errors=DirAvailable--etc-kubernetes-manifests,DirAvailable--var-lib-minikube,DirAvailable--var-lib-minikube-etcd,FileAvailable--etc-kubernetes-manifests-kube-scheduler.yaml,FileAvailable--etc-kubernetes-manifests-kube-apiserver.yaml,FileAvailable--etc-kubernetes-manifests-kube-controller-manager.yaml,FileAvailable--etc-kubernetes-manifests-etcd.yaml,Port-10250,Swap,Mem,SystemVerification,FileContent--proc-sys-net-bridge-bridge-nf-call-iptables": Process exited with status 1
stdout:
[init] Using Kubernetes version: v1.22.1
[preflight] Running pre-flight checks
[preflight] The system verification failed. Printing the output from the verification:
KERNEL_VERSION: 5.3.0-1028-aws
DOCKER_VERSION: 20.10.8
DOCKER_GRAPH_DRIVER: overlay2
OS: Linux

```



