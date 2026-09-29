# CCCS 106 - Group Laboratory Task Submission: Form Validation & Defensive Programming

### 1. Group & Team Members Roster
- **Group Name / Number:** Qode Team / Group 12
- **Year & Section:** BSCS 3A
- **Date of Submission:** 2026-09-29
- **Submitting Member:** Kelly Saldo

| Role / Order | Full Name | Student ID Number |	Institutional Email |	Key Technical Contribution |
| :---: | :--: | :---: | :-- | :--- |
| **Member 1** |	Kelly Saldo |	2411287 |	kesaldo@my.cspc.edu.ph	| Regex, Domain Validator Engine, & Documentation |
| **Member 2** |	Rizelyn Borbe |	[202X-XXXX] |	[email@cspc.edu.ph] |	[e.g., Flet UI Reactive Error States & Events] |
| **Member 3** |	Tristan Bisenio |	[202X-XXXX] |	[email@cspc.edu.ph]	| [e.g., Dataclass Contracts & Automated Testing] |
| **Member 4** |	Nash Sabas |	[202X-XXXX] |	[email@cspc.edu.ph]	| Regex & Domain Validator Engine |

### 2. Git Repository & Commit Verification
- **Dedicated GitHub Repository URL:** (https://github.com/kellysldo/cccs106-lab-form-validation-group12)
- **Repository Visibility:** Public
- **Final Verified Commit SHA on `main`:** [Paste 7-character or 40-character commit hash, e.g., a1b2c3d]

### 3. Automated Test Suite Output (`test_validation.py`)

Run `python test_validation.py -v` in your terminal and paste the full output block below:

```cmd
[Paste terminal test execution output here showing all 14 tests passing with "OK"]
```


### 4. Verification Screenshots
**A. Multi-Field Validation Error State (Matching Figure 1)**

_(Ensure red error borders, error descriptions, and red SnackBar are clearly visible)_
![Validation Error Screenshot]([Upload or paste screenshot here])

**B. Successful Application Registration State (Matching Figure 2)**

_(Ensure clean form fields, green SnackBar, and the session contract card are clearly visible)_
![Successful Registration Screenshot]([Upload or paste screenshot here])

### 5. Technical Reflection & Engineering Audit
- **Defensive Error Handling:** [In 1–2 sentences, explain how the team's code prevents GUI crashes when non-numeric or malformed GWA inputs are entered.]
- **Multi-Tier Separation:** [In 1–2 sentences, explain why client-side Flet error clearing alone does not replace domain-tier validation.]
- **Team Collaboration Reflection:** [In 1–2 sentences, describe how your team coordinated branch merges, code reviews, or pairing to complete the validation pipeline.]
