---
title: "Fix windows system slow ness"
datePublished: Mon Apr 28 2025 15:00:27 GMT+0000 (Coordinated Universal Time)
cuid: cma17ginx001g09kw8zm90zdj
slug: fix-windows-system-slow-ness
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1745852366544/676844b2-b328-46a6-a03c-0f4a0ba10c25.jpeg
tags: windows-11, system-slow

---

1) Check if there is any Hard disk issues

CMD&gt; wmic diskdrive get status  
if status shows “ OK” then there is no issue with your hard disk

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1745851702720/09fbd6f6-017d-48ce-af0e-d862b0b21c4a.png align="center")

2) Stop background tasks  
Windows + R  
Type : taskschd.msc  
This will open up task scheduler  
Expand task scheduler library → Microsoft → windows  
click on application experience  
Right click on “ Microsoft compatible Appraiser” and Disable it

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1745852056917/599099e3-0690-44ac-adf0-3901eae02e47.png align="center")

next :On the left look for customer experience improvement program  
Right click → consolidator and disable it

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1745852163483/0a5b23a5-1e29-4c9d-b89a-19bfb5166687.png align="center")

Next : scroll down to power efficiency Diagnostics  
and Disable any thing on the right  
  
Now close all and restart computer windows will not secretly waste any recourses speeding up your computer !