# Wordpressproject

This project is about setting up a wordpress site on AWS
The objective of this project is to isolate and secure wordpress infrastructure

Firstly 

1. VPC Creation and defining an IP address range for out VPC.
![Vpc](./img/Vpc%20Creation.png)

IP address for the VPC; 

10.0.0.0/16

2.Creation of subnet both public and private, define IP address for each and Availability zones.

![SUBNET DEFINITION FOR PUBLIC AND PRIVATE](./img/2.%20Subnets%20definition.png)
![](img/4.%20Subnet%20asso%201.png)
![](./img/4.%20Subnet%20asso%202.png)

3. Define route tables to route traffic into and out of the VPC.
![ROUTE TABLE CONFIGURATION](./img/3.%20Route%20tables.png)

![ROUTE TABLE](./img/3.%20Route%20tables%202%20private.png)


4. INTERNET GATEWAY : 

it allows resources in the VPC to connect to the internet, to send inbound and outbound traffic.

![](./img/5.%20INTGW.png)
PUBLIC AND PRIVATE SUBNET WITH NAT GATEWAY 
![](./img/6.%20NATGW.png)



5. CREATION OF BATION HOST 

![BASTION](./IMG/7.%20BASTION%20HOST.png)

DEFINING SECURITY GROUP TO ALLOW SSH TRAFFIC 

![BASTION2 ](./IMG/7.%20BASTION%20SG.png)




6. CREATION OF WORDPRESS INSTANCE 
![WORDPRESS](./IMG/7.%20WORDPRESS%20APP.png)



DEFINING SECURITY GROUP TO ALLOW SSH TRAFFIC

![SECURITY GROUP (WORDPRESS)](./img/7.%20WORDPRESS%20SG.png)


INSTALLING ALL THE NECESSARY PACKAGES AND APPLICATIONS

![](./IMG/9%20.%20PHP.png)


![](./IMG/9%20.%20PHP%202.png)


![](./IMG/9.%20MYSQL%20START.png)


7. Database creation with the necessary setup and allowing traffic on port 3306 

![RDS CREATION](./img/21.%20RDS.png)

![RDS SECURITY GROUP](./img/)

![CONNECT WORDPRESS TO DATABASE](./IMG/9.%20Wordpress%20connect%20to%20database.png)

8. EFS CREATION AND MOUNTING IT USING IP ADDRESS FOR SHARED FILE STORAGE FOR OUR WORDPRESS

![EFS Creation](./img/21.%20EFS%20Created.png)


![EFS](./img/21.%20EFS%20Mounted(ip).png)



![EFS](./IMG/21.%20EFS%20Mounted.png)


9. CREATE IMAGE AND A LAUNCH TEMPLATE TO DEFINE CONFIGURATION OF EC2 INSTANCES

![IMAGE AMI](./IMG/13.%20Amazon%20ami.png)

LAUNCH TEMPLATES 
![LAUNCH TEM](./img/14.%20Launch%20template%201.1.png)


![LAUNCH TEM 1.1](./IMG/14.%20Launch%20template%201.1.png)

10. AUTO SCALING FOR PERFORMANCE AND OPRIMIZATION OF THE WORDPRESS SITE.

![AUTO SCALING](./IMG/16.%20Autoscaling%20group.png)



![AUTO SCALING](./IMG/16.%20Autoscaling%20group%201.1.png)




![AUTO SCALING](./IMG/16.%20Autoscaling%20group%201.2.png)



9. TARGET GROUP CREATION IS FOR GROUPING RESOURCES THAT THE APPLICATION LOAD BALANCER WILL BE ROUTING TRAFFIC TO 

![TARGET GROUP](./IMG/17.Target%20Group%201.1.png)


![TARGET GROUP](./img/17.Target%20Group%201.1.png)


![TARGET GROUP](./img/17.Target%20Group%201.2.png)

10. APPLICATION LOAD BALANCER 

![ALB](./img/18.%20Loadbal%20SG.png)


![ALB](./img/18.%20Loadbal%201.2.png)

![ALB](./img/18.%20Loadbal%201.3.png)

![ALB](./img/18.%20Loadbal%201.4.png



11. ASSESSING WORDPRESS VIA DNS FOR ALB 

![Accessing wordpress](./img/12.%20Wordpress%20site.png)


![wordpress site](./img/12.%20Wordpress%20site%201.1.png)

WORD PRESS SITE IS UP, I WENT AHEAD TO FILL THE BLANKS TO CREATE A WORDPRESS.