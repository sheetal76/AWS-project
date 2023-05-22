# scenario:

We have a small business with three-tier web application.A website and an application server both hosted on an Amazon Elastic compute cloud(EC2) instance.
We have a customer data that is stored on a backend database that we want to keep private.And we use a Amazon VPC to set up a vpc which meets the following requirements:

1) web server,application server and database server must be in a separate subnets.

<img width="769" alt="subnets" src="https://github.com/sheetal76/AWS-project/assets/122160812/fd574b0e-36e2-48fd-a754-d1708b6e36fd">

2)The first address of network starts with 172.20.0.0.
4) Each subnets must have 256 total IP4 addresses.

5) Customers must always be able access web server.To facilitate this subnets must be connected with inernetgateway if its public and to the NAT gateway if its private-subnet

<img width="662" alt="RT" src="https://github.com/sheetal76/AWS-project/assets/122160812/0c125c8c-646a-41b9-ae45-4346dc38020c">



<img width="737" alt="IGW" src="https://github.com/sheetal76/AWS-project/assets/122160812/913a7811-402a-4173-b447-ec2af00a3b5e">



<img width="724" alt="NAT GW" src="https://github.com/sheetal76/AWS-project/assets/122160812/47e45446-ff5a-4146-b166-f51650f19b21">


6) Application server must accept traffic only from our web server.
7) DB server must accept traffic only from application server.
8) Application and DB server must be able to access the internet to make patch updates.
