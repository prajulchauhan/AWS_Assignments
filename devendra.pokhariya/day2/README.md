# AWS Assignment Day-2

[![N|Solid](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5c/AWS_Simple_Icons_AWS_Cloud.svg/100px-AWS_Simple_Icons_AWS_Cloud.svg.png)](https://nodesource.com/products/nsolid)


### Task 1
> Create a vpc not by wizard this time but manually, having 2 public subnets and 2 private subnets and 2 protected subnets.

* create vpc fromm vpc dashboard your vpc section

![image](images/createvc.png)

********

![image](images/vpc.png)

* create subnet from subnet
(
![image](images/create-subnet.png)

* now you can assign public, private and protected subnet name

![image](images/pub2.png)

-----
-----
![image](images/pv1.png)

> setup should be highly available

![image](images/totalsub.png)

> Create 1 IGW and 2 NGW in each availability zone and make the appropriate routes in route tables

* 


![image](images/nat.png)


> Main route will remain intact, instead make 4 route tables
 - public_route_table
 - private_route_table_1
 - private_route_table_2 
 - protected_route_table

![image](images/rt.png)


### Task 2
> Make LAMP setup with 2 instances in each private subnets. 

* To accomplish this make a Jump server by which you can configure your private instances
    ```
     steps

     1. Create two Instances in private subnet {One Instance in each private subnet}
     2. Create a Jump Server 
     3. Install LAMP in both instance

    ```
    SSh in private Through Jump server

    ![image](images/ssh.png)

    Install Server

    ![image](images/installingLAMp.png)

> Server-1 should serve a webpage that would say "Hi! i am server 1"



> Server-2 should serve a webpage that would say "Hi! i am server 2"


### Task 3

> Launch a public load balancer that would forward the requests to these 2 LAMP instances

* 
![image](images/server2.png)

* 

![image](images/serv1.png)

> create the same setup using aws-cli except vpc

#  NOTE!
  - Machines in the protected subnets shouldn't be going to internet and vice versa (verify this by launching an instance in this subnet)
  - Make Documentation and push to the repo
  - Make sure you copy the actual logs in the documentation rather than assuming that we'll get it `We know nothing`

