# Project MERN

![MERN stack](https://github.com/santiagosaes/DevOps-Project/blob/main/3%20-%20MERN%20project/images/mernstack.png)


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
In order to complete this project you will need an AWS account and a virtual server with Ubuntu Server OS.

If you do not have an AWS account – go back to Project 1 Step 0 to sign in to AWS free tier account and create a new EC2 Instance 
of t2.nano family with Ubuntu Server 20.04 LTS (HVM) image. Remember, you can have multiple EC2 instances, but make sure you STOP 
the ones you are not working with at the moment to save available free hours.

Hint #1: When you create your EC2 Instances, you can add Tag "Name" to it with a value that corresponds to a current project you 
are working on – it will be reflected in the name of the EC2 Instance. Like this: E03-MERN

![Logo MERN](3 - MERN project/images/AWS_EC2_MERN.png)   


