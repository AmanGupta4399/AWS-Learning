# Learning
How to create instances

How to create instances by AMI

How to create instances by using Templataes

How to create users & Security groups

How to create Load balancer & Auto Scaling groups

How to create AMI
# Dashboards
in this we know  overview that how many instances , key pairs , snapshots, volumes , load balancer etc are running 
# Ec2 global view 
Region Explorer - in this we can see that in which region how many instances are running which are owned by me


Region & Zones - in this we get region name with its code s well as geographic ares like (Asia, Europe , USA etc)

Availablity zone - i this we get zone name with its loaction and region

Events - in this we get notofications if any mishappening occurs in AWS like any region or zone is out or any other event 

# Instance Categories
Instances are categorized in severral groups

1 Genral purpose - General purpose instances provide a balance of compute, memory and networking resources, and can be used for many workloads. These instances are good for applications such as web servers, code repositories, and small-to-medium databases it generally starts with T & M

2 Compute optimized - for high processors it generally starts with C

3 Memory optimized - for high performance with large memory it generally starts with X , R

4 Storage optimised - They’re designed for workloads that require high, sequential read and write access to very large data sets on local storage. it generally starts with I , D , H

5 HPC - high performance computing for complex simulations, deep learning, and visual effects rendering.it generally starts with H

# Templates
we create  one or more template to craete instances from that,  which already consists all information for that instance (means we dont enter details for our machine manually it takes that information from template )

# Saving Plans 
Resrved instance aslo known as on demand - if we know that we want our machine for 3 years , so instead of 1-1 year we take it for 3 years which cost less this is called reserve instance

it is of 2 types(convertable & non convertable)

Spot instance - in this we bid that i cant pay 3$ I can pay only 2 $ fopr that we use spot instance

Dedicated hosts - we dont know that in which host my virtual machine is running , means in 1 host many virtuals are running for diff diff person
so I can purachse one dedeicated hhost in which only my instance will run, mainly use by banks

# AMI(Amazon MAchine Image)
An Amazon Machine Image (AMI) is a pre-configured template that contains the information required to launch an Amazon EC2 instance. It defines the operating system, application server, applications, and associated configurations

# AMI Catlogue
 IN this we can see AMI created by me or AMI created by AWS community

 # EBS Volume(Elastic Block Store)
  EBS provides persistent storage volumes that can be attached to EC2 instances, allowing you to store data and run applications just like you would with a local hard drive.

  we can extend EBS volume as it is network drive

  we can connect more than one volume with one instance , but one volume will only attach to single isntance at a time

  we can connect our EBS volume with instance of different zone

  if my instance is crashed which is connected with volume , then we can attach that volume with another instance without any data loss

  # IOPS(in volume)

   EBS provides persistent storage volumes that can be attached to EC2 instances, allowing you to store data and run applications just like you would with a local hard drive.

   # Snapshots
   it is use to create a backup of EBS volume , it can be created for single or multiples volumes attached to a single instance
   # Lifecycle Manager
   it is a policy based rule for managing the creation, retention,  copy, and deletion of Amazon EBS Snapshots and EBS-backed AMIs. 
   # Security Groups
   It controls the incoming and outgoing traffic 

   # Elastic Ips
   when we start or stop instances IP of instance will change , so if we want to release any product or application for that we use elastc IPs which will not use by anyone

   # Placement GRoups
   # Key
   this is used to connect our instance , public key is keep with EC2 and private key is kept by end user


   it is of 2 types (.pem , .ppk)
   # Network Interfces
   # Load Balancer
   it is used to distribute the incoming load to different instances for high availability , to reduce server time etc.

   It is of 3 types but now we use only 2 types(Application , Network & Gateway (Gateway is not use now ))

 #  Application Load Balancer
 it works on application layer , it uses for protocols like HTTP , HTTPS

 we commonly uses internet facing beacuse HTTP & HTTPS runs on browser

 we have to atleast select two availability zones and subnet for each zone 

 we can add multiple protocols in a single loader
 # Netwrork Load balancer
 it works on transport layer , it uses protocols like TCP , UPD etc
 # Auto Scaling
 Amazon EC2 Auto Scaling helps you ensure that you have the correct number of Amazon EC2 instances available to handle the load for your application


 In this we specify minimum and maximun number of instances for auto scaling group

 For auto scaling we need template and load balancer 

 While creating auto scaling we have always to put min and max number of instances .

 After launching 0f auto scaling you will see that one instance will automatically goes in running state 

 if we delete our autro scaling group , our instance will also delete but(template & Load balancer will not delete automatically)

 It is of two types : (vertical & horizontal)

 Vetrical Auto Scaling - in this we have only 1 machine (means we always increase the size of same machine)

 Horizontal Auto Scaling - in this we not increase the size of same machine , we create new machine )

 Most common used auto scaling is horizontal auto scaling
  
   

