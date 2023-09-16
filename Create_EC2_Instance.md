# How to Create a New EC2 Instance

September 15, 2023

By:  Annie V Lam - Kura Labs

1.  Navigate to https://us-east-1.console.aws.amazon.com
2.  Search "EC2"
3.  Select "EC2"
4.  Select "Instances"
5.  Select "Lanch instances"
6.  Give a Name
7.  Under Application and OS Images, select "Ubuntu"
8.  Under Instance type, select "t2.micro"
9.  Under Key pairogin), select a key pair
10.  Network settings, select "Select existing security group"
11.  In common security groups, select a key pair (To create a new security group:  [Create Key Pair](Create_Key_Pair.md))
12.  Under Network setting, select "Select existing Security group" (To create a security group:  [Create Security Group](Create_Security_Group.md))
13.  Select a security group that has port 8080
14.  Launch instance
