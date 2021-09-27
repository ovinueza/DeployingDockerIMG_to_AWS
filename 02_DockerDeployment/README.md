# Deploying Docker Image to AWS EC2

## Requirements
GitBash

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
1) Docker Hub test image
2) Public View
3) Go Back to EC2 Instance View
4) Click on Instance ID and choose Public IPv4 DNS (Copy)
5) Open Anaconda Powershell. Navigate to the folder that contains the image. The AWS .pem file should be store there.
6) Enter the following commands on the Powershell:
	* a) chmod 400 AWSDockerTest.pem
	* b) ssh -i AWSDockerTest.pem
	* c) ec2-user@ (paste Public IPv4 DNS link)
	* d) sudo yum update
	* e) sudo yum install docker
	* f) sudo service docker start
	* g) sudo docker pull image : latest
	* h) sudo docker run --name AWS Test -p 5000:5000 yourname/image_name : latest

## Test
1) Go to AWS Instances
2) Open address
3) Delete https and add :5000 at the end of the url




		
