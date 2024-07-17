---
title: "Create your first EC2 instance!"
datePublished: Wed Jul 17 2024 10:16:42 GMT+0000 (Coordinated Universal Time)
cuid: clypotu9v001e09ljch6j1i9d
slug: create-your-first-ec2-instance
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1721197662190/9134e19c-b9fa-479f-afa2-2806ef6434de.png
tags: ec2, aws, iaas, virtual-machines, ebs, elasticcomputecloud, infrastructureasaservice, instances, elasticblockstore, elasticloadbalancing

---

**<mark>Quick Overview!</mark>**  
EC2 is one of the most popular AWS offerings. EC2 stands for Elastic Compute Cloud, and it provides Infrastructure as a Service (IaaS). With EC2, you can:

* Run virtual machines, called instances.
    
* Store data on virtual drives, known as EBS.
    
* Distribute loads across machines using ELB.
    
* Scale services with Auto-Scaling Groups (ASG).
    

Understanding EC2 is crucial for learning how the cloud works. When you rent an EC2 instance, you can configure the following:

1. **Operating System (OS)**: Choose between Linux or Windows (Mac is not available).
    
2. **Compute Power and Cores (CPU)**: Select the number of CPUs.
    
3. **RAM**: Decide how much memory you need.
    
4. **Storage Space**:
    
    * **Network Attached**: EBS & EFS.
        
    * **Hardware Attached**: EC2 instance store.
        
5. **Network Card**: Specify the speed and public address.
    
6. **Firewall Rules**: Set up security groups.
    
7. **Bootstrap Script**: Configure the instance at first launch.
    

For practice, we will use the t2.micro instance type because it's free.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721198433405/9907503c-99e6-47fe-8fc9-fa0d5f09af98.png align="center")

Let's start to create your first EC2 instance : &gt;  
EC2 instance is nothing but a virtual machine,  
**<mark>There are 7 simple steps to follow</mark>**

* **Choose AMI**: Select an Amazon Machine Image.
    
* **Choose Instance Type**: Pick the instance type.
    
* **Configure Instance**: Set up the instance settings
    
* **Add Storage**: Specify the storage requirements.
    
* **Add Tags**: Add tags for identification.
    
* **Configure Security Group**: Set up security rules.
    
* **Review**: Review all the settings before launching.
    
    **1.** After you log in go to Homepage -&gt; top left click on Services -&gt; Click on EC2, if you don't find it click on All services and locate EC2
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721198806951/e99a2470-60ac-45d1-a4de-45e9d4a491f1.png align="center")

When the page loads click on the launch instance as shown below

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721198950907/c7e80c20-0138-4b76-b675-ebfeae584de6.png align="center")

Give a name to your instance

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721199268704/aa8561aa-ea17-473f-a92c-c3dc8fb613be.png align="center")

Select Application and OS Images (Amazon Machine Image)  
this is nothing but choosing an operating system  
Select Redhat and Select Red Hat Enterprise Linux 9 which is (free tire eligible) as shown below

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721199434419/c3b32fcb-d2d2-4c8e-bd61-ecbb76c07b27.png align="center")

Select instances as t2.micro

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721199662282/8aec4063-27ea-49e3-97a4-e76abd1d1f2c.png align="center")

Select the key pair ( this step is important )  
click on Create a new pair, to know what a is keypair [click here&gt;&gt;](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html?icmpid=docs_ec2_console)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721200130268/94140b19-ecee-460a-ac5d-1f5d1a0a41d9.png align="center")

Now enter the key pair name, Select RSA, and Private key format as .pem  
and then click on Create key pair

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721200360827/49cfe92a-b0a8-4e91-b374-dbb8854105b8.png align="center")

Under Network settings  
Select Create security group, and select SSH traffic from \[anywhere\] for this example which is unsafe but for this example, we will select this

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721200558243/6b8625fa-a84c-4b07-9f03-9b7c00bfddea.png align="center")

You can also select an existing Security group that you have created for additional security but for now, let's select anywhere

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721200690932/69d1252e-8627-4a6d-b2a1-fa3a9db5882d.png align="center")

Scroll down and click on launch instance

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721200813569/fa6a86af-695d-4861-bb94-cb58a9a33959.png align="center")

One instance is created

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721200872395/ea757a1d-5c13-4ebd-9dd2-01af94e666ea.png align="center")

Scroll down and click on View all instances

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721206783175/f17514db-bbd2-4315-b15d-5e1b6493bd96.png align="center")

Now select the instance you have created and click on connect

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721206872432/11eacfd8-bdc8-4ac6-a666-ff13c983cc7e.png align="center")

Now go to Ec2 instance connect, and click on Connect  

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721209662499/a95ee729-1fbf-4efd-9cbe-14fa2cee550d.png align="center")

You may encounter an error as below.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721209728087/56b8aec6-1c1a-454b-b8ab-6eab89e2e0f0.png align="center")

This is due to the failure to set the SSH inbound rule  
`How to fix: error Failed to connect to your instance   Error establishing SSH connection to your instance. Try again later.`  
  
Failure to set the SSH inbound rule refers to not properly configuring the security group rules for an EC2 instance to allow SSH (Secure Shell) access. This rule is crucial because it determines who can remotely connect to your instance over the internet.

### What Happens When SSH Inbound Rule is Not Set

1. **No Remote Access**: Without the SSH inbound rule, you cannot remotely connect to your EC2 instance using SSH. This means you can't perform any management or configuration tasks on the instance.
    
2. **Access Denied Errors**: Any attempt to SSH into the instance will result in connection errors, typically "Connection timed out" or "Connection refused."
    
3. **Operational Delays**: Inability to access the instance can delay deployment, maintenance, and troubleshooting processes, affecting productivity and operations.
    

### How to Properly Set the SSH Inbound Rule

1. **Open Security Groups in the AWS Console**: Go to the EC2 dashboard, find the "Security Groups" section, and select the security group associated with your instance.
    
2. **Add Inbound Rule**:
    
    * **Type**: Select "SSH."
        
    * **Protocol**: This will automatically be set to TCP.
        
    * **Port Range**: This will automatically be set to 22.
        
    * **Source**: Specify the IP address range that is allowed to connect. For instance:
        
        * `0.0.0.0/0` allows SSH access from any IP address (not recommended for security reasons).
            
        * A specific IP address or range (e.g., `192.168.1.0/24`) restricts access to only those addresses.
            
3. **Save the Rule**: Click "Save" or "Apply" to update the security group.
    

### Example: Allow SSH from a Specific IP

1. **Type**: SSH
    
2. **Protocol**: TCP
    
3. **Port Range**: 22
    
4. **Source**: `203.0.113.0/24` (replace with your IP range)
    

By setting this rule, you ensure that only the specified IP addresses can SSH into your instance, enhancing both accessibility and security.  
  
**<mark>Let me show you step by step:</mark>**  
Go to instances and go to security as shown below

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721210025515/5f90db4f-827e-4124-bfe3-9c773707990d.png align="center")

Under security click on security group

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721210082961/c28901a9-8d10-46bd-89a2-1e0a90ebf45a.png align="center")

Then click on edit inbound rules

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721210134021/5ebc4f13-82ee-444b-88c1-506f77f46cde.png align="center")

Then select Add rules

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721210199204/4920497e-3c21-4f91-8618-5ac6eaf7464f.png align="center")

Then select SSH , source Select Anywhere -Ipv4 and click on save rule

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721210334277/b6e3b524-94bc-4df3-8d70-207cd3da19b9.png align="center")

Now to connect to the server from our command prompt  
Open the command prompt to see where the .pem file is stored for me its downloaded in the Downloads folder go to the download folder  
`cd:\users\Dev>cd downloads`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721210731685/b1412683-2452-49f4-9527-c4d92d7f0df3.png align="center")

Now under the connect instance go to the SSH client

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721210790156/4ce44af3-e39d-4537-9718-1add3f8ed6a8.png align="center")

Copy the public DNS paste it into the command prompt and hit enter

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721210962161/7493ff03-3839-4191-96c5-ad0ee9010891.png align="center")

You have successfully connected to the instance (server)  
to know the Name of the OS, version,  
type `$more /etc/os-release`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721211124356/72fdb8db-589b-460d-8228-e7cebffbe031.png align="center")

Hope you learned something new ticket, follow my page for more such existing learning journeys!