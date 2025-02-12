# Deployment-to-AWS
Deployment to AWS
How to run my backend into AWs account
1. Login/Signup to AWS account
2. Create an instance
3. set the inbound rules for port:80/443/3000 including ipv4 and ipv6
4. Save these commands for further use:
	a. ssh -i todo-app-class.pem ubuntu@ec2-16-170-247-204.eu-	north-1.compute.amazonaws.com
	b. icacls todo-app-class.pem /inheritance:r /grant:r "%	USERNAME%":R
	c. npm i -g pm2
	d. pm2 start index.js
5. Clone your code to machine
6. Install node/npm
 --To be continue
