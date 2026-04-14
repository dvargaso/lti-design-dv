# ATS MVP Briefing

## Brief description of the software

The **ATS MVP** is a simple Applicant Tracking System designed for **small businesses** to centralize and standardize hiring. It combines an **internal web application** for company staff with an **ATS-managed public careers page** where external candidates can view open roles and submit applications. The product is intentionally narrow in scope: it focuses on covering the core hiring flow end to end without adding unnecessary complexity, heavy automation, or enterprise-style features.

## Added value

The ATS MVP creates value by giving small teams **one shared place** to manage hiring, making each candidate’s status visible and showing what needs to happen next. It helps replace fragmented hiring practices spread across email, spreadsheets, notes, and memory with a clearer, more consistent, and more structured process. This allows teams to run hiring in a way that is **clear, shared, and consistent**.

## Competitive advantages

* **Right-sized for small companies**: built for organizations with modest hiring needs, without the weight of enterprise complexity.
* **Clear visibility**: makes candidate status and next actions easy to understand at any time.
* **Clear ownership**: supports explicit responsibility across the hiring process, helping teams know who should act next.
* **Consistent hiring process**: uses one fixed pipeline and standardized handling to reduce ad hoc or inconsistent recruiting practices.
* **Simplicity by design**: intentionally excludes integrations, advanced scheduling, multi-tenant support, complex approvals, and other non-MVP features in order to stay easy to adopt and operate.

## Summary statement

The ATS MVP is a **simple, right-sized hiring system for small businesses** that delivers **centralized hiring operations, clear process visibility, and consistent execution** without unnecessary complexity. 


# ATS MVP Briefing — Main Functions

The ATS MVP is designed to manage the hiring process end to end for a small business: from creating job openings and collecting applications to tracking candidates, coordinating interviews, gathering feedback, and recording final hiring decisions.

## 1. Job management and publishing

The system allows internal users to create and manage job openings, assign key owners, and publish jobs to the **ATS-managed public careers page**. Publishing is intentionally limited to that single public careers surface; external posting channels are not part of the MVP.

## 2. Candidate application intake

Candidates can browse open jobs, view job details, and submit applications through the public apply form. The system captures core applicant data and CV/resume submission, then brings that information into the internal hiring workflow. There is no candidate portal or post-application self-service in MVP.

## 3. Candidate and application record management

The product stores **candidate profiles** separately from **job application records**. Candidate profiles hold stable person-level data, while applications hold job-specific process data such as stage, status, feedback history, assigned owners, and next action ownership. This separation keeps hiring operations structured and reduces confusion across multiple applications.

## 4. Pipeline tracking and workflow control

A core function of the ATS MVP is moving candidates through **one fixed hiring pipeline** shared across all jobs. The system tracks where each candidate is in the process, who is responsible for the next step, and what action is required next. Pipeline stages are used for active workflow steps, while final outcomes are tracked through application status.

## 5. Interview scheduling and tracking

Recruiters can create and maintain interview records inside the ATS, including interview type, date/time, interviewer, format, location or meeting link, and status. The system tracks interviews operationally, but calendar sync, automated invites, interviewer availability logic, and self-scheduling are out of scope for MVP.

## 6. Feedback and evaluation capture

The product supports structured feedback collection using a standard feedback format. Interviewers and hiring managers can record recommendations, ratings, strengths, concerns, comments, and confidence. This gives the team a consistent way to evaluate candidates across the hiring flow.

## 7. Communication logging and follow-up tracking

The ATS MVP logs hiring-related communication as an internal timeline of interactions and notes, such as emails sent, calls made, interview invites, and message notes. It also supports basic follow-up tracking. This is logging only, not outbound communication automation.

## 8. Offer and final decision handling

The system includes **basic offer management** and final hiring decision recording. Offer handling is intentionally lightweight, and final outcomes such as hired, rejected, withdrawn, or closed are recorded at the application level. Decision ownership and status recording are clearly separated in the workflow.

## 9. Operational visibility for daily hiring work

The landing view is designed to support day-to-day execution, not analytics. Its main purpose is to show which candidates need action, what the next required action is, who owns it, what interviews are coming up, which applications are recent, and which jobs are open.

## Summary

In practical terms, the main functions of the ATS MVP are to:

* manage job openings
* collect candidate applications
* maintain candidate and application records
* track candidates through a fixed hiring pipeline
* schedule and track interviews
* collect structured feedback
* log communication and follow-ups
* record offers and final decisions
* surface next actions clearly for the hiring team 

# Lean Canvas — ATS MVP

*Based on the approved ATS MVP product context in* **Context Final Reconciled.pdf**, *with revenue model clarified in this chat as a flat monthly SaaS fee.*

| **Problem**                                                                                                                                                                                                         | **Solution**                                                                                                                                                                                                                                                                   | **Unique Value Proposition**                                                                                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Hiring data is scattered across email, spreadsheets, notes, and memory.<br><br>Tracking is manual and inconsistent.<br><br>Status and next steps are hard to see.<br><br>Hiring is fragmented and not standardized. | One shared candidate database.<br><br>One fixed hiring pipeline.<br><br>ATS-managed public careers page.<br><br>Candidate and application records.<br><br>Interview scheduling records, feedback, communication log, follow-ups, offer tracking, and final decision recording. | **A simple, right-sized ATS for small companies that centralizes hiring, makes every candidate’s status clear, and shows what needs to happen next.**<br><br>Structured hiring without enterprise complexity. |

| **Unfair Advantage**                                                                                                                                                                                                                                        | **Customer Segments**                                                                                                                                                                                                                                                         | **Key Metrics**                                                                                                                                                                                                                                                                                                                                    |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Simplicity-first design for small teams.<br><br>Clear ownership through assigned recruiter, hiring manager, and next action owner.<br><br>Strong visibility into status and next steps.<br><br>Standardized hiring flow with auditability and traceability. | Small businesses with **50–100 employees**.<br><br>Modest hiring volume: about **10–12 openings per year**.<br><br>Core internal users: HR Admin/Manager, Recruiter, Hiring Manager, Interviewer.<br><br>External candidate uses only the public careers page and apply form. | ATS becomes the default place to manage hiring.<br><br>Candidate progress and ownership are always clear.<br><br>One consistent hiring process is followed.<br><br>No parallel trackers are maintained.<br><br>The MVP covers the full hiring flow without operational gaps.<br><br>Key decisions and status changes are easy to review afterward. |

| **Channels**                                                                                              | **Cost Structure**        | **Revenue Streams**        |
| --------------------------------------------------------------------------------------------------------- | ------------------------- | -------------------------- |
| ATS-managed public careers page for applicants.<br><br>Commercial acquisition channels: **out of scope**. | **Out of scope** for now. | **Flat monthly SaaS fee**. |



# Use Cases

## 1. Create and Manage Job Openings

This use case covers how HR Admin / Manager sets up and maintains a job opening in the ATS, including creating and
editing the job, assigning the recruiter and hiring manager, managing the job status, and publishing it. In MVP,
publishing is limited to the ATS-managed public careers page, and closing a job can automatically close any remaining
active applications tied to it.

```mermaid
flowchart LR
    A[HR Admin / Manager]

    subgraph S["System boundary: ATS MVP"]
        UC1((Create job opening))
        UC2((Edit job opening))
        UC3((Assign recruiter))
        UC4((Assign hiring manager))
        UC5((Set job status: Draft / Open / On Hold / Closed))
        UC6((Publish job to ATS-managed public careers page))
        UC7((Close job opening))
        UC8((Auto-close remaining active applications))
        UC9((Log job closure in audit trail))
        N1["Constraint: publishing is limited to the ATS-managed public careers page"]
    end

    A --> UC1
    A --> UC2
    A --> UC5
    A --> UC6
    A --> UC7

    UC1 -. includes .-> UC3
    UC1 -. includes .-> UC4
    UC1 -. includes .-> UC5
    UC2 -. may update .-> UC3
    UC2 -. may update .-> UC4
    UC6 -. constrained by .-> N1
    UC7 -. includes .-> UC8
    UC7 -. includes .-> UC9
```

## 2. Collect Candidate Applications from the Public Careers Page

This use case covers how an external candidate browses open jobs, views a job detail page, completes the public apply
form, uploads a CV, and submits an application. The ATS stores the candidate profile and related application record,
reuses an existing candidate profile when the email already exists, and treats a repeated submission to the same job as
a reapplication event rather than creating a duplicate active application. There is no candidate portal or
post-application interaction in MVP beyond submission confirmation

```mermaid
flowchart LR
    C[Candidate]

    subgraph S["System boundary: ATS MVP public careers page"]
        UC1((View open jobs))
        UC2((View job detail page))
        UC3((Submit application))
        UC4((Enter required fields))
        UC5((Enter optional fields))
        UC6((Upload CV / resume))
        UC7((Detect existing candidate by email))
        UC8((Reuse existing candidate profile))
        UC9((Create job application))
        UC10((Treat same-job repeat submission as reapplication event))
        UC11((Store candidate profile))
        UC12((Store application record))
        UC13((Show submission confirmation))
        N1["Constraint: no candidate portal or post-application interaction in MVP"]
    end

    C --> UC1
    C --> UC2
    C --> UC3

    UC2 -. supports .-> UC3
    UC3 -. includes .-> UC4
    UC3 -. may include .-> UC5
    UC3 -. includes .-> UC6
    UC3 -. includes .-> UC7
    UC7 -. when email matches .-> UC8
    UC7 -. for different job .-> UC9
    UC7 -. for same job .-> UC10
    UC3 -. includes .-> UC11
    UC3 -. includes .-> UC12
    UC3 -. includes .-> UC13
    UC13 -. constrained by .-> N1
```

## 3. Review and Screen Applications

This use case covers how internal hiring staff evaluate incoming applications within the fixed MVP hiring pipeline.
Recruiters review applications, perform the HR / Recruiter Screen, record notes, and move candidates through allowed
stages; Hiring Managers review candidates and provide decision input within their scope, but they do not directly change
stages or statuses; HR Admin / Manager retains override authority. The goal is to keep candidate status, next action,
and ownership clear throughout screening and review.

```mermaid
flowchart LR
    R[Recruiter]
    HM[Hiring Manager]
    HR[HR Admin / Manager]

    subgraph S["System boundary: ATS MVP"]
        UC1((Search applications))
        UC2((Filter applications))
        UC3((View candidate and application))
        UC4((View candidates needing action))
        UC5((Perform HR / Recruiter Screen))
        UC6((Record notes))
        UC7((Recommend proceed or reject))
        UC8((Review candidates in Hiring Manager Review))
        UC9((Submit feedback))
        UC10((Approve proceed or reject within scope))
        UC11((Execute stage / status transition))
        UC12((Move to next allowed stage))
        UC13((Move back to previous stage))
        UC14((Override stage change))
        N1["Constraint: Hiring Manager provides decision input only and does not directly change stages or statuses"]
    end

    R --> UC1
    R --> UC2
    R --> UC3
    R --> UC4
    R --> UC5
    R --> UC11

    HM --> UC3
    HM --> UC8

    HR --> UC3
    HR --> UC11
    HR --> UC14

    UC5 -. includes .-> UC6
    UC5 -. includes .-> UC7
    UC8 -. includes .-> UC9
    UC8 -. includes .-> UC10
    UC11 -. recruiter path .-> UC12
    UC11 -. recruiter path .-> UC13
    UC14 -. extends .-> UC11
    UC8 -. constrained by .-> N1
```

# Data Model