# infrastructure_april
## The following Infrastructure as a Code contains provider.tf where u specify a region u want all that to be run in
* Used variables so less hardcoding
* It creates 2 instances: 1 for WEB purposes another one for DB purposes, 
* WEB instance will be in a public subnet and a custom security group will be attached including userdata 
* DB instance will be in a private subnet and a custom security group will be attached including userdata
* Used backend as s3 to store the .tfstate file of that infrastructure 
* It creates a custom VPC with 65,534 IPs by default
* Output feature is applied which will output all the necessary information
* It creates a custom IGW
* It creates a Route Table for IGW
* It creates Subnets - one public and another one private with 256 IPs by default and do Subnet Association
* IT creates by using modules a custom Launch Configuration and Auto Scaling Group
