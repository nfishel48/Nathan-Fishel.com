---
title: "5 Reasons You Need to be using Infrastructure as code"
date: 2022-10-23T21:37:07-04:00
draft: true
tags:
- Terraform
- IaC
- DevOps
- Cloud
type: post
---

![alt text](/images/servers.jpg "Image of servers in a data center")

## So what is Infrastructure as code anyway?
Infrastructure as code(aka IaC) is a way of managing your infrastructure through code instead of clicking through your cloud providers web console. With IaC you no longer need to manually provision infrastructure, instead this process can be automated.

## #1 Avoid and Revert ad-hoc changes
When it comes to your infrastructure consistency is key. When defining your infrastructure with code you can take the human varible out of the equation. With small environments it is easy enough to provision infrastructure from memory but once you start having testing, develoment, and staging versions mistakes will be made. With IaC you can deploy consistient infrastructure accross multiple environments and never need to worry about inconsitenys. But what happens when the new intern accidentlly deletes your mission critial lambda function? Using a IaC tool like terraform a simple `terraform apply` will check the state of your resources notice the missing function and deploy it and verfiy its configured correctly.

## #2 Reason Two

## #3 Reason Three

## #4 Reason Four

## #5 Reason Five
