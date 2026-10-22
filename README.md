# Quality Assurance & Test Engineering Repository

## Overview
This repository contains the comprehensive quality engineering test suite for **Huntd**, an enterprise Web3 talent marketplace and recruitment platform. The test architecture has been systematically audited, refactored, and optimized using formal test design techniques—including Equivalence Partitioning (EP), Boundary Value Analysis (BVA), Role-Based Access Control (RBAC) Decision Matrices, and State Transition Modeling—reducing redundant test cases by over 80% while expanding critical path, edge case, and security coverage.

## Scope & Module Architecture

The functional test suite spans 13 core operational domains across candidate onboarding, recruiter outreach, candidate-recruiter real-time interaction, directory search, and platform navigation:

- **Global Layout & Navigation**:
  - `header.md`: Dynamic header navigation, authentication links, profile dropdown workflows, logout session invalidation, and viewport responsiveness.
  - `footer.md`: Global footer rendering, directory navigation matrices, Web3 company banner rules, social link target redirections, and legal compliance pages.
  - `global-elements.md`: Sticky global widgets (`[Twitter Bonus]` and `[?] Feedback`), role-based display conditions, modal lifecycles, and form validation.
- **Authentication & Onboarding**:
  - `sign-up.md`: Registration workflow, email/password field validations (EP/BVA), password mask toggles, OAuth social sign-up matrix, and profile role selection.
  - `sign_in.md`: Authentication flows, error handling for invalid credentials, password recovery workflow, social sign-in, and post-login role routing.
- **Profile Setup & Onboarding Wizards**:
  - `candidate-profile-setup.md`: 4-step candidate setup wizard, skill BVA (5–15 limit), salary range conversions ($200–$18k/mo), LinkedIn experience import, manual experience CRUD, bio, avatar upload/NFT wallet connection, and CV file attachment rules.
  - `recruiter-profile-setup.md`: 3-tab recruiter onboarding wizard, company detail validations, photo uploads, wallet string checks, candidate match calculations, and automated mass outreach workflow safety.
- **Profile Maintenance & Management**:
  - `edit_profile.md`: Dual-role profile management, saved state pre-population, differential updating, rollback on navigation cancel, profile data isolation, and attachment replacements.
- **Core Platform Features**:
  - `chat.md`: Real-time candidate-recruiter messaging, contact masking/unlocking mechanisms, job offer dispatches, chat archiving/favoriting, and input sanitization (XSS/HTML escaping).
  - `web3-companies.md`: Top 100 Web3 company directory grid, row-based dynamic counters, visual card rendering, and external vacancy redirections.
  - `home-switch.md`: Main landing page switches ("For Companies" vs "For Engineers"), CEO storytelling section, value prop comparison tables, mobile app promotion, and real review carousel/swipe mechanics.
  - `jobs.md`: Job board feed, skill tag filtering, expanded vacancy details, 1-click application workflows, manual and ATS job posting (Greenhouse/Lever), and subscription modal flows.
  - `candidates.md`: Candidate directory search, multi-faceted filter combinations (role, skills, salary, job experience, English level, location/timezone map), anonymous search counters, and saved filter notifications.

## Applied Test Design Methodology

To ensure high defect-detection capability and ISO/IEC/IEEE 29119 compliance without assertion bloat, the following black-box test design techniques were applied:

1. **Equivalence Partitioning (EP)**: Applied across input fields, file upload constraints (JPG/PNG vs unsupported GIF/executables), email string structures, and social media domain formats.
2. **Boundary Value Analysis (BVA)**: Applied to string character lengths (50-char names, 100-char positions, 1,000-char bio/achievements, 2,000-char chat messages), numeric bounds ($200–$18,000/mo salary), multi-select skill counts (5 to 15 skills), and 42-character Ethereum wallet address checks.
3. **Decision Matrix (RBAC)**: Consolidated visual display and interaction rules across Guest, Candidate, and Recruiter roles into multi-role verification matrices.
4. **State Transition Modeling**: Leveraged to model multi-step onboarding setup wizards, offer dispatches, contact unlocking, chat archiving, and session persistence across page refreshes.

## Test Suite Execution Summary

| Module Specification File | Core Domain Area | Optimization Approach |
| :--- | :--- | :--- |
| `header.md` | Header & Dynamic Navigation | RBAC Decision Matrix, Viewport Responsiveness |
| `footer.md` | Footer & Social Networks | Link Matrix Consolidation, Conditional Banner Display |
| `global-elements.md` | Floating Widgets & Modals | Sticky Positioning, Form Lifecycle Merging |
| `sign-up.md` | Registration & Role Selection | EP/BVA Rules, OAuth Redirection Grids |
| `sign_in.md` | Authentication & Recovery | Credential Logic, Password Reset Engine |
| `candidate-profile-setup.md` | Candidate Onboarding Wizard | BVA Skill/Salary Limits, File Upload Matrices |
| `recruiter-profile-setup.md` | Recruiter Onboarding Wizard | Step Persistence, Mass Outreach Double-Click Rules |
| `edit_profile.md` | Profile Maintenance | Dual-Role Isolation, Persistence & Rollback Logic |
| `chat.md` | Real-Time Messaging & Offers | State Transitioning, Privacy Contact Masking |
| `web3-companies.md` | Web3 Directory | Pagination Math, Hover & External Tab Links |
| `home-switch.md` | Landing Pages & App Promotion | Review Carousel Mechanics, Email Capture Logic |
| `jobs.md` | Vacancy Feed & Postings | ATS Import Engine, 1-Click Apply State Engine |
| `candidates.md` | Search & Candidate Filtering | Multi-Filter Combination, Timezone Map Logic |

## Tools & Framework Compliance
- **Test Management**: ISO/IEC/IEEE 29119 structured Markdown test cases.
- **Automation Compatibility**: Structured for direct mapping into **Playwright** / **Cypress** data-driven test suites using JSON/CSV parameter fixtures.
- **API / UI Verification**: Chrome DevTools, Network Payload Inspection, Postman.

## Repository Structure

```
├── README.md                      # Repository overview and QA methodology guide
├── header.md                      # Header Navigation test specifications
├── footer.md                      # Global Footer test specifications
├── global-elements.md             # Floating UI Widgets test specifications
├── sign-up.md                     # Registration & Role Switch test specifications
├── sign_in.md                     # Authentication & Password Recovery test specifications
├── candidate-profile-setup.md     # Candidate Onboarding Wizard test specifications
├── recruiter-profile-setup.md     # Recruiter Onboarding Wizard test specifications
├── edit_profile.md                # Profile Editing & Dual-Role Management test specifications
├── chat.md                        # Real-Time Chat & Job Offers test specifications
├── web3-companies.md              # Web3 Company Directory test specifications
├── home-switch.md                 # Landing Page Switch test specifications
├── jobs.md                        # Job Board & Posting test specifications
└── candidates.md                  # Candidate Search & Filter test specifications
```