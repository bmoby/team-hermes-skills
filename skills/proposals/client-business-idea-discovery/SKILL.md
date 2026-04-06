---
name: client-business-idea-discovery
description: "Use a validated client profile plus a useful sector/market summary to generate broad business ideas before moving to technical solution exploration."
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [client, business, ideas, discovery, opportunities, proposal]
---

# Client Business Idea Discovery

Use this skill after:
- the client profile has been validated
- a useful sector/market context summary has been created

## Goal

Generate a broad list of business ideas before moving to technical solutions.

At this stage, the purpose is to identify:
- what could be improved
- what could be simplified
- what could be sold better
- what could be organized better
- what could improve customer experience
- what could improve follow-up, retention, or internal execution

This skill should stay focused on **business opportunities**, not technical implementation.

## Input

The expected input is:
- a validated client profile
- a sector/market summary

If one of these is missing or weak, the agent should say so and recommend fixing that first.

## Core principle

Do not jump too early into:
- websites
- bots
- AI agents
- notifications
- technical architecture

First identify the useful **business ideas** that may deserve a technical response later.

## Mandatory workflow

### Step 1 — Re-read the client profile and market summary
Restate briefly:
- who the client is
- what they do
- what they want to improve
- what the market context suggests is important

### Step 2 — Explore business opportunities broadly
Generate a wide set of business ideas related to themes such as:
- acquisition
- conversion
- customer experience
- reservation / ordering / intake
- operations
- staff coordination
- retention / repeat business
- premiumization if relevant
- service clarity
- follow-up
- process simplification

### Step 3 — Keep the ideas non-technical
At this stage, ideas should stay at the business level.

Good examples:
- "On pourrait mieux structurer la réservation pour réduire les frictions."
- "On pourrait mieux suivre les clients récurrents pour augmenter la fidélisation."
- "On pourrait améliorer la présentation de l’offre pour mieux convertir une clientèle premium."
- "On pourrait simplifier la coordination interne pour gagner du temps au quotidien."

Avoid direct solution phrasing such as:
- build a bot
- create a website feature
- send SMS reminders

That comes later.

### Step 4 — Allow broad exploration
At this stage, even ideas that may later be rejected are still useful.
The goal is to surface possibilities, not decide the final scope.

### Step 5 — Consolidate into a reusable list
The final output should be easy to reuse for the next step of technical ideation.

## Output format

Use this structure.

### 1. Rappel court du client et du contexte marché
Short synthesis.

### 2. Idées métier
Bullet list of business ideas.

### 3. Regroupements utiles si nécessaire
Optional short grouping if several ideas cluster naturally.

### 4. Points à garder pour l’étape technique
Short notes that may help the next skill.

## Writing rules

- Write in French if the user speaks French.
- Keep ideas short.
- Stay at business level.
- Do not filter too early.
- Do not score the ideas.
- Do not over-structure.
- Do not move into detailed technical solutions.

## Pitfalls to avoid

- turning business ideas into technical features too early
- writing a mini-proposal already
- filtering out too many ideas too early
- ignoring the market context summary
- repeating the same idea many times with tiny wording differences

## Deliverable options

Depending on the request, produce one of:
- business idea list only
- business idea list + short grouping
- business idea list + notes for the next technical step

## Template file

If needed, load `templates/business-ideas-list-fr.md` and fill it from the discovery work.
