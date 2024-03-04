download gitbash from https://git-scm.com/downloads
# generate a ssh key #
Use GitBash to generate a new ssh key
ssh-keygen -f <file-name> - 
- this command generates one private and one public key

ssh-keygen -f sarvag
- the private key is stored in the file sarvag
- the public key is stored in the file sarvag.pub

***to see file extension go to control panel -> file explorer options -> view -> uncheck hide extensions for known file types***

# import key pairs in aws ec2 #
1. go to aws console
2. click on ec2
3. click on key pairs
4. click on import key pair
5. browse to the location of the public key created above (ex sarvag.pub) 
    - this key is generated in .ssh folder in home directory
6. click on import key pair
7. give the key pair a name
8. click on import key pair

# creating a aws firewall rule to allow ssh traffic to the server # 
1. go to aws console
2. click on ec2
3. click on security groups
4. click on the create security group (like allow-all)
5. give the security group a name and description (allowing all traffic)
6. click on create security group
7. click on inbound rules 
8. click on edit inbound rules
9. click on add rule
    - select all traffic from the dropdown
    - select 0.0.0.0/0 from the source dropdown
10. click on save rules

***security group = firewall***

# Creating server and connecting to it using ssh #
1. go to aws console
2. click on ec2 
3. click on instances
4. click on launch instance
5. select the server type (like Amazon Linux)
6. select the instance type (like t2.micro)
7. select the key pair (like sarvag)
8. select the security group (like allow-all)
9. click on launch instance

# accessing server with ssh #
1. open gitbash
2. enter the following command
    - ssh -i <private-key-file> <username>@<public-ip>
    - ex: ssh -i sarvag ec2-user@3.238.94.191
- give absolute path of the private key file 
    - ex: ssh -i /c/Users/satish/.ssh/sarvag ec2-user@3.238.94.191

# accessing server using putty #
1. download putty from https://www.putty.org/
2. download puttygen from https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html
3. open puttygen
4. click on load
5. browse to the location of the private key created above (ex sarvag)
6. click on open
7. click on save private key
8. click on yes
9. give the file a name (ex sarvag.ppk)
10. click on save
11. open putty
12. enter the public ip of the server in the hostname field
13. enter the username in the username field (like ec2-user)
14. click on ssh
15. click on auth
16. browse to the location of the private key created above (ex sarvag.ppk)
17. click on open