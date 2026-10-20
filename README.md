# Cybersecurity Learning Portfolio

**Blue Team / DFIR · Linux · Security Labs · Hardware Security**

## About this portfolio

I'm an ICT student focusing on data networks and cybersecurity. My main interest is on the defensive side: understanding what happened, finding the evidence and being able to explain the result. I also enjoy building the lab environments needed to investigate things properly.

This repository is where I document some of that hands-on work. It includes an independent USB-C dock investigation and a sanitized overview of my work in a cyber defence exercise environment. These are separate projects, and I try to make that distinction clear.

I'm not presenting every tool I've tried as an area of expertise. The idea is to show **what I actually did, how I approached it, what I found and what remained unanswered**.

## Projects

### DELTACO USBC-DOCK2 – USB-C Dock Security Analysis (October 2026)

I bought a sealed 11-in-1 USB-C dock through a normal retail channel and wanted to understand what it actually does when connected to a computer. A dock may look like one device, but Linux can see several USB devices and interfaces behind it. I wanted to find out which ones were expected and whether anything unusual appeared.

I started with Ubuntu 26.04.1 Live on my ASUS Zenbook, kept the first tests offline and compared the system before and after connecting the dock. I then tested its features one at a time. For Ethernet, I used a separate Ubuntu laptop (Lenovo ThinkPad X230) and captured traffic from both ends of an isolated connection.

**What I checked:**

- USB topology, device classes, VID/PID identifiers and Linux drivers
- Storage/card reader, HID and audio interfaces, and display functionality
- Ethernet link, ARP, ICMP traffic, packet captures and interface error counters
- Evidence collection and SHA256 integrity checks

The Ethernet link negotiated at **1000 Mbit/s full duplex**. Bidirectional ICMP tests worked without packet loss, and the packet captures contained traffic consistent with the tests and host services. I did not observe behavior indicating malicious activity in the features I tested.

That is **not** the same as proving the dock is secure. USB-C Power Delivery was not tested, and I did not carry out firmware reverse engineering.

**[Read the project write-up](projects/deltaco-usbc-dock2/README.md)**  
[Technical DFIR report (Finnish)](projects/deltaco-usbc-dock2/docs/technical-report-fi.md) · [Step-by-step investigation guide (Finnish)](projects/deltaco-usbc-dock2/docs/investigation-guide-fi.md)

### Cyber Defence Exercise – Forensics and Artifact Analysis

My main hands-on work in the exercise was **forensic and artifact analysis**, particularly with SIFT and REMnux. I also supported the lab environment and prepared other Blue Team workflows beforehand.

I have kept the public documentation sanitized. It describes methods and learning outcomes without exposing exercise-specific evidence or internal details.

#### Disk image / VMDK analysis with SIFT

I worked through disk image structure and file system evidence in a controlled analysis environment. The practical work included identifying partitions, inspecting directories and likely artifact locations, checking logs and timestamps, and looking for files or scripts worth investigating further.

A recurring part of the process was keeping observations separate from assumptions. Finding an unusual file is a starting point, not automatically a conclusion.

#### Phishing-related artifact analysis with REMnux

I inspected suspicious text, email-related and web-related artifacts without executing unknown content. I used basic Linux tools and decoding techniques to examine file types, metadata, URLs, domains, hashes, strings and possible obfuscation or redirect logic.

The focus was on collecting leads, checking their context and documenting what could actually be supported by the available evidence.

#### Mobile / source code review

I also performed static inspection of mobile- and source-code-related artifacts. I looked at permissions, manifests, configuration, endpoints, embedded values, possible secrets, suspicious functions and signs of data collection or network communication.

The code review was part of triage. I did not treat a suspicious-looking function by itself as proof of malicious activity.

## Lab and Infrastructure Work

I helped prepare a Proxmox-based analysis environment alongside the forensic work. My tasks included preparing analysis VMs, working with SIFT/REMnux/FLARE-style environments, user configuration, templates, snapshots and access workflows. Network isolation and firewalling were also part of the planning.

This matters to me because the quality of the analysis depends partly on the environment. A lab should be safe to use, predictable and easy to reset or reproduce.

### Local AI / Qwen environment

I supported work on a local LLM-based analysis environment intended for internal use where public AI services were not appropriate for confidential material. Its potential uses included static-analysis support, explaining tool output, command suggestions and documentation.

I did **not** use the local AI setup as the main tool in my own final exercise analysis. It was supporting infrastructure, not a substitute for verifying findings.

### Elastic / Kibana preparation

Before the exercise, I practiced searching and filtering log data, working with time ranges and thinking through SOC-style investigation questions involving hosts, users, processes and network activity.

This was preparation. My main hands-on exercise work was with SIFT and REMnux, rather than an Elastic/Kibana investigation.

## How I Work

My usual approach is fairly simple:

1. Define what I'm trying to find out and what could go wrong.
2. Establish a baseline before changing or connecting anything.
3. Collect the observations and keep the original evidence where possible.
4. Compare the results, test plausible explanations and document the limitations.

I try to distinguish between **facts**, **assessments** and **unknowns**. If I cannot verify something, I would rather leave it open than turn an assumption into a finding.

Technical documentation is part of the work for me, not something I add only at the end. I maintain investigation notes, reusable checklists and playbooks so that I can revisit a case or repeat the process later.

## AI Use and Information Handling

I have used AI tools to support studying, understand tool output, plan checks and improve documentation. I still review commands and validate technical conclusions against actual evidence.

Public AI services were not used for confidential exercise material during the exercise. This repository intentionally excludes confidential exercise content, internal addresses and hostnames, credentials, sensitive screenshots and exact exercise solutions. Raw research evidence is not published here by default.

## What I'm Working On Next

My next learning priorities include more hands-on Elastic/Kibana investigations and KQL, forensic timeline analysis, phishing and malware triage with REMnux, mobile/APK analysis, and Ghidra/reverse-engineering fundamentals.

I also want to keep improving my technical reporting in English and publish more projects where the testing process and the limits of the conclusions are visible.
