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

![image](https://github.com/Nachiketa-A/AWS_Interview_Questions/assets/157089767/ca05a6a5-d1a9-4bc6-8a96-e866ddc90564)

#### 4) Name the Instances types for which the Multi AZ-deployments are available?

**ANS :** The Multi-AZ deployments are available for all the instances irrespective of their types and use.

![image](https://github.com/Nachiketa-A/AWS_Interview_Questions/assets/157089767/e7597f27-9125-418c-8e7b-bb58c36b49a7)

#### 5) Which instance can we use for deploying a 4-node cluster of Hadoop in AWS?

**ANS :** We can use i2.large or c4.8x large instance for deploying a 4-node cluster of Hadoop in AWS. However, c4.8x large instances are preferred for master machines, i2.large instances are preferred for slave machines and c.4bx needs a better configuration on the PC.

#### 6) What do you know about an AMI?

**ANS :** AMI is a template that provides information required to launch an instance or virtual machine. It is possible to select pre-built AMI’s that AMI commonly have in them while creating an instance. Also, a user can have customized AMI for the most common reason of saving space on AWS.

![image](https://github.com/Nachiketa-A/AWS_Interview_Questions/assets/157089767/ba9524be-2a43-4a1f-b1c3-42b7de93b525)

#### 7) Can we run multiple websites on the EC2 server with one Elastic IP address?

**ANS :** We need more than one elastic IP to run multiple websites on the EC2 server, so it’s not possible.

#### 8) Mention the states available in Processor State Control?

**ANS :** It contains two states:

P-state: It has different levels starting from P0 to P15.
C-State: Its levels are from C0 to C6, where C6 is the strongest state for the processor.

#### 9) What is the use of making the subnets?

**ANS :** To efficiently utilize networks that have given a large number of hosts. You can assume that many networks come with a large number of hosts. For easy access, the network is divided into subnets. This will help in managing the hosts and getting them into a more straightforward form.

#### 10) Can you use the Amazon cloud front in directing the transfer objects?

**ANS :** Yes, the Amazon CloudFront helps you in supporting through the origins of the custom. It may also include the origin that comes from outside of AWS.


![image](https://github.com/Nachiketa-A/AWS_Interview_Questions/assets/157089767/afdcc36d-ea75-4f2c-bdf1-02ff6af83005)

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





