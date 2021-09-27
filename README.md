# Deploy a high-availability web app using CloudFormation
This folder provides code for the "ND9991 - C2- Infrastructure as Code - Deploy a high-availability web app using CloudFormation" project. This folder contains the following files:


## diagram.svg
Diagram of this solution 

## create.sh
Bash script to facilitate creating the stacks

## update.sh
Bash script to facilitate updating the stacks

## project3-infra.yml
Cloudformation template for infrastructure (vpc, subnets, internet gateway, nat gatewayus and routes) to decouple network and servers

## project3-infra.json
Parameters for project3-infra.yml, EnvironmentName and CIDRs for VPC and Subnets

## project3-servers.yml
Cloudformation template for servers (IAMRole, LoadBalancer, Autoscaling group, jumpbox and security groups) 

## project3-servers.json
EnvironmentName for project3-servers.yml, should be the same environmentName than project3-infra.json

## Running example:
- ./create.sh project3-infra project3-infra.yml project3-infra.json 
- ./create.sh project3-servers project3-servers.yml project3-servers.json 

## Project3-servers.yml generate two outputs 
* UdagramUrl
with the application URL 
* SessionManagerUrl 
with url to connect to your instances via Session Manager