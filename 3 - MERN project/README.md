# Project MERN

![MERN stack](https://github.com/santiagosaes/DevOps-Project/blob/main/3%20-%20MERN%20project/images/mernstack.png)

## Objetives
1.  To gain a hands-on experience in Linux server administration
2. Setting up a robust and scalable web server infrastructure
3. Deploy a simple To-DO application that creates To-Do lists.
4. Create a MongoDB database that communicates with this To-Do application and stores to-do list.
5. Get familiar with RESTful API

## In this project, you are tasked to implement a web solution based on MERN stack in AWS Cloud.

## MERN Web stack consists of following components:
- MongoDB: A document-based, No-SQL database used to store application data in a form of documents.
- ExpressJS: A server side Web Application framework for Node.js.
- ReactJS: A frontend framework developed by Facebook. It is based on JavaScript, used to build User Interface (UI) components.
- Node.js: A JavaScript runtime environment. It is used to run JavaScript on a machine rather than in a browser.

As shown on the illustration above, a user interacts with the ReactJS UI components at the application front-end residing in the
browser. This frontend is served by the application backend residing in a server, through ExpressJS running on top of NodeJS.

Any interaction that causes a data change request is sent to the NodeJS based Express server, which grabs data from the MongoDB 
database if required, and returns the data to the frontend of the application, which is then presented to the user.

## Preparing prerequisites

- You have an AWS account set up and have an Admin user created with full admin permissions. Click the link: Getting Started on AWS for a detailed step-by-step guide on how to create an AWS account.
- Create a key pair and a security group
- Basic knowledge of AWS
- Basic knowledge of Linux
- Basic knowledge of how to create an EC2 instance.
- Basic SSH knowledge
- Basic knowledge of Database management Systems and the difference between Relational and Non-relational databases.


In order to complete this project you will need an AWS account and a virtual server with Ubuntu Server OS.

If you do not have an AWS account – go back to Project 1 Step 0 to sign in to AWS free tier account and create a new EC2 Instance 
of t2.nano family with **Ubuntu Server 20.04 LTS (HVM) image**. Remember, you can have multiple EC2 instances, but make sure you **STOP** the ones you are not working with at the moment to save available free hours.

Hint #1: When you create your EC2 Instances, you can add Tag "Name" to it with a value that corresponds to a current project you 
are working on – it will be reflected in the name of the EC2 Instance. Like this: E03-MERN

![ec2](https://github.com/santiagosaes/DevOps-Project/blob/main/3%20-%20MERN%20project/images/AWS_EC2_MERN.png) 

Hint #1 (for Windows users only): In previous projects we used Mobaxterm to connect to our EC2 Instances.

![Mobaxterm](https://github.com/santiagosaes/DevOps-Project/blob/main/3%20-%20MERN%20project/images/mobaxterm.png)


# STEP 1 – BACKEND CONFIGURATION
Update ubuntu
```
sudo apt update
```
Upgrade ubuntu
```
sudo apt upgrade
```
Lets get the location of Node.js software from Ubuntu repositories.
```
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
```
**You have to wait the 60 seconds to get a good installation of node.js v18.x.x**
**Another solution is install nvm**

Install Node.js on the server
Install Node.js with the command below

```
sudo apt-get install -y nodejs
```

Note: The command above installs both nodejs and npm. NPM is a package manager for Node like apt for Ubuntu, it is used to install 
Node modules & packages and to manage dependency conflicts.

Verify the node installation with the command below

```
node -v 
```

Verify the node installation with the command below

```
npm -v
```

Application Code Setup
Create a new directory for your To-Do project:

```
mkdir Todo
```

Run the command below to verify that the Todo directory is created with ls command

```
ls
```

TIP: In order to see some more useful information about files and directories, you can use following combination of keys ls -lih – 
it will show you different properties and size in human readable format. You can learn more about different useful keys for ls 
command with ls --help.

Now change your current directory to the newly created one:

```
cd Todo
```

Next, you will use the command npm init to initialise your project, so that a new file named package.json will be created. This
file will normally contain information about your application and the dependencies that it needs to run. Follow the prompts 
after running the command. You can press Enter several times to accept default values, then accept to write out the package.json 
file by typing yes.


```
npm init
```

Run the command ls to confirm that you have package.json file created.

Next, we will Install ExpressJs and create the Routes directory.



