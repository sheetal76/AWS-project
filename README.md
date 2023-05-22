# scenario:

We have a small business with three-tier web application.A website and an application server both hosted on an Amazon Elastic compute cloud(EC2) instance.
We have a customer data that is stored on a backend database that we want to keep private.And we use a Amazon VPC to set up a vpc which meets the following requirements:

1) web server,application server and database server must be in a separate subnets.
2) The first address of network starts with 172.20.0.0.
3) Each subnets must have 256 total IP4 addresses.
4) Customers must always be able access web server.
5) Application server must accept traffic only from our web server.
6) DB server must accept traffic only from application server.
7) Application and DB server must be able to access the internet to make patch updates.
