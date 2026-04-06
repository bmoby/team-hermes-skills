---
name: client-solution-idea-discovery
description: "Use a validated client profile to explore a wide range of solution ideas through several parallel analysis angles, then consolidate them into a broad idea list for later filtering."
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [client, discovery, ideas, solutions, orchestrator, proposal]
---

# Client Solution Idea Discovery

Use this skill after:
- the client profile has already been created and validated
- a sector/market summary has been produced
- a business idea list has been produced

## Goal

Take:
- a validated client profile
- a useful sector/market summary
- a business idea list

and generate a broad set of possible **technical** solution ideas that may later feed:
- a proposal
- a roadmap
- a feature selection phase
- a business discussion

This skill is intentionally exploratory.
Its job is **not** to filter hard, rank precisely, or decide the final scope.
Its job is to surface as many useful, plausible, or interesting technical directions as possible in response to the business ideas already identified.

## Input

The expected input is:
- a **validated client profile**
- a **sector/market summary**
- a **business idea list**

If one of these inputs is too weak, incomplete, or missing, the agent should say so and recommend completing the previous step first.

## Core principle

Do **not** over-structure the output.
Do **not** turn this into a scoring exercise.
Do **not** try to narrow down too early.

At this stage, even ideas that may later be rejected are still useful.
The objective is broad exploration with lightweight wording.

## Mandatory workflow

### Step 1 — Re-read the upstream artifacts
Before idea generation, restate in a compact way:
- the client profile
- the useful sector/market context
- the main business ideas already identified

### Step 2 — Explore several idea angles in parallel
This skill should explore ideas through several analysis angles.
The default angles are:
- web
- bots
- AI agents
- notifications
- AI image / video

Each angle can be handled by:
- a separate subagent
- a separate internal analysis pass
- or a separate reusable specialist skill

The main rule is that each angle should stay focused on its own scope and produce idea lists independently before consolidation.

### Step 3 — Generate as many relevant ideas as possible per angle
Each angle should produce a list of short idea statements.

Good format examples:
- "On pourrait créer un site vitrine premium avec réservation simplifiée pour mieux convertir les demandes."
- "On pourrait utiliser un bot WhatsApp pour préqualifier les demandes avant traitement humain."
- "On pourrait envoyer des notifications automatiques pour confirmer, relancer ou rappeler les réservations."
- "On pourrait utiliser un agent IA interne pour aider l’équipe à répondre plus vite aux questions répétitives."

Do not require heavy structure for each idea.
One sentence per idea is enough.

### Step 4 — Allow weak or uncertain ideas
Do not discard ideas too early just because they may not survive later selection.
If an idea is plausible within the scope, it can be included.
This step is for exploration, not final arbitration.

### Step 5 — Consolidate the idea lists
Merge the outputs from all angles into:
- ideas by angle
- a final combined idea list

Remove only clear duplicates.
Do not aggressively compress the result.

### Step 6 — Keep the output easy to reuse later
The final output should make it easy for a future skill or human to:
- review the ideas
- group them later
- filter them later
- turn some of them into a proposal

## Default analysis angles

### 1. Web
Explore ideas related to:
- website presence
- elegant presentation
- landing pages
- menus or catalogs
- reservation flows
- ordering flows
- request forms
- lightweight admin views
- customer-facing web experience

### 2. Bots
Explore ideas related to:
- Telegram bots
- WhatsApp bots
- Discord bots if relevant
- conversational intake
- booking support
- FAQ handling
- customer support assistance
- lead qualification through chat

### 3. AI agents
Explore ideas related to:
- internal assistants
- customer-facing AI helpers
- AI qualification flows
- AI support assistants
- operational copilots
- AI-assisted processing
- AI task routing or drafting if useful

### 4. Notifications
Explore ideas related to:
- confirmation messages
- reminders
- follow-ups
- alerts
- internal notifications
- customer notifications
- email / SMS / WhatsApp / Telegram notifications where relevant

### 5. AI image / video
Explore ideas related to:
- AI-generated visuals
- promotional assets
- menu visuals
- brand content
- short marketing videos
- content generation for visibility
- elegant visual experiences if useful for the business

## Modularity rule

This system must stay easy to extend.
If a new analysis angle is useful later, it should be easy to add a new specialist without redesigning the whole workflow.

The orchestrator should therefore treat each angle as a separate module with low dependency on the others.

## Output format

Use this structure.

### 1. Rappel court du profil client, du contexte marché et des idées métier
Short synthesis of the upstream inputs.

### 2. Idées côté web
Bullet list.

### 3. Idées côté bots
Bullet list.

### 4. Idées côté agents IA
Bullet list.

### 5. Idées côté notifications
Bullet list.

### 6. Idées côté image / vidéo IA
Bullet list.

### 7. Liste consolidée de toutes les idées
A merged list without obvious duplicates.

## Writing rules

- Keep the ideas short.
- Write in French if the user speaks French.
- Prefer useful business language over technical jargon.
- Do not over-explain.
- Do not score the ideas.
- Do not rank the ideas unless explicitly asked.
- Do not reject ideas too early.
- Do not turn the result into a proposal yet.

## Pitfalls to avoid

- filtering too early
- trying to decide the final scope at this stage
- writing mini-specifications for every idea
- overloading the output with evaluation metadata
- repeating the same idea too many times with tiny wording changes
- ignoring the validated client profile

## Deliverable options

Depending on the request, produce one of:
- idea discovery only
- idea discovery + consolidated list
- idea discovery + brief note on which angles seemed richest

## Specialist modules

If useful, load and follow these specialist skills:
- `client-idea-analyst-web`
- `client-idea-analyst-bots`
- `client-idea-analyst-ai-agents`
- `client-idea-analyst-notifications`
- `client-idea-analyst-image-video-ai`

## Template file

If needed, load `templates/solution-idea-list-fr.md` and fill it from the discovery work.
