---
layout: post
title: AWS Pros & Cons
date:   2015-01-27 15:10:08
categories: reference
---
Have used [AWS](aws.amazon.com) quite a bit over last year sometimes get asked "should I ... AWS" questions. Here's a list of first things that come to my mind regarding AWS (and maybe cloud services generally). 


*Things to consider:*

- Main claimed benefit of aws is its flexibility - you can roll out new servers as you need (for temporary resource needs or just testing new setups) and take them down as well
	- I have moved mysql server to high-memory node for half a day just to run some one-time heavy ops (like adding a column to table with billions of rows) 
- It is easy to start your system on cheapest server(s) and upgrade it gradually when more resources are needed
- [AWS Free tier](http://aws.amazon.com/free/) allows to set up minimal version of the service with no costs
- Available APIs that allow to automate virtually all the operations over AWS systems 
	- I have set up a proxy system, that launches and uses new micro instance when new IP address is needed
- Lots of documentation cover most use cases
- Price at cloud provider tends to be higher than for equal dedicated server
- Reserved instances can cut down your costs considerably - This requires upfront payment and min a year commitment
- Check and optimise data flow - this can cause unexpected cost increases
- Incoming bandwidth is free (at EC2)
- Set up billing monitor to get early warning when anything is eating up budget
- On AWS storage services (S3, DynamoDB, RDS, ..) costs tend to go up with high read/write volumes, so don't miss these
	- In most cases it came cheaper to set up own database on EC2 instance as monthly IOPS was >100M
- Use [AWS calculator](http://calculator.s3.amazonaws.com/index.html) to plan costs
- Global network (of AWS regions) allows to set up servers close to your users and launch very redundant setups