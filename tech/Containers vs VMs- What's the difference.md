## https://www.youtube.com/watch?v=cjXI-yxqGTI&list=PLhttcwQhqVrXJJhrwesKtKh8kvgUXt6AB&index=6&t=2s
What's up y'all?
I've got a question for you.
What are virtual machines and containers,
and how do they fit into our modern, cloud-native way of building and architecting applications?
My name's Nigel
and I'm going to try to answer that question for you in four parts.
First, let's talk about some of the differences between virtual machines and containers.
On one side we've got virtual machines, which I'm going to abbreviate as VMs,
which you may have used because `they've been popular` for longer.
And then containers over here on this other side,
which may be a bit newer to you
but you've probably seen them if you're working in the spaces of app modernization,
or you're dealing with microservices,
or anything that demands this new way of building and architecting applications.

And I should say that it's not necessarily new,
but it's been that we're dealing with them a lot more lately.
So, the first thing that i want to bring up is the the level at which virtualization happens.
So, these two technologies are different ways of achieving virtualization,
and virtual machines are what's called "hardware virtualization",
because it happens at the hardware level.
So, we're going to start with our hardware down at the bottom,
because these are computers after all.
And what we have on top of our hardware is what's called a "hypervisor".
And our hypervisor is what's responsible for creating these virtualized
instances of each of the components that make up our machines.
We're talking about processors, RAM, storage, network, cards,
all of these things are being virtualized by our hypervisor.

Whereas with containers, we start, again, with the hardware down at the bottom,
but we build them up a little bit differently
because we have, on top of our hardware, our kernel,
`which is what helps` our software and hardware talk to each other.
And, on top of our kernel, we have our operating system
and we call it our "Host OS" because it's going to be what's hosting all of our containers.
And then, on top of the operating system, we have each container that's running,
C1, C2, containers ... we can run `many dozens` of containers in one instance of an operating system.
And that's why this is called "operating system level virtualization",
because it happens at the operating system level, whereas with our virtual machines we're working at the hardware level.
And this model that `I've drawn out` is our Type 1 hypervisor,
or we call it like ... "full virtualization", or "full system virtualization".

The second thing that I want to bring up is about the type of isolation that we're achieving.
With our virtual machines we're achieving isolation of machines.
So, if we can imagine at our base layer we have one server that's `in a rack` somewhere,
but we want to take our resources and `split them up` so that we're getting much more use out of what we have.
So, we take our hypervisor and we make a "Machine 1",
and we make a "Machine 2", and we make a "Machine 3".
We're creating `what looks like separate workstations`, separate servers out of one,
we're making our one server look like it's many different machines.
And each machine is relatively independent of each other,
like they don't really know about each other and we, interacting with them, `wouldn't necessarily know` that we're even in a virtual machine.
It just appears as if it is another completely different server, machine somewhere else.

Whereas with our containers, we're dealing with process isolation. So, when we're running applications on our laptops
we have them running in usually the same environment.
They can all see what's running at the same time and talk to each other and share resources and things like that,
but when we're dealing with containers, perhaps for security,
we want to make sure that our applications can only see what's absolutely necessary for them to run and nothing else.
And that's what containers allow us to do,
where they're sharing the same operating system, they're sharing the same kernel,
but it's appearing to each container as if they have their own operating system
and `only what's installed in them is the` the libraries that are needed,
as well as the scripts, the code, everything that we need to run our applications and that's it.
And we're able to run all these applications side-by-side and they don't necessarily know about each other.
So, we're dealing with isolation of the process, as opposed to isolation of the machine.

And the third thing that I want to bring up is about how these resources are accessed.
So, again, our hypervisor is creating ... ... with our Type 1 hypervisor, we're creating different machines out of our server,
and that's mainly where the interaction is happening.
We're interacting with what we think is hardware, `but that's being managed for us by the hypervisor to what the actual hardware is.`
Whereas with containers, we're using a couple of features, there are more, but I just want to draw your attention to two features
of the Linux kernel that are allowing this illusion of isolation for our processes.
And the first one that I want to bring up are namespaces,
and they're what is allowing the customization
and the appearance that each instance of the container has its own operating system.
And then we have our "cgroups" (control groups), which are responsible for monitoring and metering our resources
to make sure that we never `tax` our system with containers,
we're limiting the amount of resources they're accessing,
we're monitoring what it is, and being able to control exactly what it is we're giving each container control of.
So, we have a bit of granular control over the resources that are flowing to our containers.
Whereas in our hypervisor, we're creating ... we have the the isolation of our different machines.

And the last thing that I want to talk about is this difference in portability and flexibility.
So, with our virtual machines we have what I like to think of as infinite flexibility of our hardware,
because we're making a different machine out of our server,
we're saying, "this is how many processors that I want this machine to have",
"this is how much RAM I would like it to have",
and we're able to be flexible about the kind of system that we're building.
Whereas with containers, we have infinite portability, is how I like to think of it,
because we have our container that's being defined in a single file
and this is known to a lot of people as a Docker file.

But we have essentially a few lines of text that are saying exactly how to build our container,
how to run our container, what libraries are necessary,
what steps to take to build our container up.
And we take this one file, we run it `on our machine`, we can `spin up` our application.
We store it in a repository somewhere else
and then we're able to run that on different machines.
We can take our one file and be able to make it run pretty much wherever,
there's no hardware limitations, anything like that.
Well, there are some hardware limitations if you built your containers for ARM or x86,
but, `aside from that`, you have a lot of flexibility
in how you're able to run your containers.

I've been speaking a lot about Type 1 virtualization, about Type 1 hypervisors,
but the truth is there's another type of virtualization called Type 2.
So, in our Type 1, where we're dealing with our hypervisor right on top of our hardware,
our Type 2 deals a little bit higher.
And this is probably the kind of virtualization that you `may be used to interacting with daily`,
where we're running something like a virtual box or parallels.
So, we can `take the flexibility that's offered` by our `lightweight` Type 2 hypervisors,
and the `portability` that's offered by containers, and run these together.
We see the technologies around virtual machines maturing, like with KubeVirt,
and we're seeing in newer versions of Kubernetes and OpenShift,
that we can run virtual machines and containers not as competing technologies,
but as technologies that can work together depending on our use-cases.
Thank you so much for `sticking with us` through the video.
If you have any questions please drop us a line below,
and if you want to see more videos like this in the future please like and subscribe to our channel.
And don't forget,
you can grow your skills and earn a badge with IBM CloudLabs,
which are free browser-based, interactive Kubernetes labs.
