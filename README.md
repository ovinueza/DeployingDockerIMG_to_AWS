# Docker

## Requirements
GitBash

[Docker Desktop](https://www.docker.com/products/docker-desktop)

[Docker Hub account (Free Tier)](https://hub.docker.com/)

AWS account (Free Tier)

## Create EC2 Instance

from console.aws.amazon.com
1) Lauch a Virtual Machine
2) Select Amazon Linux AMI
3) Click Next: Configure Instance Details
4) Next: Add Storage
5) Next: Add Tags
6) Next: Configure Security Group
	* a) Add Rule
	* b) Custom TCP
	* c) Set Port Range to the one specified in the Dockerfile (ie 5000)
	* d) Add IP address. (Use 0.0.0.0/0 for single time use projects)

7) Review and Lauch
8) Lauch
9) On the pop-up window select
	* a) Create a new Key-Pair
	* b) Name the Key-Pair
	* c) Download the Key-Pair and store on a folder near your project
10) Launch Instances
11) View Instances. Make sure instanc is running


## Connect Image





		
