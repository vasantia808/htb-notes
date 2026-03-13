# Section 05: Gathering System Information

**Module:** 07 - Introduction to Windows Command Line  
**Heading:** CMD  
**Date:** 2026-03-12

---

## Summary

This section covers host enumeration goals and techniques.

---

## Key Concepts

I learned how to get basic system, network, domain, and user info using CMD.exe. 

---

## Commands

```cmd
systeminfo
# Obtain information about the host, OS, versions, etc.
```
```cmd
hostname
# Display name of the host
```
```cmd
ver
# Display version
```
```cmd
ipconfig /all
# Provides detailed network configuration information
```
```cmd
whoami /all
# Obtain information about the current user's security privileges on the system and groups.
```
```cmd
net user
# Add, remove, or manage user accounts
```
```cmd
net group
# Manage global groups on a domain controller
```
```cmd
net localgroup
# Manage local user groups on a computer
```
```cmd
net share
# Display information about shared resources and create new shared resources on your local machine
```
```cmd
net view
# Display information about shared resources on other computers on the network
```
---

## What I Found Interesting or Challenging

I found out that using these commands can create noise that blue teams/admins will eventually notice since most average users 
do not use CMD.exe. If you are an admin or on a blue team, it is important that when you notice this type of activity, you should
investigate quickly.

---

*Last updated: 2026-03-12*
