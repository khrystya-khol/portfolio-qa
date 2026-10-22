# Candidate Profile Setup Test Cases

## Wizard Behavior

| ID | Test Case |
|---|---|
| CPS-001 | Verify that the step indicator shows the correct progress and entered data persists when navigating between steps |
| CPS-002 | Verify that double-clicking the submit button on a wizard step submits the step only once |

## Step 1: Role and Core Skills

| ID | Test Case |
|---|---|
| CPS-003 | Verify that the Role and Position fields are required |
| CPS-004 | Verify that the Technical skills field accepts a minimum of 5 and a maximum of 15 skills |

## Step 2: Expectations and Salary

| ID | Test Case |
|---|---|
| CPS-005 | Verify that the monthly salary accepts values from $200 to $18,000 and rejects values outside this range |
| CPS-006 | Verify that the annual salary accepts values from $2,400 to $216,000 and rejects values outside this range |
| CPS-007 | Verify that the Office location field depends on the selected Employment type |

## Step 3: Job Experience

| ID | Test Case |
|---|---|
| CPS-008 | Verify that at least one job experience entry is required to proceed |
| CPS-009 | Verify that the LinkedIn experience import validates the profile link |
| CPS-010 | Verify that the manual experience form validates dates and text field limits |

## Step 4: Bio, File Uploads and Avatar

| ID | Test Case |
|---|---|
| CPS-011 | Verify that the profile photo upload accepts only JPG and PNG files up to 5MB |
| CPS-012 | Verify that the CV upload accepts only PDF, DOC and DOCX files up to 5MB |
| CPS-013 | Verify that the Web3 wallet address field validates the address format |
| CPS-014 | Verify that the Portfolio URL field validates the URL format |
| CPS-015 | Verify that the user can complete all steps and activate the profile |
