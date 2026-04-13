##Prompt inicial para crear contexto

You are my software product manager assistant.
I want to perform  a product definition for a new Applicant Tracking System
This is a product that will be used by Recruiters and candidates during the whole job application cycle.

That's the first base definition a very simplistic one.

My goal is to produce a stronger first version of product artifacts:

✅ Brief description of LTI software, added value and competitive advantages.
✅ Explanation of the main functions.
✅ Add a Lean Canvas diagram to understand the business model.
✅ Description of the 3 main use cases, with the diagram associated with each one.
✅ Data model that covers entities, attributes (name and type) and relationships.
✅ High-level system design, both explained and with an attached diagram.
✅ C4 diagram that goes in depth into one of the system components, whichever you prefer.

I don't want to do all that at once. I want to tackle each item independently.

But before doing that. What I really want to do is prepare the context for this project, so that it can be user across multiple chats while creating each artifact.

So I want you to prepare an interview for me, where you will ask me questions about the product and the answer to those questions will be the initial definition and the context for the creation of the artifacts.

You  may plan all the questions  but we will go one by one and all of this information must be captured in a "context.md" live document that will hold the information and will evolve over time.

Is the plan clear or do yo have any questions ? 


##Prompt market research
You are my market researcher. You've got a deep understanding of the hiring lifecycle, modern and legacy hiring processes and existing tools.

I'm planning on creating an applicant tracking system.  For this I need to understand what are the main paint points for candidates, recruiters and hiring managers.

Provide a list with the top 10 pain points these people in this roles face during the recruiting process. 



## Prompt Product Brief 

Role: You are a senior product manager.

Context:
A whole product ideation was captured and refined  for the ATS MVP product and it was captured in the  "Context Final Reconciled.pdf". You must use all that information as the context for this task

Task: Use all the product information to create briefing for the ATS MVP that contains the following information: "Brief description of the software software, added value and competitive advantages."

Output format: MD



# Prompt:  Explanation of the main functions

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


