# Network Scanning Guide for Beginners — Learn Nmap Like a SOC Analyst

A practical, no-fluff guide to network scanning with Nmap — built from real home lab sessions, not theory.

When I started learning cybersecurity, most tutorials either skipped the basics or made network scanning sound more complicated than it needed to be. This guide walks through the fundamentals the way a working SOC analyst actually uses them.

## What's inside

- Discover live hosts on a network using Nmap
- Identify open ports and running services
- Understand and interpret Nmap scan results
- Learn from practical home lab examples
- Explore MITRE ATT&CK reconnaissance techniques
- Full Nmap command cheat sheet for quick reference

## Sample: Host Discovery

```bash
# Discover live hosts on a /24 subnet
nmap -sn 192.168.1.0/24

# Output
Nmap scan report for 192.168.1.1
Host is up (0.00041s latency).
Nmap scan report for 192.168.1.13
Host is up (0.00038s latency).
```

**Why this matters (hacker's perspective):** before you can attack or defend a network, you need to know what's actually on it. Host discovery is reconnaissance step one — and it maps directly to MITRE ATT&CK's [T1018 — Remote System Discovery](https://attack.mitre.org/techniques/T1018/).

## Sample: Service & Version Detection

```bash
nmap -sV 192.168.1.13

PORT     STATE SERVICE VERSION
22/tcp   open  ssh     OpenSSH 8.9p1
80/tcp   open  http    Apache httpd 2.4.52
3306/tcp open  mysql   MySQL 8.0.32
```

Knowing exact service versions lets you cross-reference against known CVEs — this is how real vulnerability assessments start.

## Get the full guide

The full guide covers 7 essential Nmap scan types, complete walkthroughs with real lab results, defensive countermeasures for each technique, and a complete command cheat sheet you can keep using as a reference.

**[📖 Get it on Amazon — $7.00](https://www.amazon.com/dp/B0H6Y5225K)**

---

### About the author

Written by **Henry Uwaezuoke** — Lagos-based IT technician transitioning into cybersecurity, focused on SOC analysis and penetration testing. See more of my work: [bihghefty.github.io/cyberportfolio](https://bihghefty.github.io/cyberportfolio)
