# Lab 2: VPC and Networking

* Log into the Amazon AWS console
* Make sure you are in the correct region
* Go into the VPC service

* Go to Elastic IPs
* Allocate new Elastic IP for your NAT gateway

* Go to the VPC Dashboard
* Click “Start VPC wizard” button
* Select “VPC with Public and Private Subnets”
* Set the VPC CIDR as 10.0.0.0/16
* Set the VPC name
* Set the CIDR for the public subnet as 10.0.0.0/24, set the name and select AZ where this should be created
* Set the CIDR for the private subnet as 10.0.2.0/24, set the name and select the same AZ as for public subnet
* Select your Elastic IP from step 5
* Press the “Create VPC” button
* The VPC, Internet Gateway and NAT are automatically created as well as the two subnets

* Go to Subnets
* Check the Public Subnet Route table and make sure it contains link to the Internet Gateway
* Check the Private Subnet Route table and make sure it contains link to the NAT
* Create two more subnets: 1 public and 1 private with CIDRs 10.0.1.0/24 and 10.0.3.0/24 and put these subnets into different AZ than the previous subnets
* Make sure the new public subnet is associated with the IGW and the new private subnet is associated with NAT
