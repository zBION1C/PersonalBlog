---
layout: post
title:  "Active directory explained simple"
date:   2024-03-16 23:12:48 +0100
categories: windows
---

I stumbled upon the active directory concept multiple times, without understanding intuitively what it does, why it is used and how what are it's implications in the cybersecurity context. Every time i searched "What is active directory?" on google all i got was a very high level explanation of the concept, without a technical grasp on it. Well now that i gathered some information on it i will try to explain it in an intuitive way with use case scenarios.

## Local authentication vs Central authentication
Let's start by defining what is the difference between **local authentication** and **remote authentication**.

**Local authentication** is the most familiar to all of us. When you startup your personal computer you are required to input a username and a password to authenticate and use the computer. When you give this information to the computer, it will check in a *local* database the credentials and if it finds a match it will grant you access to the computer. To understand more this concept let's make an example. Suppose you loose your computer (let's hope not), and you buy a new one. If you input the credential of the stolen computer it will not grant you access to it, because the credential database was local to the stolen computer!
Simple, intuitive and functional.

Now suppose that you are a system admin for the company *hooli.com* which has 100 computers spread across the entire building in different floors. Your boss ask you to configure the accounts and passwords of all the computers of *hooli*. In a universe where only local authentication exists you have to configure manually every computer by accessing it physically (or remotely, but it's still a lot of work). I will start to faint at the 25th computer configured! Fortunately we exists in a universe where **central authentication** was invented. Central authentication permits us to configure accounts in one centralized database. Now when an employee wants to authenticate it will send his credential to this database and if the check is positive he will be authenticated. This type of authentication has a lot of benefits:
- Accounts are not bound to computers. A HR employee that usually use a computer in the HR floor of *hooli* can use a computer in another floor logging in with his/her account. All the permissions of the users are fetched from the central database.
- Authentication is performed in a centralized manner, so the life of a system administrator is a lot easier.
- It permits share of file and network resources (expand)

## Active directory
Active directory is an implementation of the mentioned **central authentication**.