As Cloud Solutions Architects we are used to jumping into implementations when tasked with delivering outputs. 
But taking some time back to think through your solution and maybe coming up with a diagram of the implementation has proven to be better.

Cloud Architecture diagrams are a way to visualize the infrastructure you want to design. This lab will introduce us to Cloud Network architecture diagrams 
using LucidChart.

If you don't have a LucidChart account. You can sign up for one [here](https://www.lucidchart.com/pages/). The free trial is all you need to follow up with the lab. 
After sign up, on the default diagram screen, ensure you enable the AWS architecture libraries for 2017 and 2019 in the Shape Manager.


![S1](https://user-images.githubusercontent.com/103466963/171021811-3f136434-b38f-4a71-87e5-784e9c5a63a9.png)

There are icons and shapes for the various AWS resources. 

We will start off with adding the AWS cloud container shape, It represents your AWS account and all resources it can access.

![S](https://user-images.githubusercontent.com/103466963/171022792-99bcc115-2d5f-40f8-9c14-00c068316a44.png)


Availability Zones (AZ)

An AZ is a data centre (physical building). It is advised to have more than one availability zone to avoid a single point of failure. Let’s add it to the diagram:

![zones](https://user-images.githubusercontent.com/103466963/171023124-7914b08c-4db9-4d85-9f86-443d14cf8ca9.png)


Virtual Private Cloud (VPC)

A virtual private cloud is a pool of networked cloud resources. It can span more than one availability zone. Let’s add the VPC container to the diagram:

![vpc](https://user-images.githubusercontent.com/103466963/171023827-4d0c6df3-085f-4da2-809b-8c6eeecced0e.png)

Subnets

A subnet is a subset of the overall VPC network and it only exists in a single availability zone, unlike its parent network, the VPC which can span over multiple AZs.
Let’s add public subnets to the diagram.

![Subnets](https://user-images.githubusercontent.com/103466963/171024233-ac1e9365-4e80-4213-a8ad-a7b41afd24be.png)

Internet Gateway

The Internet Gateway (IGW) is a resource that enables inbound and outbound traffic from the internet to your VPC. We are going to attach it to the edge of your VPC. Let’s add it to the diagram.

![Sc1](https://user-images.githubusercontent.com/103466963/171024483-85314af6-6cbd-4c3e-9353-25222f968a61.png)

Servers and AutoScaling Group

An autoscaling group manages multiple instances of the same resource (for example, servers), based on need. For instance, when there is a lot of internet traffic to a site, the autoscaling group can start more servers. When there is less traffic, the autoscaling group can reduce the number of servers. 
Let’s add servers (EC2 instances) and an autoscaling group to the diagram.

![Sc45](https://user-images.githubusercontent.com/103466963/171025150-3fb967d0-291c-4929-afbe-6ecb1619a3ab.png)

Load Balancer

A load balancer takes incoming traffic and distributes it to two or more resources. For example, it can take inbound user requests to access your website, and it can distribute the requests evenly among two or more servers. Without a load balancer, having public-facing servers in more than one AZ would mean that users would have to use a different URL to reach each of the AZs. 
This can be impractical compared to just a single URL. Now let’s add it to the diagram.

![S123](https://user-images.githubusercontent.com/103466963/171025496-e368fd58-d673-479a-b9a1-c9636debe9f4.png)

Conclusion

We have looked at various AWS networking resources and also drawn the architecture diagram. Some extra resources that could be added to this infrastructure are RouteTables, Security Groups etc. 
The decision to add resources will be based on the requirements for the architecture you are designing.



