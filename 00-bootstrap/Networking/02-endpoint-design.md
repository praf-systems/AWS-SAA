Why S3 Gateway endpoint reduces NAT dependency
1. For EC2 instances and lamba/others having access to S3 services/endpoints over port https

The 3 SSM endpoints (names)
1. com.amazonaws.us-east-1.ssm
2. com.amazonaws.us-east-1.ssmmessages
3. com.amazonaws.us-east-1.ec2messages

The endpoint SG rule (443 from VPC CIDR)
1. Name: saa-sg-vpce
2. Description: Allow HTTPS from private workloads to VPC endpoints
3. VPC: saa-vpc
4. Inbound rule : HTTPS (443)
   Source: the VPC CIDR 10.10.0.0/16