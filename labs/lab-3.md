# Lab 3: Create a Webserver

* Log into the Amazon AWS console
* Make sure you are in the correct region
* Go into the EC2 service

* Press the “Launch instance” button
* Select Amazon Linux AMI
* Select “t2.micro” instance and press “Next: …” button
* Select your VPC and one of the public subnets
* Enable the “Auto-assign Public IP”
* Press the “Create new IAM role button” and create new role
* Select Amazon EC2 Service Role and select AmazonS3FullAccess, AmazonVPCReadOnlyAccess and AmazonEC2ReadOnlyAccess and press Next and afterwards “Create Role”
* Go back to the “Launch Instance wizard” and select the role you just created and press next
* Don’t change any volume setting and press Next
* Set the Tags according to the DBG requirement (Name, Owner, Creator, CostCenter) and press “Next: …”
* Select create new security group, set the name and description
* And allow access to SSH and HTTP and press “Review and Launch”
* Review the entered data and press the “Launch” button
* Create new Key pair and download the private key

* Wait until the instance is in “running” state
* Use the public IP address to connect to the host using SSH and the key you generated
* Install Nginx webserver using command “sudo yum install nginx”
* Start the nginx service using command “sudo service nginx start”
* To make sure the service starts automatically after reboot, run “sudo chkconfig nginx on”
* Open the IP address / DNS of your host in browser -> You should see the webpage served by your server.
