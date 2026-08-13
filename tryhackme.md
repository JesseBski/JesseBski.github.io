---
layout: default
title: TryHackMe SOC Level 1 Pathway
---

# Welcome to my TryHackMe SOC 1 Pathway
> This page documents my progress through TryHackMe's SOC Level 1 learning path. Each module below follows the same format as my main projects section: What I did, What Tools/Concepts I used, and What I learned.

---

[← Back to Home](index.md)

--- 


### 📘 Blue Team Introduction

**Summary:** This covers the first stretch of the pathway, including "Junior Security Analyst Intro", "SOC Role in Blue Team", "Humans as Attack Vectors", and "Systems as Attack Vectors". These rooms covered the fundamentals before any alert triage: who's actually on a SOC team, how that team fits into a larger security organization, and the two broad categories of things a SOC defends - humans and systems. Each room was paired with concepts, and a short simulated scenario to apply them.

**What I did:** 
- **Junior Security Analyst Intro** - Learned the core SOC team roles, like Senior Analyst, SOC Engineer, SOC Manager, and Incident Responder, and what a day-to-day workload looks like. After reviewing SOC roles and daily tasks, I completed a simulated task where I inspected a SIEM dashboard, copying malicious IP's from a critical alert, and escalating the ticket to a senior analyst.
- **SOC Role in Blue Team** - Mapped where SOC sits inside a company's broader security structure and how Blue Teams (defense) relate to Red Teams (offense) and GRC (compliance). Here I broke down SOC's internal tiers (L1/L2/Engineers/Manager), the Cyber Incident Response Team (CIRT), and specialized roles like Threat Intel and AppSec. I then finished a final challenge acting as a CISO of a simulated company, assigning the right responder to seven simultaneous incidents.
- **Humans as Attack Vectors** - Studied why humans are the most targeted part of an attack surface and how social engineering works by exploiting trust and emotion rather than technical flaws. Humans can easily fail to detect phishing, malware downloads, and deepfake impersonation. At the end of this room, I practiced a simulation as a SOC analyst, where I opened a security dashboard and reviewed an "Employees at Risk" panel, and updated a company's Security Policy tab.
- **Systems as Attack Vectors** - Covered how systems get breached - human-led entry points like weak passwords, inserting malicious USB drives, unpatched vulnerabilities (Zero-Day and CVE/Patch cycle), supply chain compromise, and misconfigurations. I practiced triaging a "Systems at Risk" panel and chose the correct fixes from a Remediation Plan tab in a simulated dashboard.

**Tools/Concepts I Used:**
> Simulated SIEM dashboard, Simulated Security Dashboard, Simulated Remediation Console.

**What I Learned:**
- The SOC team structure and escalation path - where an L1 analyst's job stops and a Senior Analyst's begins.
- How SOC fits into a company's overall security org, alongside Red Team and GRC, under a CISO.
- The difference between an internal SOC and an MSSP, and the range of specialized Blue Team roles beyond SOC (CIRT, Digital Forensics, Threat Intel, AppSec).
- Why humans are the most exploited part of an attack surface, and the difference between mitigating an attack and detecting one.
- How systems get compromised beyond a single hacker - weak configuration and supply chain risks are just as common as direct exploits.
- The standard response pattern to a disclosed vulnerability: patch when available, restrict access and apply vendor mitigations while you wait.
