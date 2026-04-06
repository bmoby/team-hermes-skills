---
name: client-scenario-analyst-ops-stories
description: "Write internal and operational stories using the upstream discovery artifacts, actor profiles, situation catalog, and discovered features."
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [client, scenarios, operations, stories, discovery]
---

# Client Scenario Analyst — Ops Stories

Use this skill to write internal and operational end-to-end stories.

## Goal

Write many realistic stories showing how internal actors may use, manage, or struggle with the discovered features.
This analyst should generate multiple stories per important actor/profile and should favor completeness over brevity.

## Scope

Typical story areas:
- owner workflows
- manager workflows
- staff coordination
- operator handling
- dispatch / assignment
- internal validation
- overload and exception handling
- conflict handling
- recovery after mistakes

## Rules

- Work from the upstream artifacts plus actor and situation catalogs.
- Be concrete.
- Show sequence and outcome.
- Include both normal and difficult cases.
- For each important profile, write several stories rather than one token example.
- Each story must explicitly reference which existing options/features are used.
- If a story needs something that is not in the option list, write the missing option explicitly at the end of that story.
- Do not collapse everything into one generic path.

## Output format

### Histoires et scénarios côté interne / opérations
#### Story
- **Profil concerné :**
- **Situation :**
- **Déroulé :**
- **Options / fonctionnalités utilisées :**
- **Options manquantes :**
