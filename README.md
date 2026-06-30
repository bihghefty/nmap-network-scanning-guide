# Network Scanning Guide for Beginners — Learn Nmap Like a SOC Analyst

Network scanning is one of the first skills every cybersecurity professional should learn.

Whether you're interested in becoming a SOC analyst, penetration tester, or network defender, knowing how to discover hosts, identify services, and understand what devices are exposing on a network is essential.

This guide is based on hands-on practice in my home lab and explains Nmap the way I wish it had been explained when I was starting out—simple, practical, and focused on real-world use.

## What's Inside

- Discover live hosts on a network using Nmap
- Identify open ports and running services
- Learn how to read and understand Nmap results
- Real examples from a home lab
- MITRE ATT&CK mappings for reconnaissance techniques
- A printable Nmap command cheat sheet

---

## Example: Host Discovery

```bash
# Discover live hosts on a /24 subnet
nmap -sn 192.168.1.0/24

# Output
Nmap scan report for 192.168.1.1
Host is up (0.00041s latency).

Nmap scan report for 192.168.1.13
Host is up (0.00038s latency).
```

One of the first questions during a security assessment is, "What devices are actually on this network?"

A simple host discovery scan helps answer that question. Before you can secure or assess a network, you need to know what systems are available. This technique aligns with **MITRE ATT&CK T1018 – Remote System Discovery**.

---

## Example: Service & Version Detection

```bash
nmap -sV 192.168.1.13

PORT     STATE SERVICE VERSION
22/tcp   open  ssh     OpenSSH 8.9p1
80/tcp   open  http    Apache httpd 2.4.52
3306/tcp open  mysql   MySQL 8.0.32
```

Finding open ports is only part of the job.

Knowing the exact software and version running on a system allows security professionals to investigate known vulnerabilities, verify configurations, and prioritize potential risks.

---

## Why I Wrote This Book

When I started learning Nmap, I found plenty of tutorials explaining the commands, but very few explained why those commands mattered in real cybersecurity work.

I wrote this guide to bridge that gap. Instead of memorizing commands, you'll learn when to use them, what the results mean, and how they fit into real-world reconnaissance and defensive security.

---

## Get the Full Guide

The complete guide includes:

- Host discovery
- Port scanning
- Service and version detection
- Operating system detection
- Common Nmap scan types
- Practical home lab walkthroughs
- Defensive security tips
- MITRE ATT&CK mappings
- A printable Nmap cheat sheet

📚 **Available on Amazon**

**Amazon Author Page:**  
https://amazon.com/author/henryuwaezuoke

---

## About the Author

Hi, I'm **Henry Uwaezuoke**.

I'm a cybersecurity educator, SOC analyst, penetration tester, and IT professional with a passion for helping beginners build practical cybersecurity skills.

I enjoy turning complex technical concepts into simple, hands-on lessons that people can immediately apply in their own labs. My goal is to help aspiring cybersecurity professionals build confidence through practice rather than theory alone.

---

## Connect with Me

🌐 **Cybersecurity Portfolio**  
https://bihghefty.github.io/cyberportfolio

📚 **Amazon Author Page**  
https://amazon.com/author/henryuwaezuoke
