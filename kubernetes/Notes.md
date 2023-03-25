=Master Node=

Spec and the State: the state is the current state of the system and the spec is the new state that we actually provide to kubernetes and how we want the system to actually look.


Controller: If something fails, the controller finds out about it and notices and response.
If there's any sort of tasks that need to be run, then the controller will pick that up, run them for us until they're actually done etcetera.

cluster store: which is also known as the etcd 
And the way to think about this cluster store is pretty much a key value pair storage that represents all of the state of our cluster living in this XXX. It's pretty much the ultimate source of truth for the whole of our cluster.

Worker Nodes
 - Kubelet: takes the instructions from the pot spec which describes pod mainly from the api server and it just ensures that the containers are working properly.  It takes the instructions from the pod spec which describespod mainly from the api server and it just ensures that the containers are healthy and running
accordingly.
 - Container Runtime - communicate with containers
 - Kube-proxy - connection and networking, reduce network overhead
 - Pod 1
 - Pod 2
 - Container



actually being booted on these pods.
This is the primary machine.
And so it doesn't need a c
And finally we've got the Q proxy which really is responsible
for handling connection and networking that are needed
for the systems to actually work.
It makes smart decisions to reduce the network overhead
wherever it can.
Okay so we have our node and then we have the setup that's
required to run the note.
And then we have these pods that are actually on this note
itself as we said before, it's the main thing that we
actually deploy ourselves.
When we write a deployment we describe a pod and it's usually
the smallest deployable unit in kubernetes.
That's not actually container itself there.
She lives on top of these pots or inside of the pots.
Now upon itself will usually be at least one container
or a group of containers.
And the pod has his own network resources and its own storage,
a shared storage resource inside each pod and each pod will
actually have its own I. P.
Address which is accessible or reachable by the node and also
by other pods inside of this network.
So this private network is actually created
inside of the node for all these pods to communicate
with each other if necessary but not accessible
from the outside world unless we actually enable that later
will discuss that.
And so the pot itself will normally contain at least our
application container.
This is like a docker container with our application on it.
So as we know inside of this application is usually no Js
installed or python actually installed.
And inside of this pod it sets up like an internal network
as well, which is like a local host.
So inside of here we have this local host.
And if you have more than one container, they can communicate
to each other across this local host.
Just as an idea in terms of a normal type of setup,
if you have like an application container on the pod,
if you wanted to have multiple containers, this generally
an advanced use case.
Um but you may have for example an application container
and then maybe a volume.
This volume would have some kind of shared storage
that will be used amongst any other containers on this
on this pot itself.
Or you could have maybe your application container and innit
container which will actually be run before the actual main
container.
Maybe to run some kind of script to set everything up for pre
conflict script or something.
Um you can also have sidecar containers.
Much of this.
We're not going to cover inside of this course.
But if we had something like a sidecar container
that will run like a tailing log file, would be able
to access that container potentially from the outside and see
live logs of things are actually happening.
Maybe inside of one of the other containers, uh essentially
it's just one or more contains living inside this pod
on this local host network.
Okay. So now we've had a look at this um a bit more detail.
We discussed the relationship between the master node
and the worker notes and the master node and one or more work
on those making up the cluster and we discussed
ourselves communicating to the master node with instructions
or rest api requests that hit the server, which tell
the master to do things to bring up new pods or take them
down. We provide a new state to the master and the master
cleverly knows the old state which you can get
from this cluster store or at C.
D is it's often the known um and I can go ahead and with our
new spec spin up our cluster according to whatever our new
spec actually is or make any corrections, um doing a lot
of other clever stuff in the background like false tolerance
and making sure that everything is always up.
We now have a really good idea to go ahead in the next task
and actually write our first deployment and we spoke
about this deployment being this desired state
and that the controller itself looks at the old state
and changes the actual states to the desired state.
So we're gonna go ahead and do that in the next task.
We have provided a lot of repetition of concepts
across this course so far in order to really hold a lot
of these concepts down and now, hopefully, even
though everything is still going to be a little bit muddled
in your mind, once we start writing it
out and start discussing things line by line in our actual
deployments, it should become a lot more clear to you exactly
what's going on, what we're doing and the instructions line
by line of how we actually create these clusters.
So awesome work.
I look forward to seeing you on the next exercise when
we're going to start writing our first deployment.
See you there.



Courses
 - https://www.coursera.org/learn/kubernetes-basic-architecture-first-deployment/ungradedLti/BDxG6/kubernetes-basic-architecture-and-first-deployment

