# Lab Infrastructure and Local AI Environment

## Scope

This document describes my lab infrastructure and local AI environment work in a sanitized way.

The main areas were:

- Proxmox-based lab preparation
- SIFT, REMnux and FLARE-style analysis machines
- User creation and access workflows
- Snapshots and VM templates
- Secure analysis environment thinking
- Local Qwen-based AI / LLM environment support

No internal IP addresses, credentials, hostnames, exact firewall rules or confidential configuration values are included.

---

## Proxmox Lab Preparation

I supported the preparation of a Proxmox-based cybersecurity lab environment for analysis and exercise use.

This included:

- Preparing virtual machines for analysis workflows
- Supporting repeatable VM deployment
- Using snapshots before risky changes
- Working with VM templates
- Preparing analysis systems for multiple users
- Considering how analysts would access systems
- Documenting setup and usage steps

This helped me understand that reliable infrastructure is a requirement for effective cybersecurity analysis.

---

## Analysis VM Preparation

### SIFT

SIFT was prepared and used for forensic-style workflows.

Its purpose included:

- Disk image analysis
- File system inspection
- Timeline-oriented analysis
- Log and artifact review
- Evidence handling

I used SIFT especially for VMDK / disk image analysis.

---

### REMnux

REMnux was prepared and used for suspicious artifact analysis.

Its purpose included:

- Phishing artifact analysis
- Malware-adjacent static analysis
- URL and string extraction
- Decoding
- Suspicious file inspection
- Command-line analysis workflows

I used REMnux especially for phishing and artifact analysis.

---

### FLARE-style Windows Analysis VM

A FLARE-style Windows analysis machine was also part of the wider lab environment.

Its purpose was to support Windows malware analysis and reverse-engineering workflows where needed.

Important safety considerations included:

- Keeping the VM controlled
- Using snapshots
- Restricting unnecessary exposure
- Handling suspicious files carefully
- Avoiding accidental execution outside an analysis workflow
- Learning how to disavle windows defender

---

## User Creation and Access Workflows

I practiced creating and preparing user access for analysis machines.

This included thinking about:

- Which user should perform analysis tasks
- When administrative privileges are required
- How to keep normal analysis separate from system administration
- How to document access instructions
- How to make the environment usable for others

This helped me understand the operational side of lab preparation.

---

## Snapshots and Templates

Snapshots and templates were important parts of the workflow.

They supported:

- Returning systems to a clean state
- Repeating analysis setup
- Reducing setup time
- Recovering from mistakes
- Preparing multiple similar analysis machines
- Making the environment more reliable during exercise work

This taught me that snapshots and templates are not only convenience features. They are part of safe analysis operations.

---

## Secure Analysis Environment Thinking

During lab preparation, I practiced thinking about isolation and access control.

Important principles included:

- Do not expose analysis systems unnecessarily.
- Restrict remote access to trusted networks where possible.
- Use firewall rules and access control.
- Keep suspicious artifacts in controlled systems.
- Use snapshots before risky analysis steps.
- Avoid mixing clean systems and suspicious content.
- Document what each VM is intended for.
- Decide when a machine should or should not have internet access.

This was especially important for malware-adjacent work.

---

## Local AI / Qwen Environment

I supported the preparation of a local AI-assisted analysis environment based on a local Qwen-style LLM setup.

The purpose of the local AI environment was to provide AI assistance inside an approved environment when public AI tools were not appropriate for confidential material.

The local AI environment could support:

- Malware analysis assistance
- Reverse-engineering support
- Static analysis explanations
- Command ideas
- Documentation help
- Investigation checklist creation
- Explaining suspicious code patterns
- Summarizing tool output for manual review

I did not mainly use this local AI environment in my own final analysis work, but the environment supported other malware-analysis related work.

---

## Local AI Safety Principles

The local AI environment was treated as an assistant, not as an authority.

Important principles:

- AI output must be validated manually.
- AI-generated commands must be checked before running.
- AI-generated explanations must be compared with real evidence.
- AI should not be treated as final proof.
- Sensitive data should not be sent to public AI services.
- Local AI can reduce confidentiality risk, but it does not remove the need for human review.

---

## Public AI Usage Boundary

Before the exercise, I used cloud-based AI tools for preparation and learning support.

This included:

- Understanding concepts
- Drafting documentation structures
- Generating command ideas
- Creating grep/search ideas
- Drafting simple Python helper script ideas
- Preparing checklists and playbooks

During the exercise, public AI services were not used for confidential exercise material. AI support during the exercise was limited to the approved local LLM environment where applicable.

---

## Lessons Learned

This infrastructure work taught me that:

- A good lab environment improves analysis quality.
- VM preparation is part of cybersecurity work.
- Templates and snapshots reduce risk.
- Access control and network isolation matter.
- Local AI can be useful in restricted environments.
- AI must be validated manually.
- Documentation makes the environment usable for others.