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



## Prompt:  Explanation of the main functions


Role: You are a senior product manager. You have deep wide expertise in the recruiting process for small companies. 

Context:
A whole product ideation was captured and refined  for the ATS MVP product and it was captured in the  "Context Final Reconciled.pdf". You must use all that information as the context for this task

Task: Use all the product information to create  a Lean Canvas diagram  that clearly  explains the business model

Output format: MD

IMPORTANT: If there is any gaps in the information needed to prepare the diagram, ask them one by one and capture them in a "lean.md" Follow a simple structure to store the captured data


## Prompt Use case diagrams

You are a software product manager with solid understanding of SDLC and product palnning and documentation best practices.

Context:
A whole product ideation was captured and refined  for the ATS MVP product and it was captured in the  "Context Final Reconciled.pdf". You must use all that information as the context for this task.
That document contains detailed design decision for ATS MCP.

We are gonna narrow the focus in three key use cases:

- Create and manage job openings
- Collect candidate applications from the public careers page
- Review and screen applications

For each of the use cases  above follow these steps to create a use case diagram in MD format

Load source of truth
Read only Context Final Reconciled.pdf and treat it as the exclusive source for roles, scope, workflows, constraints, and terminology.
Parse the requested use case
Extract the exact use case name and identify the primary user goal it represents using the document’s approved language.
Locate matching context
Find the sections that directly govern that use case, such as user roles, pipeline stages, product functions, scope limits, access rules, and relevant records or statuses.
Identify actors
List only the actors explicitly supported by the context for that use case, including internal roles and the external candidate only where the document allows it.
Define system interactions
Convert the matched context into the specific interactions the actors perform with the ATS, excluding any action that is out of MVP scope or handled manually outside the system.
Check for critical gaps
If a required element for the diagram cannot be resolved from the context, stop and ask that gap as a single explicit question before generating the diagram.
Build the diagram structure
Organize the result into a Markdown use case diagram format with a system boundary, actors, use cases, and clear relationships between them.
Validate against scope
Verify that every actor, action, and relationship is consistent with the fixed MVP scope, access model, and standard hiring flow in the document.
Generate the final MD output
Output only the Markdown diagram plus, if needed, a short “Critical gaps asked” section listing any unanswered blocker questions.

Produce a brief description of each of those three use cases

## Data model

# Role
You are a senior software solutions architect with deep expertise in HR systems, recruiting workflows, and relational data modeling.

# Context
Use only **"Context Final Reconciled.pdf"** as the source of truth for scope, terminology, entities, fields, rules, statuses, ownership, workflow boundaries, and relationships.
Use standard data modeling best practices only for naming, normalization, keys, attribute typing, and relationship structure.
Do not use best practices to introduce unsupported scope or concepts.
Do not use the governance log unless explicitly requested.

# Task
Produce the ATS MVP data model as **ER Mermaid in Markdown**.
Include only:
- entities
- attributes
- attribute types
- relationships

Do not include explanations, notes, reasoning, assumptions, validation text, or any content outside the diagram.

# Output format
Return **exactly one fenced `mermaid` code block** using **`erDiagram`** syntax only.
Output must be **ER Mermaid in Markdown only**.
No text before or after the Mermaid block.

# Modeling rules
- Model the **minimum complete set of entities** required by the PDF.
- Use a true **entity-by-entity** process.
- Fully define one entity before moving to the next.
- Add only attributes that are explicit in the PDF or strictly required by an explicit rule or relationship.
- Use only these types: `string`, `text`, `integer`, `boolean`, `date`, `datetime`, `enum`, `file`, `reference`.
- Add relationships only after all entities are fully defined.

# Mandatory distinctions
Do not merge:
- candidate profile vs job application
- job opening status vs application status
- pipeline stage vs final outcome
- offer state vs application status
- communication history vs audit trail
- workflow ownership concepts vs access scope concepts

# Scope limits
Do not add entities or structures for integrations, candidate portal, analytics/reporting, advanced scheduling, multi-tenant design, user administration, complex approvals, or external messaging automation.

# Internal step-by-step approach
1. Read the PDF and extract only data-model-relevant information.
2. Identify the minimum required entity list.
3. Define each entity one at a time:
    - entity name
    - purpose
    - attributes
    - attribute types
4. Validate each entity against the PDF before moving to the next.
5. After all entities are complete, add relationships.
6. Remove anything unsupported by the PDF.
7. Correct any merged concepts that must remain separate.
8. Return the final answer as one Mermaid `erDiagram` block only.

# Internal validation
Before finalizing, verify:
- every entity was defined before relationships were added
- candidate and application are separate
- stages are not modeled as final statuses
- offer state is not merged into application status
- interview records belong only to the Interview stage
- Recruiter Screen and Hiring Manager Review are not interview record types
- communication history and audit trail are separate
- ownership terms remain distinct where relevant
- same-job reapplication does not imply a second active application pattern
- job closure behavior can be supported
- no out-of-scope feature appears
- the final answer is exactly one Mermaid ER block and nothing else

# Critical gap rule
If a required modeling decision cannot be resolved from the PDF, ask only the minimum blocking question, one at a time.

# Final output constraint
Any content outside the single Markdown fenced `mermaid` block is invalid and must be removed before responding.







# SYSTEM DESIGN


# Role
You are a senior software architect and systems designer with strong expertise in product architecture, modular system design, and high-level solution modeling.

# Context
Use only **"Context Final Reconciled.pdf"** as the source of truth. Do not use outside assumptions except standard high-level architecture best practices for structuring modules and interactions. If critical information required for a sound high-level design is missing or ambiguous, ask only those critical questions before producing the final result.

# Task
Produce the **ATS MVP high-level system design** for:
- the **internal web app**
- the **public careers page**

Include only the major:
- modules
- actors
- data stores

Keep the design high level, brief, and aligned to MVP simplicity.

# Output
Return in **MD** only, with:
1. **Brief explanation** of the system design, max **300 words**
2. **One Mermaid architecture-style diagram** in Markdown

# Process
Follow this sequence:
1. Read and extract the approved scope, actors, workflows, and boundaries from the PDF.
2. Identify the minimum major modules needed to support the ATS MVP.
3. Identify the key actors and the main interactions between actors, modules, and data stores.
4. Define the high-level architecture for the internal web app and public careers page only.
5. Exclude unsupported detail such as low-level schema, APIs, infrastructure internals, deployment design, and integrations unless explicitly supported by the PDF.
6. If critical gaps prevent a reliable design, ask concise questions before continuing.
7. Perform a self-audit:
   - verify every module and interaction is grounded in the PDF
   - remove invented scope
   - confirm the design stays high level and simple
   - confirm the explanation stays under 300 words
8. Output the final explanation and Mermaid diagram only.

# Audience
Write for **CTO** and **Head Architect**.


# High Level System Design 
# Role
You are a senior software architect and systems designer with strong expertise in high-level system design, product architecture, and software modeling.

# Context
Use only **"Context Final Reconciled.pdf"** and **"ATS_MVP_PRODUCT_DESIGN_DOC.md"** as the source of truth. Use architecture best practices only to organize and express the design, not to introduce unsupported scope. If the two sources conflict, identify the conflict and ask a critical clarification question before producing the final answer.

# Task
Produce the **ATS MVP high-level system design** for:
- the **internal web app**
- the **public careers page**

Include only the major:
- modules
- actors
- data stores

Keep the design high level, simple, and strictly aligned to MVP scope.

# Output
Return **Markdown only** with:
1. **Brief explanation** of the design, maximum **300 words**
2. **One Mermaid architecture-style diagram**

# Process
1. Read both source documents and extract only approved scope, actors, workflows, boundaries, and constraints.
2. Identify the minimum major modules required for the ATS MVP.
3. Identify the key actors, major data stores, and the main interactions among them.
4. Build the architecture for the internal web app and public careers page only.
5. Where clearly supported by the source, make the diagram more meaningful by showing:
   - system boundaries
   - core workflow paths
   - role-to-module access mapping
6. Exclude unsupported detail such as low-level schema, internal APIs, infrastructure internals, deployment design, and integrations.
7. If critical gaps prevent a reliable design, ask only those critical questions.
8. Perform a self-audit before finalizing:
   - every element is grounded in the source
   - no invented scope was added
   - the design remains simple and high level
   - the explanation stays within 300 words



# C4 Diagram

# Role
You are a senior software architect with strong expertise in C4 modeling, Mermaid syntax, and requirements-driven architecture.

# Context
Use only **"Context Final Reconciled.pdf"** and **"ATS_MVP_PRODUCT_DESIGN_DOC.md"** as the source of truth. Use architecture best practices only to structure and express the design, not to introduce unsupported scope. If the two sources conflict, identify the conflict and ask a critical clarification question before producing the final result.

# Task
Produce **one valid Mermaid C4 Container diagram** for the **ATS MVP**, focused only on the **Hiring Pipeline and Stage Tracking** slice.

# Include
Show only what directly supports this slice:
- Recruiter
- Hiring Manager
- HR Admin / Manager
- Interviewer
- ATS internal system boundary
- major internal containers relevant to pipeline and stage tracking
- relevant internal data stores
- fixed hiring pipeline
- stage tracking
- application status handling
- next action ownership
- feedback / notes
- interview tracking
- communication log / follow-up tracking
- decision / closure handling
- audit trail
- role/scope-based control boundaries

# Exclude
Do not include:
- public careers page
- infrastructure internals
- deployment nodes
- integrations
- security internals
- unrelated MVP areas
- component-level decomposition
- mixed C4 levels

# Output
Return **Markdown only** with exactly **one fenced `mermaid` code block**.
The diagram must:
- start with **`C4Container`**
- use only valid Mermaid C4 Container syntax
- use only supported constructs such as `Person`, `System_Boundary`, `Container`, `ContainerDb`, `Container_Boundary`, and `Rel`
- avoid unsupported or risky features
- be written to maximize renderability and clarity

# Process
1. Extract only the approved actors, responsibilities, workflow rules, tracked states, and data relevant to hiring pipeline and stage tracking.
2. Model the slice as a **Container-level C4 diagram**, not as a hybrid multi-level diagram.
3. Represent pipeline behavior through container names, responsibilities, and relationships rather than component decomposition.
4. Make the fixed pipeline explicit where architecturally meaningful.
5. Show control boundaries clearly:
   - Recruiter moves candidates through allowed stage transitions
   - Hiring Manager provides decision input but does not directly change stages or statuses
   - HR Admin / Manager has override rights
6. Keep the diagram fully internal.
7. Perform a self-audit before finalizing:
   - every element is grounded in the source
   - no invented scope was added
   - only Container-level C4 syntax is used
   - the result is valid Mermaid C4 and likely to render
   - exactly one Mermaid block is returned

# Audience
Write for **architects and engineers**.



