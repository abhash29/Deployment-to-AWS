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


### How to Publish My Node Module
1. Create a Common Folder
2. Place the folder next to your client and server directories.
3. Write the Code
	Ensure your module's code is properly written and exported.
4. Create an NPM Account
	Sign up at npmjs.com.
	In VS Code, log in using the command:
	sh
	Copy
	Edit
	npm login
	Modify package.json
5. Update the name field:
	json
	Copy
	Edit
	"name": "@100xabhash/common"
	Update tsconfig.json
6. Ensure the following configurations are set:
	json
	Copy
	Edit
	{
  	"rootDir": "src",
  	"outDir": "dist",
  	"declaration": true
	}
7. Publish the Package
	Run the following command:
	sh
	Copy
	Edit
	npm publish --access=public
