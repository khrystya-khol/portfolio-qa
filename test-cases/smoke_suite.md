# Smoke Test Cases

> Run these cases on every new build to confirm the critical functions work before deeper testing starts. Each case is a short, positive check of a core flow, with no boundary or negative scenarios. The Related Cases column points to the detailed cases in the other suites.

## Application Access and Navigation

| ID | Test Case | Related Cases |
|---|---|---|
| SMK-001 | Verify that the For Engineers page loads as the default landing page | FEP-001 |
| SMK-002 | Verify that the For Companies page loads and its call-to-action button redirects the user to the Candidates List page | FCP-001, FCP-002 |
| SMK-003 | Verify that the header logo and primary navigation links redirect to the correct pages | HDR-001 |
| SMK-004 | Verify that the footer is displayed and its main links redirect to the correct pages | FTR-001, FTR-005 |

## Registration and Authentication

| ID | Test Case | Related Cases |
|---|---|---|
| SMK-005 | Verify that a new user can register with a valid email and password | SUP-006 |
| SMK-006 | Verify that the user can choose the Candidate or Recruiter profile type after registration | SUP-009 |
| SMK-007 | Verify that Candidate and Recruiter can sign in and are redirected to the correct page | SIN-003 |
| SMK-008 | Verify that the user can sign out and the session is ended | HDR-006 |

## Profile Setup and Management

| ID | Test Case | Related Cases |
|---|---|---|
| SMK-009 | Verify that Candidate can complete all profile setup steps and activate the profile | CPS-001, CPS-015 |
| SMK-010 | Verify that Recruiter can complete the company details and contact information steps | RPS-001, RPS-002 |
| SMK-011 | Verify that Recruiter can send the greeting message to matching candidates | RPS-006, RPS-007 |
| SMK-012 | Verify that the user can open the profile edit form and update profile data | EDP-001, EDP-004, EDP-007 |

## Candidates and Web3 Companies

| ID | Test Case | Related Cases |
|---|---|---|
| SMK-013 | Verify that the Candidates List page loads and candidates can be filtered with the Role and Technologies filters | CND-001 |
| SMK-014 | Verify that Guest sees the sign-up prompt when hovering over the Filters section | CND-005 |
| SMK-015 | Verify that the Top 100 Web3 Companies grid is displayed | W3C-001 |
| SMK-016 | Verify that clicking a company opens its vacancies page in a new browser tab | W3C-004 |

## Jobs

| ID | Test Case | Related Cases |
|---|---|---|
| SMK-017 | Verify that the Jobs page loads and a vacancy expands to show its details | JOB-005 |
| SMK-018 | Verify that Candidate can apply for a vacancy with the [1-Click Apply] button and sees the Applied status | JOB-006, JOB-007 |
| SMK-019 | Verify that Recruiter can post a job | JOB-001, JOB-002 |

## Chat

| ID | Test Case | Related Cases |
|---|---|---|
| SMK-020 | Verify that Recruiter can start a chat thread with a candidate | CHT-001 |
| SMK-021 | Verify that messages can be sent in a chat thread | CHT-001, CHT-007 |
| SMK-022 | Verify that candidate contacts stay hidden until the candidate agrees to share them | CHT-005 |
| SMK-023 | Verify that a job offer can be sent in the chat thread | CHT-006 |
