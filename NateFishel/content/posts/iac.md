---
title: "5 Reasons You Need to be using Infrastructure as code"
date: 2022-10-23T21:37:07-04:00
draft: false
tags:
- Terraform
- IaC
- DevOps
- Cloud
type: post
---

![alt text](/images/servers.jpg "Image of servers in a data center")

## So what is Infrastructure as code anyway?
Infrastructure as code(aka IaC) is a way of managing your infrastructure through code instead of clicking through your cloud provider's web console. With IaC you no longer need to manually provision infrastructure, instead, this process can be automated.

## #1 Avoid and Revert ad-hoc changes
When it comes to your infrastructure consistency is key. When defining your infrastructure with code you can take the human variable out of the equation. With small environments, it is easy enough to provision infrastructure from memory but once you start having testing, development, and staging versions mistakes will be made.

## #2 Speed
Since you can view all your current infrastructure as code in a file when changes are required, you need to update this file and deploy it. When combined with a CI/CD system deploys can become frictionless and speed increase exponentially.

## #3 Testing
With IaC you can run your code through unit tests you can see what changes will be made to your infrastructure before you deploy. This prevents unnecessary downtime through faulty configurations getting pushed to production.

## #4 Reusability
Once Infrastructure modules have been created they can be reused and redeployed as many times as needed. This means those huge time savings when you need to create new environments or launch subsequent applications that will have similar infrastructure needs.

## #5 Cost optimizations
When using infrastructure as code you can apply best practices for cost and make sure everything is tracked in a state file. This is even more powerful when you combine this with a drift detection tool. You can always be sure that you are getting the most for your money in this way.
