---
title: "How to connect an EC2 instance from Windows"
datePublished: Sun Jul 21 2024 09:36:46 GMT+0000 (Coordinated Universal Time)
cuid: clyvd5vt9000a09jnfuo0hlii
slug: how-to-connect-an-ec2-instance-from-windows
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1721554470763/0c307374-cf50-4fe5-bb00-e53870895a36.png
tags: ec2, ssh, mobaxterm

---

Today let's understand how to access an EC2 instance from your Windows computer, After you create an EC2 instance (if you don't know how to create an EC2 instance please [**click here**](https://devprojects.hashnode.dev/project-3-creating-first-ec2-instance-on-aws) for step by step guide and once you are done creating an EC2 instance come back here )

now you will need the IP address of the instance and the key you downloaded when creating the instance to connect to your EC2 instance from **MobaXterm** using SSH  
  
now open **MobaXterm if you have not downloaded MobaXterm** click here and [download it &gt;&gt;](https://mobaxterm.mobatek.net/download-home-edition.html) and after you install it Open **MobaXterm** and follow the steps below

Now Open Mobaxterm and click on **Session**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721553737138/c02418c1-6f58-4bbe-b4f1-ba321b7cfd98.png align="center")

Select SSH

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721553774968/0f2ffbbc-198a-4d97-9a91-afdbcd6524fa.png align="center")

Now you will need the Remote host (IP address of your instance )and the .pem file your private key to connect to your instance

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721553830941/a56d0061-6d81-4a6d-b5b3-7d9a90dcca6a.png align="center")

how do you get them?  
go back to your Instance on AWS click on your instance, and copy the IP address as shown below

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721553973260/7a471854-95c6-412b-8e9c-9152a40298c8.png align="center")

Go back to **MobaXterm** enter the IP address on the Remote host

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721554062395/c8ab7720-bc7f-40dd-84e0-811ac33f5e4a.png align="center")

Give any under the name , and now it is time to upload the private key, you remember when you create an instance you create a new private key, and a .pem file gets downloaded that will be the key/file you will be uploading in place of use the private key and then click on OK

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721554203808/90934577-57df-4c9e-b928-12d892f5b397.png align="center")

it will ask a pop-up to accept it click on Accept

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721554267893/8093e57f-5f19-4421-a15b-6fa97557d66d.png align="center")

Perfect now you are connected to your EC2 instance from your windows using **MobaXterm**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721554343069/919d35dd-5e3b-47c1-a0d6-cf4b949976e7.png align="center")

If you come across any errors, please comment on them so we can troubleshoot them together.