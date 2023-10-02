# How to Create a New EC2 Instance

September 15, 2023

By:  Annie V Lam - Kura Labs

## Create a New EC2 Instance
1.  Navigate to https://us-east-1.console.aws.amazon.com
2.  Search "EC2"
3.  Select "EC2"
4.  Select "Instances"
5.  Select "Launch instances"
6.  Give a Name
7.  Under Application and OS Images, select "Ubuntu"
8.  Under Instance type, select an instance type
9.  Under Key pair (login), select a key pair or see below to create a key pair
10. Under Network settings, select "Select existing security group" (If selecting "Create security group, see below)
11. Select a security group that has port 8080
12. Select "Launch instance"
13. To see if the instance is reachable, in a different instance ping it $ping -c 4 ip_address 

### Create a Keypair
1.  Select "Create new key pair"
2.  Enter Key pair name  (if using public EC2 to connect to private EC2, it must be using the same Keypair)
3.  Key pair type, select "RSA"
4.  For Private key file format, select ".pem"
5.  *Create key pair 
   
*This will download a .pem file that you'll need if you are planning to ssh

### Create a Security Group for Custome TCP port 8080 (needed for Jenkins)  

1.   Under Network settings, click "Edit"
2.   Select your VPC
3.   Select your Subnet
4.   For Auto-assign public IP, select "Enable"
5.   Under Firewall (security groups), select "Create security group"
6.   For the Security Group name - required, enter a name for your security group
7.   For the Type rule, select "**Custom TCP**" (This will allow us to ping the instance)
8.   For Port range enter "8080"
9.   For Source type, select "Custom"
10.  For Source, select "0.0.0.0/0"
11.  To Add Other ports, select "Add security group rule" and repeat steps 7 to 10, but replace the port number with your desired port number
 
### To add Custom ICMP - IPv4 (Needed for private and public EC2)
1.  Select "Add security group rule"
2.   For the Type rule, select "**Custom ICMP - IPv4**" (This will allow us to ping the instance)
3.   For Source type, select "Anywhere"

### To add a custom port for SSHing (Needed for private and public EC2)
1.  Select "Add security group rule"
2.  For the Type rule, select "**ssh**"
3.  For Source type, select "Anywhere"

   

