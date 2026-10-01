# CCCS 106 - Group Laboratory Task Submission: Form Validation & Defensive Programming

### 1. Group & Team Members Roster
- **Group Name / Number:** I-git
- **Year & Section:** BSCS 3A
- **Date of Submission:** 2026-09-30
- **Submitting Member:** Kelly Saldo

| Role / Order | Full Name | Student ID Number |	Institutional Email |	Key Technical Contribution |
| :---: | :--: | :---: | :-- | :--- |
| **Member 1** |	Kelly Saldo |	2411287 |	kesaldo@my.cspc.edu.ph	| Domain Validator Engine, Defensive Pipeline, & Documentation|
| **Member 2** |	Rizelyn Borbe |	2410605 |	riborbe@my.cspc.edu.ph |	Flet UI Reactive Error States & Documentation |
| **Member 3** |	Tristan Bisenio |	232000006 |	trbisenio@my.cspc.edu.ph	| Defensive Pipeline & Automated Testing |
| **Member 4** |	Nash Sabas |	2412117  |	sanash@my.cspc.edu.ph	| Regex & Domain Validator Engine |

### 2. Git Repository & Commit Verification
- **Dedicated GitHub Repository URL:** (https://github.com/kellysldo/cccs106-lab-form-validation-group12)
- **Repository Visibility:** Public
- **Final Verified Commit SHA on `main`:** [Paste 7-character or 40-character commit hash, e.g., a1b2c3d]

### 3. Automated Test Suite Output (`test_validation.py`)

Run `python test_validation.py -v` in your terminal and paste the full output block below:

```cmd

python test_validation.py -v
test_dataclass_contract_creation (__main__.TestScholarshipValidator.test_dataclass_contract_creation) ... ok
test_gui_submission_flow (__main__.TestScholarshipValidator.test_gui_submission_flow) ... ok
test_invalid_email_domain (__main__.TestScholarshipValidator.test_invalid_email_domain) ... ok
test_invalid_gwa_non_numeric (__main__.TestScholarshipValidator.test_invalid_gwa_non_numeric) ... ok
test_invalid_gwa_out_of_bounds (__main__.TestScholarshipValidator.test_invalid_gwa_out_of_bounds) ... ok
test_invalid_name_empty (__main__.TestScholarshipValidator.test_invalid_name_empty) ... ok
test_invalid_name_length_and_symbols (__main__.TestScholarshipValidator.test_invalid_name_length_and_symbols) ... ok
test_invalid_phone_numbers (__main__.TestScholarshipValidator.test_invalid_phone_numbers) ... ok
test_invalid_student_id_format (__main__.TestScholarshipValidator.test_invalid_student_id_format) ... ok
test_valid_email (__main__.TestScholarshipValidator.test_valid_email) ... ok
test_valid_gwa (__main__.TestScholarshipValidator.test_valid_gwa) ... ok
test_valid_name (__main__.TestScholarshipValidator.test_valid_name) ... ok
test_valid_phone_normalization (__main__.TestScholarshipValidator.test_valid_phone_normalization) ... ok
test_valid_student_id (__main__.TestScholarshipValidator.test_valid_student_id) ... ok

----------------------------------------------------------------------
Ran 14 tests in 0.160s

OK

```


### 4. Verification Screenshots
**A. Multi-Field Validation Error State (Matching Figure 1)**

_(Ensure red error borders, error descriptions, and red SnackBar are clearly visible)_
![Validation Error Screenshot](screenshots/error-state.png)

**B. Successful Application Registration State (Matching Figure 2)**

_(Ensure clean form fields, green SnackBar, and the session contract card are clearly visible)_
![Successful Registration Screenshot](screenshots/success-state.png)

### 5. Technical Reflection & Engineering Audit
- **Defensive Error Handling:** If someone types something that isn't a number in the GWA field, our validator catches the conversion error (TypeError or ValueError) and raises a GWARangeError with a clear message, so the app doesn't crash. The form then shows that message in red under the field, along with a red SnackBar, and the user can fix it and try again.

- **Multi-Tier Separation:** The red error styling in Flet only changes what the user sees on screen. The real rules live in the validator, so wrong data still gets rejected even if someone skips the form or the UI changes. It also lets us test the rules without opening the app, which is what our 14 tests do.

- **Team Collaboration Reflection:**  The team split the work by role and used separate feature branches (feature/scholarship-validation, feature/bisenio, and feature/Borbe), merging into main through pull requests. The process was not smooth. Tristan's branch was 9 commits behind and 2 ahead of main, so GitHub could not merge its pull request automatically --- he merged it directly into main instead. That merge was committed with unresolved conflict markers in scholarship_portal.py, which made the whole test suite fail with a SyntaxError until Kelly fixed it. Later, Rizelyn's push to feature/Borbe was rejected after a teammate had edited the same README sections. These problems taught the team to update their branch with the latest main and resolve conflicts there before opening a pull request, to check for leftover conflict markers before committing, and to rerun the 14 tests after every merge. The team should remember to assign each person their own files or README sections to avoid overlapping edits next time.