# Cybersecurity Learning Portfolio – DFIR, Artifact Analysis and Lab Infrastructure

## Overview

This repository contains a sanitized cybersecurity learning portfolio based on my work in a cyber defence exercise environment and related preparation work.

The portfolio focuses on practical blue team learning, especially:

- DFIR and artifact analysis
- Disk image / VMDK analysis with SIFT
- Phishing artifact analysis with REMnux
- Mobile / source code analysis
- Proxmox-based lab preparation
- Local AI-assisted analysis environment support
- Technical documentation and reusable playbooks
- Elastic/Kibana preparation before the exercise

This public version does not include confidential exercise material, real internal IP addresses, hostnames, domains, indicators of compromise, credentials, screenshots with sensitive data, organization-specific information or exact exercise solutions.

The goal is to show what I practiced, what I built, how I approached the work, and what I learned.

---

## My Actual Role

My final hands-on work during the exercise focused mainly on forensic and artifact analysis using SIFT and REMnux.

My main practical work included:

- Inspecting VMDK / disk image evidence with a SIFT-style forensic workflow
- Analyzing phishing-related artifacts with REMnux
- Reviewing mobile/source-code related artifacts statically
- Documenting observations, findings, assumptions and next steps
- Supporting the wider lab environment and technical documentation

I also prepared and practiced other areas before the exercise, including Elastic/Kibana log analysis and SOC/threat hunting workflows. However, my final hands-on exercise work did not mainly focus on Elastic/Kibana.

---

## Main Hands-on Work

### VMDK / Disk Image Analysis with SIFT

I used a SIFT-style forensic workstation to inspect disk image evidence in a controlled way.

The work included:

- Identifying disk image structure and partitions
- Working from a controlled analysis environment
- Mounting or preparing evidence for inspection in a safe way
- Reviewing file system contents
- Checking user directories and common artifact locations
- Looking for recently modified files, suspicious scripts, binaries or unusual filenames
- Reviewing logs and timestamps where available
- Documenting commands, observations and open questions
- Separating confirmed observations from assumptions

This helped me understand how disk image analysis requires careful evidence handling, repeatable workflow, documentation and timeline-oriented thinking.

---

### Phishing Artifact Analysis with REMnux

I used a REMnux-style environment to analyze phishing-related artifacts safely.

The work included:

- Inspecting suspicious text-based artifacts, email-related files and web-related content
- Checking file types and metadata
- Extracting URLs, domains, filenames, hashes and suspicious strings
- Looking for encoded or obfuscated content
- Decoding content where appropriate
- Reviewing possible redirection logic
- Avoiding execution of unknown content
- Documenting possible indicators and follow-up actions

Tools and techniques included Linux command-line utilities such as file identification, hashing, strings, grep/ripgrep-style searching, text inspection and CyberChef-style decoding.

This helped me understand the importance of safe static analysis, indicator validation and clear documentation.

---

### Mobile / Source Code Analysis

I also performed static review of mobile/source-code related artifacts.

The work included checking for:

- Application permissions
- Manifest or configuration files
- API endpoints
- External URLs
- Hardcoded values
- Possible secrets or tokens
- Suspicious functions
- Network communication logic
- Obfuscation indicators
- Data collection or exfiltration-related logic

I treated source code observations as leads that required validation, not as final conclusions by themselves.

This helped me understand how code review can support incident analysis, especially when combined with other evidence sources.

---

## Lab and Infrastructure Work

In addition to analysis work, I supported the preparation of a Proxmox-based cybersecurity lab environment.

This included:

- Preparing analysis virtual machines
- Working with SIFT, REMnux and FLARE-style environments
- Creating and configuring users for analysis systems
- Supporting repeatable access workflows
- Using VM templates and snapshots
- Considering isolation and firewall rules
- Preparing systems so analysts could work in a safer and more repeatable way

This part taught me that infrastructure preparation is part of cybersecurity work. A good lab environment makes analysis safer, faster and easier to repeat.

---

## Local AI / Qwen Environment Support

I supported the preparation of a local AI-assisted analysis environment based on a local LLM setup.

The purpose of the local AI environment was to support internal analysis workflows where public AI tools were not suitable for confidential material.

The local environment could support:

- Malware and reverse-engineering workflows
- Static analysis support
- Command ideas
- Documentation support
- Analysis checklist creation
- Explaining code or tool output

I did not mainly use the local AI environment in my own final analysis work, but the environment supported other malware-analysis related work.

The key lesson was that AI can support analysis and documentation, but it must not replace manual validation or analyst judgment.

---

## AI Usage and Boundaries

Cloud-based AI tools were used before the exercise for preparation and learning support.

This included:

- Learning support
- Command examples
- Grep/search ideas
- Simple Python helper script ideas
- Documentation structure
- Playbook drafting
- Checklist preparation

During the exercise, public AI services were not used for confidential exercise material.

All AI-generated suggestions were treated as untrusted assistance. Commands, scripts, findings and conclusions were manually reviewed and validated.

---

## Elastic/Kibana Preparation

Before the exercise, I practiced Elastic/Kibana-based log analysis and threat hunting workflows.

This included:

- Basic searching and filtering
- Time range handling
- Thinking about relevant fields
- Practicing SOC-style investigation questions
- Reviewing host, user, process and network event fields
- Documenting findings and next steps

Important clarification: my final hands-on exercise work focused mainly on SIFT/REMnux-based forensic and artifact analysis, not Elastic/Kibana investigation.

Elastic/Kibana practice still helped me understand how log analysis supports incident response and threat hunting.

---

## Documentation Work

Documentation was a major part of my work.

I created and practiced:

- Investigation notes
- DFIR workflows
- Artifact analysis templates
- Phishing analysis checklists
- Disk image analysis notes
- Mobile/source-code analysis checklists
- IOC documentation structures
- SOC/threat hunting playbooks
- Public vs private documentation boundaries

This helped me understand that documentation is not separate from technical cybersecurity work. Good documentation makes analysis easier to validate, continue and report.

---

## Skills Demonstrated

This portfolio demonstrates practical learning in:

- Digital forensics basics
- Disk image triage
- VMDK analysis workflow
- Phishing artifact analysis
- Static source-code review
- Linux command-line investigation
- Safe handling of suspicious files
- REMnux and SIFT workflows
- Proxmox lab preparation
- VM templates and snapshots
- Secure analysis environment design
- Local LLM / AI-assisted workflow support
- Technical documentation
- SOC/DFIR process understanding

---

## Lessons Learned

Key lessons:

- Evidence handling and documentation are critical.
- Public writeups must be sanitized.
- Findings, assumptions and next steps must be separated.
- Static analysis is useful, but conclusions require validation.
- Lab preparation makes analysis safer and faster.
- Elastic/Kibana is an important area for continued SOC practice.
- AI can support learning, commands and documentation, but it must not be treated as final evidence.
- It is important to be honest about what was actually done and what was only prepared or practiced.

---

## Next Steps

Areas I want to improve next:

- More practical Elastic/Kibana hunting
- Better KQL skills
- Deeper forensic timeline analysis
- More structured phishing analysis
- Mobile/APK analysis
- Static malware analysis with REMnux
- Ghidra and reverse-engineering basics
- Better English technical reporting
- More sanitized portfolio writeups