---
name: client-scenario-story-mapping
description: "Use validated upstream artifacts to generate actor profiles, situations, and end-to-end stories through a multi-agent workflow, then consolidate them into a structured scenario map."
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [client, scenarios, stories, mapping, personas, multi-agent]
---

# Client Scenario Story Mapping

Use this skill after the upstream discovery chain has already produced:
- a validated client profile
- a sector/market summary
- a business idea list
- a technical idea / feature list

## Goal

Transform the discovered features and business ideas into a large, structured scenario document that helps:
- imagine how the solution actually behaves in real life
- group features by user-experience logic
- discover missing pieces
- discover edge cases and abusive cases
- identify weak, rarely useful, or disconnected options
- prepare later architecture, scoping, and proposal work

This skill is intentionally expansive.
It should generate many stories, not just a neat short summary.

## Core principle

Do **not** try to solve everything in one monolithic pass.
Use fresh-context subagents or equivalent separate passes with clearly separated responsibilities.

This skill should be orchestrated as a multi-agent workflow whenever possible.
A single-agent fallback is acceptable, but the preferred mode is role-based decomposition.

## Preferred role split

### Role 1 — Actor / profile builder
Create likely actors and user profiles such as:
- end customers
- premium customers
- rushed customers
- confused customers
- loyal returning customers
- dishonest or abusive customers
- elderly users
- parents with children if relevant
- internal owner / manager
- staff / operators
- partners / subcontractors if relevant

### Role 2 — Situation / behavior mapper
Create likely situations and states such as:
- best case
- normal case
- rushed case
- inattentive case
- stressed case
- aggressive case
- dishonest case
- misunderstanding
- delay
- no-show
- conflict
- overload
- outage / exception if relevant

### Role 3 — Client-facing story writer
Write end-to-end stories involving:
- discovery
- request / booking / ordering
- interaction
- issue handling
- follow-up
- completion

### Role 4 — Internal / operational story writer
Write stories involving:
- owner
- manager
- staff
- operators
- dispatch / coordination
- internal validation
- conflict handling
- overload and exceptions

### Role 5 — Consolidator
Merge everything into a final structured scenario map.
Group by logic and highlight patterns.
Do not over-compress.

## Mandatory workflow

### Step 1 — Re-read all upstream artifacts
Restate briefly:
- what the client does
- what matters in the market context
- what business ideas were identified
- what technical ideas / features were identified

### Step 2 — Build the actor catalog
Generate a broad actor list.
Include both external and internal actors.
Include normal and difficult profiles.

### Step 3 — Build the situation catalog
Generate a broad situation list.
Include:
- normal situations
- exceptional situations
- conflict situations
- dishonest behavior if relevant
- stress / urgency situations
- operational failures if relevant

### Step 4 — Write end-to-end stories
Using the actors, situations, and discovered features, write many stories.
Stories should show how pieces fit together.
They may be short or medium length, but must be concrete.

### Step 5 — Group stories by user-experience logic
Group the stories around coherent experience blocks such as:
- discovery
- reservation / order / request
- confirmation
- preparation
- service delivery
- incident handling
- follow-up
- retention
- internal handling

### Step 6 — Surface missing or weak areas
At the end, identify:
- repeated missing capabilities
- friction points appearing across many stories
- features that seem disconnected
- features that seem rarely useful

This is not a final prioritization step.
It is only a structural observation step.

## Output format

Use this structure.

### 1. Rappel court des entrées
Short synthesis of the upstream artifacts.

### 2. Profils / acteurs possibles
Bullet list.

### 3. Situations / comportements possibles
Bullet list.

### 4. Histoires et scénarios côté client
Large grouped list.

### 5. Histoires et scénarios côté interne / opérations
Large grouped list.

### 6. Regroupements par logique d’expérience
Grouped blocks showing which stories/features naturally belong together.

### 7. Zones faibles, manques ou options peu utilisées
Structured observations only.

## Writing rules

- Write in French if the user speaks French.
- Be concrete.
- Prefer realistic stories over abstract theory.
- Use the discovered features as material, not as a checklist to force everywhere.
- Include both normal and difficult cases.
- Allow long output if needed.
- Do not jump into technical architecture or prioritization yet.

## Pitfalls to avoid

- generating only happy-path stories
- forgetting internal actors
- forgetting abusive or difficult behaviors
- writing vague stories with no real sequence
- collapsing everything into one generic narrative
- over-prioritizing or over-pruning at this stage

## Specialist modules

If useful, load and follow these specialist skills:
- `client-scenario-analyst-actors`
- `client-scenario-analyst-situations`
- `client-scenario-analyst-client-stories`
- `client-scenario-analyst-ops-stories`

## Template file

If needed, load `templates/scenario-story-map-fr.md` and fill it from the scenario work.
