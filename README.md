# Deployment to AWS

## How to Run My Backend on AWS

### Login/Signup to AWS
- Sign in or create an AWS account at [AWS Console](https://aws.amazon.com/console/).

### Create an EC2 Instance
- Launch a new instance based on your backend requirements.

### Set Inbound Rules for Required Ports
- Configure security group inbound rules:
  - **HTTPS:** Allow traffic on port `443`
  - **HTTP:** Allow traffic on port `80`
  - **Custom Backend Port (e.g., 3000):** Allow both **IPv4** and **IPv6**

### Connect to the Instance & Deploy Code
- Clone your backend repository onto the instance.

### Useful Commands for Deployment

**SSH into your EC2 instance:**
```sh
ssh -i todo-app-class.pem ubuntu@ec2-16-170-247-204.eu-north-1.compute.amazonaws.com
```

**Fix permissions for `.pem` file (Windows users):**
```sh
icacls Finance_Visualizer.pem /inheritance:r /grant:r "%USERNAME%":R
```

**Reconnect to the instance using SSH:**
```sh
ssh -i todo-app-class.pem ubuntu@ec2-16-170-247-204.eu-north-1.compute.amazonaws.com
```

**Install PM2 (to keep the backend running in the background):**
```sh
npm i -g pm2
```

**Start the backend process using PM2:**
```sh
pm2 start index.js
```

### Ensure a Secure & Valid URL
- Use **HTTPS** instead of HTTP.
- Ensure the URL does not include `:3000` at the end.

---

# How to Publish My Node Module

### 1. Create a Common Folder
- Place the folder next to your `client` and `server` directories.

### 2. Write the Code
- Ensure your module's code is properly written and exported.

### 3. Create an NPM Account
- Sign up at [npmjs.com](https://www.npmjs.com/).
- In VS Code, log in using the command:
  ```sh
  npm login
  ```

### 4. Modify `package.json`
- Update the name field:
  ```json
  "name": "@100xabhash/common"
  ```

### 5. Update `tsconfig.json`
- Ensure the following configurations are set:
  ```json
  {
    "rootDir": "src",
    "outDir": "dist",
    "declaration": true
  }
  ```

### 6. Publish the Package
- Run the following command:
  ```sh
  npm publish --access=public
  ```

