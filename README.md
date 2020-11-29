# Serverless_DeepLearning-Test-Application

# STEP 1
Attach existing policies directly. Then check AdministratorAccess. Click Next. Then click Next till end and create User
5. Once you create User. You need to copy Access Key ID and secret access Key. Also Download the .CSV file.(If you go to next page, You cannot get this secretKey again. Careful!)
# AWS Account Creation

1. Go to AWS webpage and create a new account
2. Add a Debit/Credit Card and do a transaction verification
3. Choose a Tier you want: Here I chose Free Tier.

# STEP 2 - SETUP YOUR SYSTEM:

# Getting started with SERVERLESS

There are few pre-requisites for our SERVERLESS framework to run on our local machine. I provide the set-up instructions for Ubuntu-Linux version.

Pre-requsites:
1. Python3 and pip3 ( It is needed for our execution of AI Model)
2. Docker - Serverless bundle up our entire code to container before deployment - It is easy to manage with Docker. Please follow the instructions here to install:https://docs.docker.com/engine/install/ubuntu/
3. NodeJS and NPM - This command should work: sudo apt get install -y nodejs. Once after this, check npm --version and node --version
4. Install SERVERLESS with Node Package Manager(NPM): sudo npm install -g serverless

5. Check serverless installation by typing "serverless" in terminal

# STEP 3 - Configuring SERVERLESS with your AWS account:

It is important to give admin access to SERVERLESS from respective AWS account. For this go to IAM MANAGEMENT CONSOLE dashboard. 

1. Click Users
2. Add User
3. Give User-Name of your choice and Give check for programmatic access
4. Click Next(Permissions). In Permissions, Click Attach existing policies directly. Then check AdministratorAccess. Click Next. Then click Next till end and create User
5. Once you create User. You need to copy Access Key ID and secret access Key. Also Download the .CSV file.(If you go to next page, You cannot get this secretKey again. Careful!)

6. After downloaded the .CSV file, come back to terminal. Type sls config credentials --provider aws --key your_key --secret your_secret_code
7. Now your AWS account is added to SERVERLESS local

# STEP 4 HELLO_WORLD SERVERLESS!

1. mkdir some_folder, cd some_folder:
      sls create --template aws-python3 --name helloservice
2. It will create two base files for you. Such as handler.py and serverless.yml
3. Go to serverless.yml, just below fucntions and under handler add memorySize: 128 also add timeout 30
4. Go back to terminal and type: sls deploy
5. Now you can go back and check you lambda function created on your AWS GUI

If this all goes well, Yes you are in the right direction. Please stop here if you stuck with any error.

