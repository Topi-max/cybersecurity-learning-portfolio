# DFIR and Artifact Analysis Practice

## Scope

This document describes my practical DFIR and artifact analysis work in a sanitized way.

The main areas were:

- Disk image / VMDK analysis
- Phishing artifact analysis
- Mobile / source code analysis
- Safe artifact handling
- Technical documentation

No confidential exercise data, real indicators, internal infrastructure details or exact exercise solutions are included.

---

## Disk Image / VMDK Analysis

### Goal

The goal of disk image analysis was to inspect a system image safely and identify relevant artifacts that could support an investigation.

I focused on understanding:

- What the disk contained
- Which partitions and file systems were present
- Which user and system locations were relevant
- Whether there were suspicious files, scripts or timestamps
- What should be documented for follow-up analysis

---

### Environment

I used a SIFT-style forensic environment for this work.

SIFT was useful because it provides a Linux-based environment designed for forensic workflows such as disk inspection, file system analysis, timeline thinking and evidence handling.

---

### Practical Workflow

My workflow followed this structure:

1. Identify the evidence type.
2. Work in a controlled analysis environment.
3. Avoid modifying original evidence.
4. Inspect disk layout and partitions.
5. Mount or access the file system safely.
6. Review relevant file system locations.
7. Search for suspicious files, scripts, logs and timestamps.
8. Record commands and observations.
9. Separate confirmed findings from assumptions.
10. Write next steps for further analysis.

---

### Examples of Locations and Artifacts Reviewed

Depending on the image contents, I reviewed or considered areas such as:

- User home directories
- Desktop, Downloads and Documents folders
- Temporary directories
- Recently modified files
- System log locations
- Application log locations
- Startup or persistence-related locations
- Browser-related artifacts
- Suspicious scripts
- Unknown binaries
- Archive files
- Configuration files
- Files with unusual names or extensions

---

### Command-line Techniques Practiced

I practiced using command-line techniques such as:

- File type identification
- Hash calculation
- Directory listing and sorting
- Searching file names
- Searching file contents
- Extracting strings
- Checking timestamps
- Reviewing logs with text tools
- Recording commands and results in notes

Example tool categories included:

- `file`-style file identification
- `sha256sum`-style hashing
- `find`-style file searching
- `grep`/`ripgrep`-style content searching
- `strings`-style string extraction
- timeline-oriented review where applicable

The exact evidence names and findings are not included in this public version.

---

### Documentation Approach

For disk image analysis, I documented:

- What was checked
- Which tools or commands were used
- Which files or paths looked relevant
- Which timestamps were important
- What was confirmed
- What was only a hypothesis
- What should be investigated next

This helped me practice forensic note-taking and evidence-based reporting.

---

### Lessons Learned

Disk image analysis taught me that:

- A controlled workflow is more important than random searching.
- Original evidence should be protected.
- Timestamps need context.
- Suspicious files need validation.
- Good notes are essential.
- Forensic analysis requires patience and structure.

---

## Phishing Artifact Analysis

### Goal

The goal of phishing artifact analysis was to inspect suspicious material safely and extract useful indicators without executing unknown content.

---

### Environment

I used a REMnux-style environment for phishing and suspicious artifact analysis.

REMnux was useful because it supports malware-adjacent and artifact-focused workflows with many command-line analysis tools.

---

### Practical Workflow

My phishing analysis workflow was:

1. Identify the artifact type.
2. Calculate hashes if needed.
3. Inspect content statically.
4. Extract visible strings.
5. Search for URLs, domains and suspicious patterns.
6. Decode encoded content when appropriate.
7. Review attachments or embedded references.
8. Document possible indicators.
9. Validate findings before treating them as final.
10. Write follow-up questions and next steps.

---

### Things I Looked For

I looked for:

- Sender and header anomalies
- URLs
- Domains
- IP addresses
- Suspicious filenames
- Attachment names
- File hashes
- Encoded strings
- Base64-like content
- Obfuscated JavaScript or HTML
- Redirection logic
- Credential harvesting indicators
- External resource loading
- Suspicious keywords or commands

---

### Techniques Practiced

I practiced techniques such as:

- Static file inspection
- String extraction
- Grep/ripgrep-style searching
- URL extraction
- Hashing
- Decoding encoded content
- Defanging indicators for documentation
- Separating indicators from conclusions

I did not execute unknown phishing artifacts directly.

---

### Documentation Approach

For phishing artifacts, I documented:

- Artifact type
- Hashes where relevant
- Extracted indicators
- Where the indicator was found
- Context around the indicator
- Confidence level
- Open questions
- Recommended next steps

---

### Lessons Learned

Phishing analysis taught me that:

- Static analysis can reveal a lot without execution.
- Extracted indicators must be validated.
- Encoded content should be handled carefully.
- Context matters.
- It is important to document where each indicator came from.
- Public writeups must avoid exposing real exercise indicators.

---

## Mobile / Source Code Analysis

### Goal

The goal of mobile/source-code analysis was to inspect source code and configuration artifacts for security-relevant behavior.

---

### Practical Workflow

My source-code review workflow was:

1. Identify the project or artifact structure.
2. Locate configuration and manifest files.
3. Review permissions.
4. Search for URLs and endpoints.
5. Search for hardcoded values.
6. Review suspicious functions or classes.
7. Check network-related logic.
8. Look for obfuscation indicators.
9. Document observations.
10. Mark uncertain items for follow-up validation.

---

### Things I Looked For

I reviewed or searched for:

- Application permissions
- Manifest files
- Configuration files
- API endpoints
- External URLs
- Hardcoded credentials or tokens
- Authentication-related logic
- File access
- Network communication
- Data collection behavior
- Obfuscation
- Suspicious function names
- External libraries
- Debug or test values left in code

---

### Techniques Practiced

I practiced:

- Reading configuration files
- Searching source code with grep/ripgrep-style tools
- Looking for URL patterns
- Looking for API key or token patterns
- Reviewing permission declarations
- Mapping suspicious code to possible behavior
- Documenting findings with file paths and context

---

### Lessons Learned

Mobile/source-code analysis taught me that:

- Code can provide useful investigative leads.
- A suspicious string is not automatically a confirmed finding.
- Findings need context and validation.
- Permissions should be reviewed together with actual code behavior.
- Hardcoded values can be important, but they must be interpreted carefully.
- Documentation should include file paths, context and confidence level.

---

## Overall DFIR Lessons

Across these analysis tasks, I learned that good DFIR work requires:

- Safe handling
- Structured workflow
- Good notes
- Tool familiarity
- Careful validation
- Clear separation between evidence and assumptions
- Public/private reporting boundaries