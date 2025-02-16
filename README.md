# AWS-Project-SQS-Nodejs-Backend
Overview

This project demonstrates how to integrate AWS Simple Queue Service (SQS) with a Node.js backend. The application allows messages to be sent from a web interface to an SQS queue and retrieved for display. It utilizes AWS EC2, SQS, IAM roles, security groups, and basic web technologies (JavaScript, HTML, and EJS).

Architecture & Components

AWS SQS: Queue service for message storage and retrieval.

AWS EC2: Compute instance hosting the Node.js application.

IAM Role: Grants EC2 permission to interact with SQS.

Security Group: Allows traffic on port 3000.

Node.js & Express: Backend server handling API requests.

HTML & EJS: Frontend for user interaction.

Setup Guide

Step A: Create an SQS Queue

Log in to AWS Console.

Navigate to Amazon SQS.

Create a new queue (either Standard or FIFO based on your needs).

Note the Queue URL for later use.

Step B: Configure EC2 & IAM Role

Create a Security Group:

Allow inbound traffic on port 3000.

Launch an EC2 Instance:

Use Amazon Linux as the OS.

Attach the previously created security group.

Attach an IAM role with permissions to access SQS.

Install Node.js on EC2:

curl -sL https://rpm.nodesource.com/setup_16.x | sudo bash -

sudo yum install -y nodejs

node -v

npm -v # Verify installation

Initialize Node.js Project:

npm init -y npm install express aws-sdk body-parser ejs

Step 1: Create app.js

Create a new file app.js and add the app.js content:

Step 2: Create Frontend Files index.html and add index.html content

also create send.html and add send.html content

also create messages.ejs and add messages.ejs content

Step C: Run the Application

Ensure your EC2 instance has the appropriate IAM role for SQS access.

Start the server:

node app.js

Access the web interface via:http://<EC2_PUBLIC_IP>:3000

Use the Send Message page to add messages to the queue.

Use the View Messages page to fetch messages from the queue.

See below secrrenshots

![image](https://github.com/user-attachments/assets/0d77a50b-36b1-43cc-bbae-52bdb0a1b37f)

![image](https://github.com/user-attachments/assets/b927565c-573c-4f4a-8288-6a58ec57c213)

![image](https://github.com/user-attachments/assets/c6fd256a-3a3a-4a53-a52a-a7afbc3a9a7a)





