---
name: client-scenario-analyst-client-stories
description: "Write client-facing end-to-end stories using the upstream discovery artifacts, actor profiles, situation catalog, and discovered features."
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [client, scenarios, stories, journeys, discovery]
---

# Client Scenario Analyst — Client Stories

Use this skill to write client-facing end-to-end stories.

## Goal

Write many realistic stories showing how the discovered features may be used by external users.
This analyst should generate multiple stories per important actor/profile and should favor completeness over brevity.

## Scope

Typical story areas:
- discovery
- request / booking / ordering
- confirmation
- follow-up
- issue handling
- completion
- return usage / loyalty

## Rules

- Work from the upstream artifacts plus actor and situation catalogs.
- Be concrete.
- Show sequence and outcome.
- Include both normal and difficult cases.
- For each important profile, write several stories rather than one token example.
- Each story must explicitly reference which existing options/features are used.
- If a story needs something that is not in the option list, write the missing option explicitly at the end of that story.
- Do not collapse everything into one generic happy path.

## Output format

### Histoires et scénarios côté client
#### Story
- **Profil concerné :**
- **Situation :**
- **Déroulé :**
- **Options / fonctionnalités utilisées :**
- **Options manquantes :**
