# VPC INTERFACE ENDPOINT LAB
This Repository is used to explain VPC Interface Endpoint Lab using (IaaC) Terraform.

An interface endpoint is a type of VPC endpoint that enables communication between instances in an Amazon VPC and services over AWS PrivateLink, allowing secure access to services without imposing availability risks or bandwidth constraints on network traffic.For each subnet that you specify from your VPC, we create an endpoint network interface in the subnet and assign it a private IP address from the subnet address range. An endpoint network interface is a requester-managed network interface.

# PREREQUISITE

1. Create a VPC
2. Create Public and Private subnet
3. Launch EC2 Instances in both Subnet
4. Create Interface Endpoint for SQS in Private subnet
5. Create IAM Role For SQS and attached to Private Instance
6. Login to bastion Host (EC2 Instance)
7. SSH into private EC2 and access SQS (PutMessage) using interface endpoint.

   Create VPC:
<img width="954" alt="2025-02-10 (79)" src="https://github.com/user-attachments/assets/e6b378a4-5a9b-41b2-a859-29fb9a5b29bb" />

Create Public and Private Subnet:
<img width="960" alt="2025-02-10 (55)" src="https://github.com/user-attachments/assets/77286e66-464d-407d-98b9-247a9b86ce87" />

Launch EC2 instance in both Subnet:

<img width="960" alt="2025-02-10 (52)" src="https://github.com/user-attachments/assets/68fc6986-f636-4508-81d9-b89a9092d6ac" />

Create Interface Endpoint:

<img width="960" alt="2025-02-10 (53)" src="https://github.com/user-attachments/assets/9849f33a-0a42-4a77-a0cf-6a5048c7112f" />

Create IAM Role for SQS and attached to EC2 Server (Private):

<img width="960" alt="2025-02-10 (49)" src="https://github.com/user-attachments/assets/06802401-f09c-4521-a6a5-bd4b741d2017" />

<img width="960" alt="2025-02-10 (51)" src="https://github.com/user-attachments/assets/7d6f2c9a-6d58-4055-9ed0-7621e082f411" />

Login to EC2 server (Bastion Host) save your private key, give it chmod 400 permissions and ssh into the private EC2 Instance:

<img width="960" alt="2025-02-10 (61)" src="https://github.com/user-attachments/assets/1ffbc5c1-0efc-4295-a25f-fbf7e227f1a4" />

Access SQS (PutMessage) using interface endpoint:

<img width="960" alt="2025-02-10 (43)" src="https://github.com/user-attachments/assets/453ac944-4b55-4f21-9f90-4c42bef834c1" />

Goto SQS QUeue click on send and receive messages:

<img width="960" alt="2025-02-10 (45)" src="https://github.com/user-attachments/assets/5251bcfe-0cc8-445c-9377-9771fc719659" />

Click on pull Messages:

<img width="960" alt="2025-02-10 (46)" src="https://github.com/user-attachments/assets/8f09a976-6b7a-48ea-8a89-b0b8cadf9c48" />

Click the Message ID to show the body of the message:

<img width="960" alt="2025-02-10 (47)" src="https://github.com/user-attachments/assets/0ba4a010-28d5-463c-96a0-1bddeeaa7cab" />

<img width="960" alt="2025-02-10 (48)" src="https://github.com/user-attachments/assets/8eb5caf3-5e8e-4ac2-8879-252588b2cec7" />





















   
