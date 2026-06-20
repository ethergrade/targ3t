# Targ3t Agile Final Project – Penetration Testing Automation MVP

## Project Board Structure

Recommended Kanban columns:

1. Product Backlog
2. Sprint Backlog
3. In Progress
4. Done
5. Closed

## Sprint / Milestone

**Sprint 1 – Targ3t MVP Hardening**  
Suggested dates: 2026-07-01 to 2026-07-14

## User Stories

### 1. Improve interactive scan wizard

**User Story**  
As a penetration tester, I need an interactive scan wizard, so that I can configure a target scan without remembering every command-line option.

**Acceptance Criteria**  
Given that I start Targ3t in interactive mode  
When I enter the target, output folder, and scan phase  
Then the system validates my inputs and starts the correct scan workflow.

**Estimate:** 5 story points  
**Status:** In Progress  
**Labels:** user-story, product-backlog, sprint-backlog, backend, cli, priority-high

---

### 2. Support headless CLI execution

**User Story**  
As a security engineer, I need to run Targ3t in headless mode, so that I can automate scans in scripts or CI/CD pipelines.

**Acceptance Criteria**  
Given that I run Targ3t with command-line arguments  
When I provide target IP, report path, and selected phases  
Then the system executes without interactive prompts and stores the output correctly.

**Estimate:** 5 story points  
**Status:** In Progress  
**Labels:** user-story, product-backlog, sprint-backlog, backend, cli, automation, priority-high

---

### 3. Execute Nmap reconnaissance workflow

**User Story**  
As a penetration tester, I need automated Nmap reconnaissance, so that I can quickly identify open ports and exposed services.

**Acceptance Criteria**  
Given that a valid target is provided  
When the reconnaissance phase starts  
Then Targ3t runs Nmap and saves port, service, and version results in the target report folder.

**Estimate:** 8 story points  
**Status:** In Progress  
**Labels:** user-story, product-backlog, sprint-backlog, reconnaissance, backend, priority-high

---

### 4. Run web enumeration with Dirb

**User Story**  
As a web security analyst, I need automated web enumeration, so that I can discover hidden directories and web assets.

**Acceptance Criteria**  
Given that a target web service is detected  
When the web enumeration phase starts  
Then Targ3t runs Dirb and stores discovered paths, status codes, and output logs.

**Estimate:** 5 story points  
**Status:** In Progress  
**Labels:** user-story, product-backlog, sprint-backlog, web, reconnaissance, priority-medium

---

### 5. Run Nikto vulnerability assessment

**User Story**  
As a security analyst, I need automated Nikto web scanning, so that I can identify common web server vulnerabilities.

**Acceptance Criteria**  
Given that a web target is available  
When the vulnerability assessment phase starts  
Then Targ3t runs Nikto and saves findings in a structured report file.

**Estimate:** 5 story points  
**Status:** In Progress  
**Labels:** user-story, product-backlog, sprint-backlog, vulnerability-assessment, web, priority-high

---

### 6. Map discovered services to Searchsploit results

**User Story**  
As a penetration tester, I need discovered services mapped to Searchsploit results, so that I can quickly identify potential exploit references.

**Acceptance Criteria**  
Given that Nmap has identified services and versions  
When the exploit intelligence phase runs  
Then Targ3t queries Searchsploit and saves matching exploit references in the report folder.

**Estimate:** 8 story points  
**Status:** In Progress  
**Labels:** user-story, product-backlog, sprint-backlog, exploit-intelligence, backend, priority-medium

---

### 7. Generate structured report directory

**User Story**  
As a security consultant, I need a clean report directory structure, so that I can easily review evidence after a scan.

**Acceptance Criteria**  
Given that a scan is started  
When Targ3t creates the output workspace  
Then the system generates separate folders for reconnaissance, web enumeration, vulnerability assessment, credentials, and logs.

**Estimate:** 3 story points  
**Status:** In Progress  
**Labels:** user-story, product-backlog, sprint-backlog, reporting, backend, priority-high

---

### 8. Create scan summary report

**User Story**  
As a security consultant, I need a scan summary report, so that I can quickly communicate key findings to stakeholders.

**Acceptance Criteria**  
Given that scan phases are completed  
When the summary report is generated  
Then the system includes target information, executed phases, discovered services, key findings, and report file locations.

**Estimate:** 5 story points  
**Status:** In Progress  
**Labels:** user-story, product-backlog, sprint-backlog, reporting, priority-medium

---

### 9. Refactor global configuration variables

**User Story**  
As a developer, I need to refactor global configuration variables, so that Targ3t is easier to maintain and customize.

**Acceptance Criteria**  
Given that configuration values are currently spread across the script  
When the refactoring is completed  
Then dictionary paths, tool paths, and report paths are grouped in a clear configuration section.

**Estimate:** 3 story points  
**Status:** In Progress  
**Labels:** user-story, product-backlog, sprint-backlog, technical-debt, backend, priority-medium

---

### 10. Add automated shell script checks

**User Story**  
As a developer, I need automated shell checks, so that future script changes reduce the risk of regressions.

**Acceptance Criteria**  
Given that the repository contains Bash scripts  
When automated checks are executed  
Then the system validates shell syntax and reports errors before release.

**Estimate:** 5 story points  
**Status:** In Progress  
**Labels:** user-story, product-backlog, sprint-backlog, technical-debt, quality, priority-medium

---

## Sprint Estimate

Total: **52 story points**

| Issue | Story Points |
|---|---:|
| 1 | 5 |
| 2 | 5 |
| 3 | 8 |
| 4 | 5 |
| 5 | 5 |
| 6 | 8 |
| 7 | 3 |
| 8 | 5 |
| 9 | 3 |
| 10 | 5 |
| **Total** | **52** |

## Burndown Chart Data

| Day | Date | Remaining Story Points |
|---:|---|---:|
| 0 | 2026-07-01 | 52 |
| 1 | 2026-07-02 | 48 |
| 2 | 2026-07-03 | 43 |
| 3 | 2026-07-04 | 39 |
| 4 | 2026-07-05 | 34 |
| 5 | 2026-07-06 | 29 |
| 6 | 2026-07-07 | 25 |
| 7 | 2026-07-08 | 20 |
| 8 | 2026-07-09 | 15 |
| 9 | 2026-07-10 | 10 |
| 10 | 2026-07-11 | 6 |
| 11 | 2026-07-12 | 3 |
| 12 | 2026-07-13 | 0 |
