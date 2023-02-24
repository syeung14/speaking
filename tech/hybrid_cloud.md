## https://www.youtube.com/watch?v=sUoeVhbp4cQ&list=PLOspHqNVtKABPTyvxoNW0e4XSgCNdZ40F


Now today we're going to go through an example to  lay out some of those advantages and disadvantages  
of a fictional distribution company  that started to undergo that hybrid  
cloud transformation process. Now we're going to  start with what they have kind of on-premises.  
Now right off the bat let's start with  this legacy application that they've got.  
Now this is an application that enables their  users to get shipment and tracking information  
and it continues to work so they don't really  have a good reason to modernize it, although  
it is kind of running on some legacy, old school,  let's say Java EE based monolithic architecture.  

In addition, they've also got some customer  data that's running on-premises. Now this is  
one of the key advantages of hybrid cloud is  it lets you run workloads where you need them.  
So in this particular case to comply with GDPR or maybe some other regulations they need to  
keep that data on-premises which is actually a pretty cool advantage of hybrid cloud that they  
can continue to do that. Now, they've also  got some HR software running on-premises,  
we're going to call this BPMS, or  business process management software,  
and this is going to allow their customers to do or rather their workforce to do things like  
requesting time off, or maybe you know doing some purchase work orders that kind of thing.  
So that's what they've got on-prem. Now we  mentioned that they've started the hybrid cloud  
transformation, they started to take advantage  of cloud native, so let's see what they've done  
in the public cloud. Now we've distilled the cloud  into kind of three major categories in the past,  
so Infrastructure as a Service, Platform  as a Service, and Software as a Service.  
Now, let's start with PaaS and what they've done  here is they've taken advantage of a Kubernetes,  
or container-based environment, maybe even something like managed OpenShift running in  
the cloud to create a new version of the same  application we talked about before the one one  
that works for mobile users. So mobile backend  as well as a database there that kind of works  
for mobile users to be able to get tracking and  shipment information. 

But this led to an increased  cost and support to maintain all those users, so  they started to take advantage of another service  
available in the cloud. So here's where SaaS  comes in. They took a chat bot and they built  
it into that application and that enables them to offset some of that increased support costs.  
In addition, let's say they're also using  some of the SaaS capabilities for IoT  
for their delivery drivers, maybe in their warehouses, their distribution centers, that kind  
of thing. So IoT is helping you know track the goods and maybe making sure they're temperature  
controlled, that kind of thing. And finally, for IaaS, here's an environment that I think kind of  
benefits from lift and shift. So some of  that business process management software  
that they've got running on-prem. Maybe they've  migrated some of that software over to the cloud,  
and I think that's an excellent opportunity to  start taking advantage of IaaS is by kind of doing  
that lift and shift, taking advantage of some of  that software and moving it there. Maybe they're  
also running some CMS systems like WordPress for  content management and they're running that as  
software on some VMs that are made available  through the IaaS capabilities in the cloud.  

Now those two environments are integrated together  because you know they've got some shared data,  
obviously the web interface and the mobile  backend were probably using a similar  
data source. Finally they've also got edge environments, so these are going to be things  
like distribution centers. They're called edge environments because they're at the edge, they're  
where data is being created and these distribution  centers basically enable the customer to do things  
like kind of run workloads right where the data is  being created. So maybe something like Kubernetes,  
or again OpenShift, a distribution of Kubernetes to manage the edge workloads where data is really  
being created. And those are obviously going  to be integrated to the on-premises and cloud  
environments to share data about shipments so their users are getting the latest and greatest  
information about you know where that shipment  is. So this is where the the company is today  
and they've run into a number of challenges.  So number one, they have increased complexity.  
So as they've gone from on-premises to the cloud  and all these engine environments now they have  
kind of an increased number of environments, so their ops teams have to maintain that.  
In addition, they need a way to port assets  from one environment to another. So, so far  
they haven't necessarily run into any issues but  they're starting to build a chat bot into the  
mobile backend and say hey maybe we should start taking advantage of that on our web application  
as well. And they're finding they're not able to easily do that, their DevOps teams are struggling  
because their assets aren't quite portable, maybe they have multiple vendors they're working with  
there isn't that consistency. 

And the  last concern I'll raise is security,  more environments, higher surface area of attack,  their security team has to kind of invest more  
resources to help maintain these solutions. So  there is a solution to all of this and it's taking  
on a unified and open hybrid cloud approach and  that's going to start at the infrastructure layer  
that we've already talked about a little bit. So,  that infrastructure layer is going to be things  
like the on-premises environment, on-premises environment, it's going to be public and private  
cloud environments, as well as edge locations.  But here's where the key piece kind of starts to  
kind of work out. So at the foundational layer  they need to start building some standardization.  
So here's where they can start building in a  consistent operating system. So, something like  
Linux, or RHEL, or Red Hat Enterprise Linux, is  going to help here because their developers can  
work against a single operating system  across these multiple environments.  
And I mentioned RHEL because that brings me  to my next point here the platform layer.
And here's where they're going to be  running something like Kubernetes.  
Kubernetes is great because it gives you  that consistent container based environment  
that works in any kind of location on-premises,  edge, the cloud, but you can even take it a step  
further with OpenShift container platform which  is going to give you that enterprise supported  
approach to containers, and again,  it's great because it runs anywhere.  
Finally, the key to all of this is the solutions.  So this consistency and standardization enables  
customers to focus on standardized solutions  across the board so this can be things like the  
apps that they're developing, or the data that  they need to manage, or even security solutions  
that they're building across the board. And this  is just scratching the surface there's other use  
cases here that I'm not even diving into. Things  like integration, managing these multiple cloud  
environments, automation, that kind of thing. But  this standardized layer and platform enables them  
to focus on solutions that work across the  board. Now this is going to lead to a number  
of advantages. Now the number one thing about  hybrid cloud is that it needs to be portable.  
That means your workloads need to be able to move  across environments. Now we mentioned they've got  
a monolithic legacy application architecture  on-prem, maybe they start pulling in OpenShift,  
or Kubernetes on-premises, start refactoring into  microservices and cloud native based applications,  
and they start having containers for that web  interface application. Now if they want to they  
can start porting those assets to the cloud  and take advantage of the elasticity there to  
scale up and down on demand. Number two, it's  going to be faster innovation. Now with that  
portability their developers can now think in a  new way they can build once and deploy anywhere.  
So that chatbot experience they built for the  mobile backend they're going to be able to  
readily port that to the on-premise experience to  the web user interface experience, the legacy app  
if they modernize it to kind of container-based  architecture. So that's one of the key advantages  
their developers are going to benefit from faster  innovation, reduce time to value, faster go to  
market by taking advantage of the industry's  best, you know DevOps and agile practices. So,  
that's a key part about a hybrid cloud is faster  innovation. And finally, as we mentioned before on  
the security front with that standardized layer of  that OpenShift or Kubernetes that container-based  
environment across the board. You're going to  have consistency for things like pushing out  
compliance policies to these multiple environments  and that's going to be critical here to make sure  
you have that kind of secure and consistent  approach across these multiple environments.  
Now in the interest of standardization  and standardization across the board  
and having that kind of consistent layer.  Imagine if you could handle all of these  
layers, right, infrastructure foundation and  solutions all from a single say public cloud  
environment. That means extending the public  cloud to not just on-premises environment but  
maybe even other clouds and the edge.  Well that's when we're starting to get  
into the concept of Distributed Cloud, so  I urge you to check out my video on that.  
Now with Hybrid Cloud it's going to be paramount  that you take a unified and open approach to truly  
set yourself up for success. If you enjoyed this  video, have any questions be sure to drop a like  
or comment below. Stay tuned and follow us for  more videos like this in the future, Thank you.