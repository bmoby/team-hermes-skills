---
name: client-intake-profile-check
description: "Turn raw client notes into a harmonized client profile, detect missing mandatory information, and decide whether there is enough information to continue toward research and proposal work."
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [client, intake, discovery, profile, qualification, proposal]
---

# Client Intake Profile Check

Use this skill when the user gives raw client information and wants a first structured output before research, solution design, or commercial proposal work.

The input can be:
- messy notes
- WhatsApp exports
- meeting notes
- questionnaire answers
- voice transcript summaries
- copied website text
- mixed facts collected over time

## Goal

Transform raw input into:
1. a **harmonized client profile**
2. a **completeness diagnosis**
3. a clear decision on whether we can continue toward research / solution design / proposal drafting

This skill exists to avoid starting from vague information and producing low-quality proposals.

## Core principle

Do **not** jump to solution design too early.
First create a reliable client profile.
Then check whether the mandatory information is present.
Only after that should the agent continue toward research, automation ideas, website ideas, AI agents, bots, or proposal drafting.

## What this skill must produce

The deliverable must always contain:
- a normalized client profile
- mandatory information already known
- mandatory information missing
- useful but non-blocking missing information
- optional information
- explicit assumptions if any
- a verdict:
  - **READY**
  - **READY WITH ASSUMPTIONS**
  - **BLOCKED**
- a recommended next action
- if information is missing: a **minimal question set** to ask the client
- a clear note that the **human decides** whether to:
  - continue immediately
  - ask the missing questions first

## Universal mandatory information

These are the minimum information blocks required across almost any domain.
If one of these blocks is too weak or absent, the skill should mark it clearly.

### 1. Activity identity
Mandatory:
- company / project name if known
- main activity
- main offer / what they actually sell
- target market or geographic context if known

### 2. Target customer
Mandatory:
- who they sell to
- B2B / B2C / mixed if known
- main customer segment

### 3. Main business objective
Mandatory:
- what they want to improve now
- top priority if identifiable

Examples:
- get more leads
- increase bookings
- reduce admin time
- improve follow-up
- improve customer support
- structure operations

### 4. Current way of operating
Mandatory:
- how requests arrive today
- how work is processed today
- which people/roles are involved if known
- tools/channels already used if known

### 5. Current frictions
Mandatory:
- key problems
- major bottlenecks
- major manual pain points
- lost opportunities / slow response / errors if identified

### 6. Expected scope or improvement area
Mandatory:
- what the client asked for or seems to want
- which area is in scope now
- whether this is a new setup or an improvement of existing tools if known

### 7. Constraints
Mandatory when known, otherwise strongly flag as missing if they are likely critical:
- budget level or ambition level
- timing / urgency
- channel constraints
- language constraints
- human constraints (small team, low technical maturity, need human validation, etc.)

## Useful information (good to know, but not always blocking)

- existing website / social presence
- current CRM / spreadsheet / booking tools
- service list details
- pricing model
- volume estimates
- team size
- brand positioning
- competitor references
- internal approval process
- preferred communication channels

## Optional information

- detailed feature wishes
- preferred technical stack
- exact design preferences
- wording / tone preferences
- deep branding material
- advanced reporting wishes
- long-term roadmap ideas

## Blocking rules

The skill must classify the case into one of three states.

### READY
Use this when:
- the mandatory blocks are sufficiently filled
- missing items are minor or non-blocking
- a first research / automation / proposal phase can begin responsibly

### READY WITH ASSUMPTIONS
Use this when:
- some mandatory information is partial
- but we can continue if we clearly separate:
  - confirmed facts
  - assumptions
  - open questions

### BLOCKED
Use this when one or more critical points are missing and prevent serious work.

Typical blockers:
- we do not really understand what the business sells
- we do not know who the target customer is
- we do not know the main business objective
- we do not understand the current workflow at all
- we do not know the main operational pain points
- we do not know what the client wants to improve first

## Mandatory workflow

### Step 1 — Normalize the raw input
Extract the raw material into structured fields.
Do not preserve the disorder of the source.
Rewrite clearly.
Merge duplicate facts.
Resolve obvious wording inconsistencies.

### Step 2 — Build the harmonized client profile
Always create a profile with the following sections:
- identity
- offer
- target customers
- business objective
- current operations
- tools/channels in use
- frictions / pain points
- expected scope
- constraints
- digital maturity

If some fields are unknown, mark them explicitly as:
- unknown
- unclear
- partially known

### Step 3 — Separate fact vs assumption
Always distinguish:
- **confirmed facts**
- **reasonable assumptions**
- **open questions**

Never present assumptions as confirmed information.

### Step 4 — Diagnose completeness
Classify each missing item into one of these groups:
- **mandatory missing**
- **useful missing**
- **optional missing**

### Step 5 — Decide if the process can continue
Return exactly one verdict:
- READY
- READY WITH ASSUMPTIONS
- BLOCKED

### Step 6 — Generate the minimum question set when information is missing
If any important information is missing, the skill must generate a short, targeted list of questions.
Do not ask a giant questionnaire.
Ask only the smallest set of missing information needed to unblock the next phase or improve reliability.

The question set must:
- be prioritized
- focus first on blocking information
- be grouped in a way that a human can easily copy/send to the client
- avoid asking for information already known

### Step 7 — Leave the final decision to the human
The skill must not decide alone whether to continue immediately or to pause for clarification.
It must instead provide a recommendation.

The final output should make clear that the human can choose between:
- **continue now** using the current information
- **ask the client the missing questions first**

## Output format

Use this structure.

### 1. Profil client harmonisé
A structured profile based on the template.

### 2. Informations confirmées
Bullet list of strong confirmed facts.

### 3. Hypothèses raisonnables
Only if needed.

### 4. Informations manquantes
Split into:
- obligatoires
- utiles
- facultatives

### 5. Verdict de complétude
One of:
- READY
- READY WITH ASSUMPTIONS
- BLOCKED

### 6. Questions minimales à poser au client
Include this section whenever anything important is missing.
The questions must be:
- short
- specific
- directly usable by the human
- limited to what is necessary

### 7. Prochaine action recommandée
Examples:
- lancer la recherche
- lancer une réflexion V1
- demander 4 informations bloquantes
- passer à la préparation de proposition

### 8. Décision humaine attendue
Always end with the explicit decision point:
- **Option A — Continuer maintenant**
- **Option B — Poser d’abord les questions au client**

## Writing rules

- Be concise and operational.
- Prefer normalized business wording over copied raw notes.
- Do not hallucinate missing facts.
- Do not start proposing solutions in detail at this stage.
- If the input is weak, make the diagnosis explicit instead of compensating with invention.
- If the user provided a lot of scattered detail, synthesize it cleanly.

## Good behavior by default

- Keep the profile lean.
- Mark uncertainty clearly.
- Avoid long explanations when a missing item can be stated in one line.
- Ask only for what is needed to move forward.

## Pitfalls to avoid

- turning intake into a full proposal
- mixing current facts with future recommendations
- asking generic discovery questions without showing what is already known
- generating a huge checklist unrelated to the client context
- pretending the case is ready when the core business model is still unclear

## Deliverable options

Depending on the request, produce one of:
- client profile only
- client profile + missing info diagnosis
- client profile + unblock questions
- client profile + readiness verdict for proposal work

## Template file

If needed, load `templates/client-profile-template-fr.md` and fill it from the raw input.
