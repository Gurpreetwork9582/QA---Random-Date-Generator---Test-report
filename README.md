

**Defect:**
Bug Report – BUG-001

Title: Random Date Generator produces incorrect dates when End Date is earlier than Start Date

Severity: High
Priority: High

Environment:
Browser: Chrome
OS: macOS
Device: Desktop
Network: Stable

Steps to Reproduce:
Open the Random Date Generator
Enter Start Date: 2029-01-01
Enter End Date: 2022-12-31
Click Generate Random Date

Expected Result:
The generator should either:
Show a validation error: “Start date cannot be greater than End Date”, or
Prevent the generation of any dates outside the logical range.

Actual Result:
The generator produces dates that are outside the correct range, including dates between End Date and Start Date incorrectly.

Screenshot / Attachment:
<img width="754" height="577" alt="Screenshot 2026-02-25 at 9 16 08 PM" src="https://github.com/user-attachments/assets/cdab9684-2473-45ad-b01a-011e521f0d86" />
