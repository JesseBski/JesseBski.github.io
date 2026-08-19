---
layout: default
title: TryHackMe SOC Level 1 Pathway
---

# Welcome to my TryHackMe SOC 1 Pathway
> This page documents my progress through TryHackMe's SOC Level 1 learning path. Each module below follows this format: What I did, What Tools/Concepts I used, and What I learned.
> Newer modules will be at the bottom of the page.

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


---

### 🔍 SOC Alert Triage & Investigation

**Summary:** This section covers the next stretch of the pathway, including "SOC L1 Alert Triage", "SOC L1 Alert Reporting", "SOC Workbooks and Lookups", "SOC Metrics and Objectives", and "Introduction to Phishing". These rooms moved from theory into the actual day-to-day work of an L1 analyst: picking up and investigating an alert, deciding whether to escalate it, using the right lookups and workbooks to get there faster, measuring how well a SOC team is performing, and finally applying all of it in a real-time simulated phishing scenario.

**What I did:**
- **SOC L1 Alert Triage** - Learned the structure of an alert (time, name, severity, status, verdict, assignee, description, fields) and the SOC platforms that manage them (SIEM like Splunk ES/Elastic, EDR/NDR like MS Defender/CrowdStrike, SOAR, and ITSM tools like Jira/TheHive). Practiced the full triage workflow - filter unclaimed alerts, sort by severity then age, assign to myself, move to "In Progress," investigate using a workbook (or manually if none exists), reach a verdict, and either escalate or close with a comment. Closed out the room by triaging 3 alerts in a simulated SIEM, weighing severity to decide investigation order, and documenting my verdict on each.
- **SOC L1 Alert Reporting** - Covered what happens after triage: reporting, escalation, and communication. Learned to write alert reports using the "5 W's" (who, what, when, where, why), when escalation to L2 is actually warranted (major attack indicators, remediation needs, external communication, or genuine uncertainty), and how to handle real-world SOC communication scenarios - like reaching an unresponsive L2 during a critical alert, or validating a suspected account compromise without using the compromised channel itself.
- **SOC Workbooks and Lookups** - Learned how identity inventory (Active Directory, SSO providers), asset inventory (AD, SIEM/EDR agents, MDM), and network diagrams give an analyst the context needed to judge whether an activity is expected. Walked through a scenario reconstructing a VPN brute-force attack path across subnets using a network diagram, then covered how SOC workbooks (playbooks/runbooks) standardize investigation steps - enrichment, investigation, escalation - so L1 analysts triage consistently instead of freelancing each case.
- **SOC Metrics and Objectives** - Learned the four core SOC metrics (Alerts Count, False Positive Rate, Alert Escalation Rate, Threat Detection Rate) and the SLA-driven triage metrics - MTTD, MTTA, and MTTR - along with target benchmarks for each. Worked through a practice scenario as a SOC manager, matching real complaints (high false positive rate, slow detection, slow acknowledgement, slow response) to the correct improvement action across three separate scenarios.
- **Introduction to Phishing** - My first hands-on run in the SOC Simulator, a real-time environment where alerts popped up live instead of sitting in a static queue. I had to decide on the fly which alert to triage first, then used a URL/IP Checker alongside Splunk logs to check whether the corporate firewall had actually allowed a user to click through to a malicious link in an email. Closed out all True Positive alerts to pass the scenario, and escalated alerts when needed, writing a case report for each.

**Tools/Concepts I Used:**
> Simulated SIEM dashboard, URL/IP Checker, Splunk logs, identity & asset inventory lookups, network diagrams, SOC workbooks, alert reporting (5 W's), SLA benchmarks (MTTD/MTTA/MTTR), real-time SOC Simulator.


**What I Learned:**
- How to prioritize an alert queue correctly - unclaimed alerts first, then by severity, then by age - and why that ordering actually reduces attacker dwell time.
- The full alert lifecycle from assignment through investigation to a documented, defensible verdict.
- Why a well-written alert report saves the next analyst's time and doubles as a long-term record, since alerts are kept indefinitely even after raw logs age out.
- When escalation is actually warranted versus when it's L1's job to close the loop themselves.
- How to use identity inventory, asset inventory, and network diagrams together to answer "is this expected?" instead of guessing.
- Why workbooks exist: they let junior analysts investigate consistently and correctly without needing years of tribal knowledge first.
- The difference between internal health metrics (alert volume, FPR, escalation rate, detection rate) and SLA-facing metrics (MTTD, MTTA, MTTR), and practical fixes for each when they slip.
- How triage changes under real-time pressure - evaluated 4 live alerts with a 5-minute MTTR, landing a 100% True Positive and 100% False Positive identification rate, and how to trace a suspicious email to a concrete yes/no on impact using firewall logs in Splunk.





