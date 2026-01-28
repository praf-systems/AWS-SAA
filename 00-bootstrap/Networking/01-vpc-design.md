1. CIDR plan
VPC CIDR: 10.10.0.0/16
Subnets (4 × /24):
1. Public A:  10.10.0.0/24
2. Public B:  10.10.1.0/24
3. Private A: 10.10.10.0/24
4. Private B: 10.10.11.0/24



2. Subnets list
1. saa-subnet-public-a
2. saa-subnet-public-b
3. saa-subnet-private-a
4. saa-subnet-private-b

Route table logic
1. Public route table -- VPC "saa-vpc" -->> Route table (saa-rt-public) -->> IGW "saa-igw" (For internet connectivity)
2. Subnet association -- 
1. saa-subnet-public-a
2. saa-subnet-public-b

2. Private route table -- VPC "saa-vpc" -->> Route table (saa-rt-private) -->> NAT gateway "saa-nat-a" (for EC2/ASG)
2. Subnet association --
3. saa-subnet-private-a
4. saa-subnet-private-b


NAT cost note (single NAT to control cost)
NAT GW: saa-nat-a 


Any gotchas you hit
None 