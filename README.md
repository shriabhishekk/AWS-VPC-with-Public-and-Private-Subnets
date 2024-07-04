# AWS-VPC-with-Public-and-Private-Subnets
Overview: The VPC has public subnets and private subnets in two Availability Zones. Each public subnet contains a NAT gateway and a load balancer node. The servers run in the private subnets, are launched and terminated by using an Auto Scaling group, and receive traffic from the load balancer. The servers can connect to the internet by using the NAT gateway.

Steps to reproduce the Project:
 ·  Create a VPC with 2 public subnet, 2 private subnet, 2 availability zone 
 and 1 NAT Gateway per availability Zone.

 ·  Create an Auto Scaling group(ASG) with a Launch Template with your 
 desired EC2 Instance(Private Instance) capacity and make sure to provide
 the required ports in inbound rule of the Security group so that there is 
 no security breach in the application.

 ·  Attach an Application Load Balancer to the ASG.

 ·  Once the ASG is created the private EC2 instances are also launched.

 ·  Now create a Bastian Host(Make sure to copy the instances key pair to 
 Bastian Host) and SSH both the EC2 instance as we do not want to 

 provide public ip’s to the EC2’s.

 ·  Once EC2 instances are connected, Deploy your application on the server.
 ·  We will see that the traffic is distributed on all the different servers.
<img width="616" alt="Screenshot 2024-07-05 at 2 10 17 AM" src="https://github.com/shriabhishekk/AWS-VPC-with-Public-and-Private-Subnets/assets/92842067/4d97d81a-e1cc-4f0b-a61a-a426790db285">
