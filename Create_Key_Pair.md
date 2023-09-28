# Create Key Pair

September 15, 2023

By:  Annie V Lam - Kura Labs

1.  Select "Create new key pair"
2.  Enter Key pair name
3.  Key pair type, select "RSA"
4.  Private key file formate, select ".pem"
5.  *Create key pair 
6.  Under Network settings, click "Edit"
7.  Select your VPC
8.  Select your Subnet
9.  For Auto-assign public IP, select "Enable"
10.  Under Firewarll (security groups), select "Create security group"
11.  For Secrity Group name - required, enter "AWS_SG"
12.  For Type rule 1, select "ssh"
13.  For Source type, select "Anywhere"
14.  Select "Add security group rule"
15.  For Type rule 2, select "Custom ICMP - IPv4" (This will allow us to ping the instance)
16.   For Source type, select "Anywhere"
*This will download a .pem file that you'll need if you 
