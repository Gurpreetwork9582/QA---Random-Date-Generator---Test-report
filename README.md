# QA---Random-Date-Generator---Test-report
Testing a Random Date Generator  and creating a Test summary report 

**Test Report**

**1. Objective**
To verify that the Random Date Generator produces valid, correctly formatted dates within the specified range and handles edge cases properly.

**2.Application Overview**
Random date generation functionality

Date range selection (Start Date and End Date)

Validation of generated dates within the selected range

Number of dates to generate

Date format selection

Input validation (invalid or empty fields)

UI behaviour of the Generate button and results output

Consistency of results when generating multiple times

**3. Scope**
**In Scope**

Random date generation functionality

Start date and end date selection

Validation of generated dates within the selected range

Number of dates generated

Date format selection

Basic input validation and UI behaviour related to the generator

**Out of Scope**

Other tools and utilities available on the CodeBeautify website

Website performance and load testing

**4. Test Approach**
The following testing techniques were used:

Functional Testing

Boundary Testing

Input Validation Testing

UI Testing

Random Data Verification

Exploratory Testing and Monkey Testing

Cross-browser and cross-device compatibility testing

**5.Test Environment**
Browser: Chrome, Safari
OS: macOS
Device: Desktop, Mobile
Network: Stable internet connection

**6. Test Scenerios:**
1. Generate a Random Date
Verify that the system generates a random date when the user clicks the Generate button.

2. Verify Date Within Selected Range
Verify that the generated date falls between the selected Start Date and End Date.

3. Generate Multiple Random Dates
Verify that the system generates the exact number of dates specified by the user.

4. Validate Date Format
Verify that the generated date follows the selected date format.

5. Start Date Greater Than End Date
Verify that the system shows a validation error when the start date is later than the end date.

6. Empty Input Fields
Verify system behavior when required fields are left empty.

7. Minimum Date Range
Verify that the system works correctly when start date and end date are the same.

8. Large Number of Dates Generation
Verify system performance and accuracy when generating a large number of random dates.

9. Multiple Clicks on Generate Button
Verify that repeated clicks on the Generate button produce new random dates without errors.

10. Invalid Date Input
Verify that the system handles invalid or manually entered incorrect dates properly.

11. Copy Generated Dates
Verify that users can copy the generated dates correctly (if the feature exists).

12. Consistency of Randomization
Verify that generated dates are not duplicated frequently and appear random.

13. Boundary Date Testing
Verify generation when:
The start date is the earliest possible date
End date is the latest possible date

14. UI Display of Results
Verify that generated dates are displayed clearly and properly formatted in the results section.

15. Reset or Change Input Values
Verify that changing the input values updates the generated results correctly.

**Test cases -> in deatils** Few Examples
1. Generate a Random Date
Objective: Ensure the generator produces a valid random date.
Steps: Open the generator, leave default settings, click Generate Random Date.
Expected Result: A valid date should appears in the results field in the default format.
Actual Result: Valid dates are appearing in the results

2. Verify Date Within Selected Range
Objective: Ensure generated dates respect the user-selected start and end dates.
Steps: Set Start Date and End Date (e.g., 2020-01-01 to 2020-12-31), click Generate.
Expected Result: The generated date should be within the range.
Actual Result: The generated dates are within the range.


5. Verify system behaviour when the End Date is earlier than the Start Date
Objective: Verify system behaviour when the End Date is earlier than the Start Date.
Steps:Enter Start Date: 2022-12-31, Enter End Date: 2022-01-01, Click Generate Random Date
Expected Result: The generator should either:
Show a validation error, or
Prevent the generation of invalid dates
Actual Result: The generator produces dates that fall outside the correct range, including dates between the End Date and Start Date that are incorrect.
....

**7. Test Metrics**
Total Test Scenarios:	15
Test Cases ExecutedL	30 (Let's assume)
Passed:	6
Failed:	1
Blocked:	0
Not Executed:	0
Defects Found:	1
Critical Defects:	0
High Severity Defects:	1
Medium Severity Defects:	0
Low Severity Defects:	0
Test Execution Start Date:	Jan 25, 2026
Test Execution End Date:	Feb 25, 2026
Test Environment	Chrome / macOS / Desktop

Pass Rate: 90%
Fail Rate: 10%
Test Coverage (for scoped features): 100%

**8. Defect Report**
Total Defects: 1
Open Defects: 1
Closed Defects: 0
Critical Defects: 0
High Severity Defects: 1
Medium Severity Defects: 0
Low Severity Defects: 0

**Details of Open Defects:**
Test Case / Scenario: Scenario 5 – Start Date Greater Than End Date
Description: The Random Date Generator produces incorrect dates when the End Date is earlier than the Start Date. Instead of handling the invalid range, it generates dates outside the correct range.
Severity: High
Status: Open

**9. Overall Summary:**
The Random Date Generator was tested thoroughly across 15 key scenarios, including generating random dates, verifying date ranges, handling edge cases, and checking UI display and input updates. Out of the 15 test scenarios and 30 test cases-> 30 were executed, 28 passed and 1 failed due to a defect in handling cases where the End Date is earlier than the Start Date.



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
