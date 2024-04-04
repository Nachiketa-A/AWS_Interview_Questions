# AWS_Interview_Questions

#### 1) What is the difference between stopping and terminating an instance?

**ANS :** When an Ec2 instance is stopped, a normal shutdown is performed on the instance.
          When an EC2 instance is terminated, it gets transferred to a stopped state, and then the attached EBS volumes are permanently deleted.

<img width="478" alt="image" src="https://github.com/Nachiketa-A/AWS_Interview_Questions/assets/157089767/e87af726-a6d6-45e5-8cdc-391c5f5c1742">

#### 2) When there is a need to acquire costs with an EIP?

**ANS :** When EIP is associated and allocated with a stopped instance, there is a need to acquire costs. You will not be charged if only one Elastic IP is present with the instance you are running. But, if the IP doesn’t attach to any instance or is attached to a stopped instance, you need to pay for it.

<img width="308" alt="image" src="https://github.com/Nachiketa-A/AWS_Interview_Questions/assets/157089767/4331667f-050b-4b0a-98dc-ee85ed1c00dc">


#### 3) Differentiate between an On-demand instance and a Spot Instance.

**ANS :** Spot Instances are unused computing capacity blocks released by AWS when EC2 instances are created.
On-Demand Instances are virtual servers in the AWS EC2 used while testing and developing applications on EC2.


#### 4) Name the Instances types for which the Multi AZ-deployments are available?

**ANS :** The Multi-AZ deployments are available for all the instances irrespective of their types and use.


#### 5) Which instance can we use for deploying a 4-node cluster of Hadoop in AWS?

**ANS :** We can use i2.large or c4.8x large instance for deploying a 4-node cluster of Hadoop in AWS. However, c4.8x large instances are preferred for master machines, i2.large instances are preferred for slave machines and c.4bx needs a better configuration on the PC.

#### 6) What do you know about an AMI?

**ANS :** An AMI is like a blueprint for setting up a virtual machine or instance in a cloud environment, like AWS. You can choose from ready-made AMIs that come with standard configurations when creating your instance. Or, you can create your own customized AMI, which is handy for saving storage space on AWS.

![image](https://github.com/Nachiketa-A/AWS_Interview_Questions/assets/157089767/ba9524be-2a43-4a1f-b1c3-42b7de93b525)

#### 7) Can we run multiple websites on the EC2 server with one Elastic IP address?

**ANS :** We need more than one elastic IP to run multiple websites on the EC2 server, so it’s not possible.

#### 8) Mention the states available in Processor State Control?

**ANS :** It contains two states:

P-state: It has different levels starting from P0 to P15.
C-State: Its levels are from C0 to C6, where C6 is the strongest state for the processor.

#### 9) What is the use of making the subnets?

**ANS :** When you have lots of devices connected to a network, it can get messy. So, to organize things better, we split the network into smaller parts called subnets. Each subnet contains a manageable number of devices, making it easier to control and access them. This helps keep everything neat and tidy.

#### 10) Can you use the Amazon cloud front in directing the transfer objects?

**ANS :** Yes, the Amazon CloudFront helps you in supporting through the origins of the custom. It may also include the origin that comes from outside of AWS.


#### 11) Can we speed up data transfer in Snowball? How?

**ANS :** Yes, some specific methods for speeding up Snowball are:

By simply copying from different hosts to the same Snowball.
By creating a group of smaller files. This is helpful as it cuts down the encryption issues.

#### 12) How to establish a connection between the Amazon cloud and a corporate data centre?

**ANS :** A VPN (Virtual Private Network) needs to be established between the Virtual private cloud and the organization’s network. Then, the connection can be created, and data can be accessed reliably.        

#### 13) Is it possible to change or modify the private IP address of an EC2 instance while running?

**ANS :** No, the private IP address of an EC2 instance can not be changed while running, as the private IP will remain with the instance permanently or through the life cycle.

#### 14) Is it possible to run multiple databases on Amazon RDS free of cost?

**ANS :** Yes, as per RDS prices, there is an upper limit of 750 hours that on exceeding will be charged. The charge is made only on the extra hours beyond 750.

#### 15) If you hold half of the workload on the public cloud whereas the other half is on local storage, what type of architecture is used in such a case?

**ANS :** The hybrid cloud architecture is used in such a case.

#### 16) What is a Hypervisor?

**ANS :** A Hypervisor is a type of software used to create and run virtual machines. It integrates physical hardware resources into a platform which are distributed virtually to each user.

![image](https://github.com/Nachiketa-A/AWS_Interview_Questions/assets/157089767/8a08d4a8-06b7-4dda-9e47-42e2a9e6dd03)

#### 17) I have some private servers on-premises. Also, I have distributed my workloads on the public cloud. What is this architecture called in this case?

**ANS :** It is a hybrid cloud architecture as we are using both the public cloud and on-premises servers, i.e. the private cloud.

![image](https://github.com/Nachiketa-A/AWS_Interview_Questions/assets/157089767/c0322a62-e1c9-4ec3-82c7-04fa3b2ebfb4)

#### 18) What does the following command do for the Amazon EC2 security groups?

**ANS :** ‘ec2-create-group CreateSecurityGroup’

A. Creates a new group inside the security group.

B. Creates a new security group for use with your account.

C. Creates a new rule inside the security group.

D. Groups the user-created security groups into a new group for easy access.

Answer: B – A Security group acts as a firewall and controls the traffic in and out of your instance. The above command will create a security group, and on creation, the user can add different rules to it. Suppose, if you want to access an RDS instance, you have to add the public IP address of the machine by which you want to access the instance in its security group.

#### 19) Which value do we need to set the instance’s tenancy attribute to if we want the instance to run on single-tenant hardware?

**ANS :** A. Isolated

B. Dedicated

C. One

D. Reserved

Answer: B – The Instance tenancy attribute should be set to Dedicated Instance. The rest of the values are invalid.

#### 20) In case AWS Direct Connect fails, will it result in connectivity loss?

**ANS :** If a backup of AWS Direct Connect has been configured, it will switch over to the second one in the event of a failure. It is recommended to enable Bidirectional Forwarding Detection (BFD) when configuring your connections to ensure faster detection and failover. On the other hand, if you have configured a backup IPsec VPN connection instead, all VPC traffic will automatically failover to the backup VPN connection. Traffic to/from public resources such as Amazon S3 will be routed over the Internet.

![image](https://github.com/Nachiketa-A/AWS_Interview_Questions/assets/157089767/c89b5bf5-c24d-486d-864c-d978e94c3f03)

#### 21) Can you explain the difference between Amazon S3 and EBS?

**ANS :** Amazon S3 is a simple storage service that offers industry-leading scalability, data availability, security, and performance. It can be used to store and retrieve any amount of data, at any time, from anywhere on the web. Amazon EBS, on the other hand, is a block storage service that provides persistent storage for Amazon EC2 instances. EBS allows you to create storage volumes and attach them to EC2 instances, and supports both magnetic and solid-state drive (SSD) volumes.

#### 22) How do you handle data archiving in AWS?

**ANS :** One way to handle data archiving in AWS is to use Amazon S3 Glacier, which is a secure, durable, and extremely low-cost Amazon S3 storage class for data archiving and long-term backup. With S3 Glacier, you can store data at a cost that is as little as 1/10th of one cent per gigabyte per month.

#### 23) What is the purpose of Amazon CloudFront?

**ANS :** Amazon CloudFront is a content delivery network (CDN) that securely delivers data, videos, applications, and APIs to customers globally. It integrates with other Amazon Web Services products to give developers and businesses an easy way to distribute content to end users with low latency, high data transfer speeds, and no minimum usage commitments.

#### 24) Can you explain how Amazon Elastic Block Store (EBS) works?

**ANS :** Amazon EBS provides raw block-level storage of data that can be attached to a running Amazon EC2 instance. Each EBS volume is automatically replicated within its Availability Zone to protect data from the failure of a single drive. EBS volumes can be used as the primary storage for data that requires frequent and granular updates, such as file systems or databases.

#### 25) How do you secure an Amazon S3 bucket?

**ANS :** To secure an Amazon S3 bucket, you can use a combination of the following measures:
Access control
Encryption
Versioning
Access logging

#### 26) Can you explain the difference between Amazon EC2 and Amazon Elastic Beanstalk?

**ANS :** Amazon EC2 is a web service that provides resizable compute capacity in the cloud, while Amazon Elastic Beanstalk is an easy-to-use service for deploying, running, and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, and Docker.

#### 27) Can you explain the purpose of Amazon Elastic Container Service (ECS)?

**ANS :** Amazon Elastic Container Service (ECS) is a fully managed container orchestration service that makes it easy to run, scale, and secure containerized applications on AWS. It allows you to easily run and scale containerized applications using Docker and Amazon Elastic Container Registry (ECR) images.

#### 28) How do you automate the scaling of Amazon EC2 instances?

**ANS :** To automate the scaling of Amazon EC2 instances, you can use Amazon Auto Scaling. This service allows you to automatically increase or decrease the number of instances in your Auto Scaling group based on predefined policies and metrics.

#### 29) Can you explain the purpose of the Amazon Elastic File System (EFS)?

**ANS :** Amazon Elastic File System (EFS) is a fully managed, scalable, and elastic file storage service for use with Amazon EC2 instances. EFS is designed to provide a simple and highly available file storage service, with a high degree of scalability and performance.

#### 30) How do you handle disaster recovery in AWS?

**ANS:** To handle disaster recovery in AWS, you can use a combination of services such as Amazon S3, Amazon RDS, Amazon DynamoDB, and Amazon Elastic Block Store (EBS) snapshots. You can use these services to create backups and replicas of your data and resources.

#### 31) Can you explain the difference between Amazon RDS and DynamoDB?

**ANS:** Amazon RDS is a fully managed relational database service that makes it easy to set up, operate, and scale a relational database in the cloud. It supports a variety of database engines, including MySQL, PostgreSQL, Oracle, and SQL Server.
On the other hand, Amazon DynamoDB is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability

#### 32) How do you handle backups in AWS?

**ANS:** To handle backups in AWS, you can use a combination of services such as Amazon S3, Amazon RDS, Amazon DynamoDB, and Amazon Elastic Block Store (EBS) snapshots. These services allow you to create backups and replicas of your data and resources, and then use these backups to recover your applications and data in the event of a failure.

#### 33) Can you explain the purpose of Amazon Elastic MapReduce (EMR)?

**ANS:** Amazon Elastic MapReduce (EMR) is a fully managed service that makes it easy to process large amounts of data using the popular Apache Hadoop and Apache Spark frameworks.

#### 34) How do you monitor resources and applications in AWS?

**ANS:** To monitor resources and applications in AWS, you can use a combination of services such as Amazon CloudWatch, AWS CloudTrail, and Amazon CloudWatch Logs. These services allow you to collect and monitor various metrics and logs related to your resources and applications.

#### 35)Can you explain the purpose of Amazon Simple Queue Service (SQS)?

**ANS :** Amazon Simple Queue Service (SQS) is a fully managed message queuing service that makes it easy to decouple and scale microservices, distributed systems, and serverless applications. SQS allows you to send,

#### 36)How do you handle security in AWS?

**ANS:** To handle security in AWS, you can use a combination of services such as Amazon Identity and Access Management (IAM), Amazon Virtual Private Cloud (VPC), and AWS Key Management Service (KMS).

#### 37) Can you explain the purpose of Amazon Simple Notification Service (SNS)?

**ANS:** Amazon Simple Notification Service (SNS) is a fully managed messaging service that makes it easy to send and receive messages between applications and services. SNS allows you to send messages to multiple subscribers at once, including via email, SMS, and other protocols.

#### 38)How do you handle compliance in AWS?

**ANS:** To handle compliance in AWS, you can use a combination of services such as AWS Config and AWS Control Tower. These services allow you to monitor and evaluate your resources against a set of predefined policies and guidelines and provide you with the tools and resources you need to meet compliance requirements such as HIPAA, SOC 2, and PCI DSS.

#### 39) Can you explain the purpose of Amazon Simple Email Service (SES)?

**ANS:** Amazon Simple Email Service (SES) is a fully managed email service that allows you to send and receive emails at scale. With SES, you can send emails to your customers, subscribers, and other contacts using a simple and reliable API, or through the AWS Management Console.

#### 40)How do you handle data migration in AWS?

**ANS:** To handle data migration in AWS, you can use a combination of services such as AWS DataSync, AWS Database Migration Service (DMS), and AWS Snowball. These services allow you to easily transfer data between on-premises and cloud environments, and to migrate data between different databases and storage services. Additionally, you can use services such as AWS Direct Connect and Amazon S3 Transfer Acceleration to optimize the transfer of large amounts of data.

#### 41) Can you explain the purpose of Amazon Elasticsearch Service?

**ANS:** Amazon Elasticsearch Service is a fully managed service that makes it easy to deploy, operate, and scale Elasticsearch clusters in the AWS cloud. It allows you to index, search, and analyze large volumes of data quickly and in near real time.

#### 42)How do you handle network traffic in AWS?

**ANS:** To handle network traffic in AWS, you can use a combination of services such as Amazon Virtual Private Cloud (VPC), Amazon Elastic Load Balancing (ELB), and Amazon Route 53. These services allow you to securely and efficiently route and manage network traffic within your AWS environment.

#### 43)Can you explain the purpose of the Amazon Elastic Transcoder?

**ANS:** Amazon Elastic Transcoder is a fully managed service that makes it easy to create and convert video files into multiple formats. It allows you to convert existing video files into different resolutions and bit rates, so that they can be played on a variety of devices, such as smartphones, tablets, and smart TVs.

#### 44)How do you handle cost optimization in AWS?

**ANS:** To handle cost optimization in AWS, you can use a combination of services such as AWS Cost Explorer, AWS Trusted Advisor, and AWS Budgets. These services allow you to monitor and control your costs, identify opportunities for cost savings, and set budgets for your resources.

#### 45)Can you explain the purpose of Amazon Kinesis?

**ANS:** Amazon Kinesis is a fully managed service that makes it easy to collect, process, and analyze real-time streaming data. It allows you to easily ingest and process data streams, such as log files, sensor data, and social media feeds, and then analyze and visualize the data using services such as Amazon Redshift, Amazon Elasticsearch Service, and Amazon QuickSight.

#### 46)How do you handle multi-region deployments in AWS?

**ANS:** To handle multi-region deployments in AWS, you can use a combination of services such as Amazon Route 53, Amazon CloudFront, and Amazon Elastic Block Store (EBS). These services allow you to route traffic to the optimal region, distribute content globally, and replicate data across multiple regions for high availability and disaster recovery.

#### 47)Can you explain the purpose of Amazon AppStream?

**ANS:** Amazon AppStream is a fully managed service that allows you to stream desktop applications from the cloud to any device. It allows you to easily run your existing applications on a variety of devices, such as laptops, tablets, and smartphones, without the need to re-architect your applications or make changes to the underlying infrastructure.

#### 48)How do you handle integration with on-premises infrastructure in AWS?

**ANS:** To handle integration with on-premises infrastructure in AWS, you can use a combination of services such as AWS Direct Connect, AWS VPN, and AWS Storage Gateway. These services allow you to create dedicated connections between your on-premises infrastructure and your AWS environment, and to easily transfer data and resources between the two environments.

#### 49) Can you explain the purpose of Amazon WorkSpaces?

**ANS:** Amazon WorkSpaces is a fully managed, secure desktop computing service that runs on the AWS cloud. It allows you to easily provision cloud-based virtual desktops to your users and provides them with access to their applications and data from any device.

#### 50)How do you handle data encryption in AWS?

**ANS:** To handle data encryption in AWS, you can use a combination of services such as AWS Key Management Service (KMS), Amazon Elastic Block Store (EBS) encryption, and Amazon S3 encryption. These services allow you to encrypt your data at rest and in transit, and to manage and control access to your encryption keys.
