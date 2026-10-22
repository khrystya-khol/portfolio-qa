# Test Case Suites

## Overview

This repository contains the test case specifications for **Huntd**, a Web3 talent marketplace that connects candidates and recruiters. Each suite file lists categorized **Test Case IDs** and **Test Case summaries** as a testing checklist, without detailed steps or expected results.

The repository holds **13 suites** with **103 test cases**, covering navigation, authentication, profile setup and maintenance, chat, and the main platform pages. A separate **smoke suite** with 23 cases selects the critical checks from these suites.

## Test Suites

### Navigation and Layout

| Suite File | ID Prefix | Area | Cases |
|---|---|---|---|
| `header_navigation_suite.md` | HDR | Header navigation, authentication links, Profile dropdown, sign out | 6 |
| `footer_suite.md` | FTR | Footer layout, Web3 banner, internal, social and legal links | 7 |
| `global_elements_suite.md` | GLB | Global buttons: Twitter Bonus modal and Feedback form | 7 |

### Authentication

| Suite File | ID Prefix | Area | Cases |
|---|---|---|---|
| `sign_up_suite.md` | SUP | Registration, OAuth sign-up, profile type selection | 9 |
| `sign_in_suite.md` | SIN | Sign in, password recovery, OAuth sign-in | 8 |

### Profile Setup and Maintenance

| Suite File | ID Prefix | Area | Cases |
|---|---|---|---|
| `candidate_profile_setup_suite.md` | CPS | Candidate setup wizard: role, expectations, experience, bio | 15 |
| `recruiter_profile_setup_suite.md` | RPS | Recruiter setup: company details, contact information, candidate outreach | 8 |
| `edit_profile_suite.md` | EDP | Editing Candidate and Recruiter profiles | 7 |

### Core Platform Features

| Suite File | ID Prefix | Area | Cases |
|---|---|---|---|
| `main_switch_suite.md` | FCP/FEP | For Companies and For Engineers landing pages | 7 |
| `candidates_suite.md` | CND | Candidate search, filters, saved filters, notifications | 8 |
| `jobs_suite.md` | JOB | Job posting, ATS import, filters, 1-Click Apply, subscription form | 9 |
| `web3_companies_suite.md` | W3C | Top 100 Web3 Companies directory | 4 |
| `chat_suite.md` | CHT | Recruiter and Candidate chat, contact unmasking, job offers | 8 |

### Smoke Suite

| Suite File | ID Prefix | Area | Cases |
|---|---|---|---|
| `smoke_suite.md` | SMK | Critical happy-path checks across navigation, authentication, profile setup, candidates, jobs and chat, linked to the detailed cases | 23 |

## Conventions

- **IDs:** each case has an ID made of the suite prefix and a three-digit number, for example `HDR-001`. The Main Switch suite uses two prefixes: `FCP` for the For Companies page and `FEP` for the For Engineers page. Smoke cases use `SMK` and list the related detailed case IDs.
- **Wording:** every test case starts with "Verify that".
- **Roles:** Guest, Candidate and Recruiter.
- **Buttons:** written in square brackets, for example [Sign In].
- **Pages:** Home page, For Companies page, For Engineers page, Candidates List page, Jobs page, Web3 Companies page, Sign Up page and Sign In page.

## Test Design Techniques

The following black-box techniques are reflected in the cases:

1. **Equivalence Partitioning:** input formats (email, social links, wallet address) and allowed file types (photo and CV uploads).
2. **Boundary Value Analysis:** skills count (5 to 15), monthly and annual salary limits, file sizes and text limits.
3. **Role-Based Access:** visibility and behavior differences across Guest, Candidate and Recruiter.
4. **State Transition:** wizard steps, job offers, chat archiving and favorites, the Applied status, and signing out.

## Repository Structure

```
README.md
header_navigation_suite.md
footer_suite.md
global_elements_suite.md
sign_up_suite.md
sign_in_suite.md
candidate_profile_setup_suite.md
recruiter_profile_setup_suite.md
edit_profile_suite.md
main_switch_suite.md
candidates_suite.md
jobs_suite.md
web3_companies_suite.md
chat_suite.md
smoke_suite.md
```
