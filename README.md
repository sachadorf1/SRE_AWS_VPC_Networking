# SRE_AWS_VPC_Networking
## Internet Gateway
## Subnets
### Route Tables
#### Network Access Control List (NACLs)
##### Security Groups

![](AWS_deployment_networking_security.png)


- What is a VPC?
- AWS isolated virtual network - It allows us to control virtual network environment including selection of your own IP address range, we can create multiple subnets within one VPC with specific network configuration. We can use both IPV4 and IPV6 for most resources, it provides security for your services or instances

- What is an Internet Gateway?
- An internet gateway - can transfer communications between an enterprise network and the internet - it allows internet access into the VPC

- What is a Subnet?
- A Subnet is a segmented piece of a larger network - The goal of a subnet to split a large network into a group of smaller, interconnected networks to help minimise traffic - or navigate traffic securely

- Route Table RT
- RT contains set of rules, called routes, that are used to determine where the network traffic from your subnet or gateway is directed

- Network Access Control List (NACL)
- NACLs are stateless - we have to explicitly allow inbound and outbound rules - they are an added layer of security at subnet level

- 4.3 Billion IP address in the world approximately

- Step 1: Create a VPC with IPV valid CDIR block
- `10.0.0.0/16` - next team member to use `10.101.0.0/16` - 10.102.0.0/16 etc (10.106.0.0/16)

- Step 2: Create internet gateway
- 2.1 Attach the IG to your VPC

- Step 3: Create route table
- 3.1 Edit route and insert your IG `target`

- Step 4: Create public subnet
- `10.0.1.0/24`
- 4.1 associate public subnet with our RT

- Step 5: Create public NACLs
- Set inbound and outbound rules for this

- Step 6: Create a security group for our app