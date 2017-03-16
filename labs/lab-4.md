# Lab 4: Create an Auto Scaling Group with webservers

* Log into the Amazon AWS console
* Make sure you are in the correct region
* Go into the EC2 service

* Go to Volumes and find the volume of your webserver host
* Make a snapshot of this volume
* Go to Snapshots and wait until the snapshot is ready
* Once the snapshot is completed, create an image from the snapshot. While creating the snapshot, select Virtualization type “Hardware assisted virtualization”
* Go to AMIs and make sure the new AMI image is available

* Go to Loadbalancers and press “Create Loadbalancer”
* Select Classic Load Balancer
* Set the name and select your VPC
* Select the protocol HTTP / port 80 and both of your public networks and press next
* Create new Security group and select type HTTP / port 80
* Don’t change anything on the Health check page and press Next
* Don’t select any instances and press Next
* Set the mandatory tags and press Review and Create
* Review the loadbalancer configuration and press Create

* Go to Auto Scaling Groups and press the “Create Auto Scaling Group” button
* Select “Create a new launch configuration” and press “Next step”
* Select “My AMIs” and select the AMI image you created in previous step
* Select t2.micro instance type and pres Next
* Name your configuration, select the IAM role from Lab 3 and press Next
* Don’t change anything in Storage and press Next
* Select the security group from Lab 3
* Review the Launch configuration and create it
* Select your keypair for SSH access
* Set the name of your ASG and select your VPC and set Group size to 2
* Select both of the private subnets you created in Lab 1
* Check “Receive traffic from one or more loadbalancers”, select the loadbalancer you created before and press Next
* Select “Keep this group at initial size” and press next
* Don’t add any notifications and press Next
* Add all the mandatory tags and check the ”Tag New Instances” checkbox so that the tags get propagated to the host
* Review and create the Auto Scaling Group
* Go to instances and you should see two instances starting

* Go to Loadbalancers again
* Wait until your loadbalancer becomes active
* Find the load balancers DNS name and check that it works
