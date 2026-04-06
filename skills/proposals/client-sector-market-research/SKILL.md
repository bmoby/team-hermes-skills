---
name: client-sector-market-research
description: "Use a validated client profile to research the client's sector and market context, then produce a short, current, useful synthesis for later business and technical exploration."
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [client, sector, market, research, discovery, context]
---

# Client Sector Market Research

Use this skill after the client profile has already been created and validated.

## Goal

Take a validated client profile and produce a short, useful, current sector/market synthesis that will help the next steps:
- business idea discovery
- technical idea discovery
- proposal work

This skill is not for writing a full market study.
It is for collecting, summarizing, and structuring practical context information that improves the quality of later reasoning.
It must stay neutral and should not give business advice, solution recommendations, or scope recommendations.

## Input

The expected input is a validated client profile containing at least:
- business activity
- target customers
- current operations
- important constraints
- what the client wants to improve

If the profile is too weak, unclear, or incomplete, the agent should say so and recommend finishing intake first.

## Core principle

Research only what is useful for better downstream thinking.
Avoid generic filler.
Avoid giant academic summaries.
Avoid weak trend lists with no impact on the client.

The result should help answer:
- what matters in this sector right now?
- what do customers expect?
- what practices are common or rising?
- what useful patterns should we keep in mind for this client?

## Mandatory workflow

### Step 1 — Restate the client context briefly
Before research, summarize:
- business type
- target audience
- positioning if known
- current operating model
- improvement intent

### Step 2 — Research the relevant sector and local market context
Look for useful, current context such as:
- customer expectations
- common digital practices
- common service patterns
- competitive pressures
- local market habits if relevant
- premium vs mass-market norms if relevant
- operational realities of the sector

### Step 3 — Extract only useful findings
Keep only findings that can help later reasoning.
Good findings are things that may influence later analysis, but this skill must not itself recommend what to do next.

### Step 4 — Separate facts from assumptions
If something is strongly supported by current sector patterns, say so clearly.
If something is a reasonable inference rather than a confirmed fact about this exact client, mark it accordingly.

### Step 5 — Produce a reusable synthesis document
The final output should be concise and reusable by later skills or agents.
It should work as a clean intermediate artifact.
It should collect and structure context, not interpret strategy or recommend actions.

## Output format

Use this structure.

### 1. Rappel court du client
Very short summary of the input profile.

### 2. Contexte secteur / marché utile
Bullet list of the most useful current context points.

### 3. Attentes clients probables
Bullet list.

### 4. Pratiques actuelles pertinentes observées
Bullet list.

### 5. Contraintes ou réalités du marché à garder en tête
Bullet list.

### 6. Éléments de contexte à transmettre
Short list of structured context elements that may be reused later, without advice or recommendations.

## Writing rules

- Write in French if the user speaks French.
- Be concise and practical.
- Prefer useful observations over broad commentary.
- Do not produce a full competitor report unless explicitly asked.
- Do not jump into detailed solution design yet.
- Keep the document reusable as input for the next step.
- Do not give advice, arbitrage, or recommendations at this stage.
- Avoid formulations such as "il faut", "on devrait", "le vrai levier", or "commencer par".

## Pitfalls to avoid

- writing a long generic market overview
- adding irrelevant trend buzzwords
- drifting into proposal writing too early
- confusing sector patterns with confirmed client facts
- producing a summary too vague to help the next step
- slipping into business advice or solution guidance

## Deliverable options

Depending on the request, produce one of:
- sector/market context summary only
- sector/market summary + current customer expectations
- sector/market summary + useful notes for later idea discovery

## Template file

If needed, load `templates/sector-market-summary-fr.md` and fill it from the research work.
