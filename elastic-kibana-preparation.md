# Elastic/Kibana Threat Hunting Preparation

## Scope

This document describes my Elastic/Kibana preparation before a cyber defence exercise.

Important clarification:

My final hands-on exercise work focused mainly on SIFT/REMnux-based forensic and artifact analysis. I did not mainly perform Elastic/Kibana investigation during the final hands-on work.

However, Elastic/Kibana preparation helped me understand SOC workflows, log-driven investigations and threat hunting thinking.

---

## What I Practiced

Before the exercise, I practiced basic Elastic/Kibana workflows such as:

- Searching events
- Filtering data
- Adjusting time ranges
- Selecting useful fields
- Reviewing host-related activity
- Reviewing user-related activity
- Reviewing process-related activity
- Reviewing network-related activity
- Structuring threat hunting questions
- Writing investigation notes

---

## Fields I Practiced Thinking About

I practiced thinking about fields such as:

- `@timestamp`
- `host.name`
- `user.name`
- `process.name`
- `process.command_line`
- `process.parent.name`
- `source.ip`
- `destination.ip`
- `event.action`
- `event.dataset`
- `event.category`
- `event.type`

These fields are useful because they help connect activity to time, users, hosts, processes and network communication.

---

## Hunting Questions I Practiced

I practiced forming questions such as:

- Are there unusual authentication attempts?
- Are there repeated failed logins?
- Is there a successful login after repeated failures?
- Are there suspicious process executions?
- Are there unusual command lines?
- Are there suspicious parent-child process relationships?
- Are there connections between internal hosts?
- Are there signs of lateral movement?
- Are there suspicious external destinations?
- Are there signs of data transfer?
- Are timestamps consistent across data sources?
- What happened before and after a suspicious event?

---

## Investigation Thinking

A useful investigation workflow I practiced was:

1. Define the question.
2. Select the relevant dataset.
3. Set the correct time range.
4. Identify useful fields.
5. Search and filter events.
6. Compare normal and suspicious activity.
7. Document observations.
8. Separate confirmed findings from assumptions.
9. Write next steps.

---

## How This Helped My Actual Work

Even though my final hands-on work did not focus on Elastic/Kibana, this preparation helped me understand:

- How SOC analysts think with logs
- Why time ranges matter
- Why field names matter
- How endpoint, authentication and network events can support incident response
- How to turn a broad question into a focused search
- Why findings must be documented clearly

This preparation supported my overall DFIR and incident response understanding.

---

## Next Steps

I want to continue improving in:

- KQL queries
- ECS field understanding
- Timeline building in Kibana
- Process execution analysis
- Authentication log analysis
- Lateral movement detection
- Endpoint and network event correlation
- Writing better hunting notes