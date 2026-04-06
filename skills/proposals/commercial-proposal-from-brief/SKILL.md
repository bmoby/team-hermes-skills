---
name: commercial-proposal-from-brief
description: "Build a structured commercial proposal from a raw client brief, following the narrative and sales style of the TSARAG VTC proposal: what we understood, what we propose, how it works, key features, operational view, and next steps."
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [proposal, sales, commercial, brief, discovery, offer, VTC]
---

# Commercial Proposal From Brief

Use this skill when the user provides a messy discovery brief, questionnaire answers, call notes, or a PDF example and wants a **clean commercial proposal** in the same spirit as the TSARAG VTC proposal.

## Goal

Transform raw discovery material into a proposal that:
- sounds clear, credible, and commercial
- shows that we understood the client
- maps pain points → solution
- explains the customer/admin/operator flows simply
- lists key features without fake precision
- ends with a clear next-step process

## Default style

Unless the user asks otherwise:
- write in **French** if the user speaks French
- keep the structure compact and business-ready
- prefer **simple / lean V1** over bloated scope
- do **not** invent pricing certainty or fake technical certainty that the brief does not support
- when the brief is sparse, you may still propose a **strong recommended scope** based on the business type, as long as you clearly separate **confirmed facts**, **recommended features**, and **open questions**
- explicitly separate **confirmed facts**, **reasonable assumptions**, and **open questions**

## Important correction — sparse briefs still require proactive solution design

If the brief is minimal (example: sector + team size + existing tool), do **not** stay too generic.
You should infer a credible commercial proposal from the business model and propose concrete, high-value features that are well-adapted to that sector.

Example for a high-end restaurant:
- online table reservation
- reservation confirmations and reminders
- Telegram / WhatsApp concierge-style reservation bot
- elegant website with menu, events, private dining, gallery, contact
- QR code menu
- review / feedback flows
- CRM-style guest notes and VIP preferences
- internal notifications for reservations, cancellations, special requests
- lead capture for events and private bookings
- multilingual experience if relevant

Rule:
- be concrete enough to be commercially compelling
- but mark unconfirmed items as **recommandé**, **option**, or **à confirmer** instead of presenting them as already requested facts

## Source model to imitate

The reference proposal has this logic:
1. Cover / title
2. What we understood + what we propose
3. How it works (client / operator journeys)
4. Key features
5. Operational view or concrete interface/process example
6. Process and next steps

Do **not** copy wording mechanically. Recreate the structure and selling logic from the brief.

## Mandatory workflow

### Step 1 — Extract the brief

Turn the raw input into these buckets:
- company / business model
- current operations
- online presence
- offers / services
- pricing model
- booking flow
- tools currently used
- team / roles
- main pain points
- missing information / unanswered questions

### Step 2 — Challenge scope first

Before drafting, identify the **simplest credible offer**.

Always ask internally:
- what is the leanest version that creates visible value fast?
- what should stay manual in V1?
- what is attractive in sales language but risky in delivery?

If the raw idea is too large, the proposal should still present a coherent solution, but phrased as:
- **V1 included**
- **optional next phase**
- **to clarify before commitment**

### Step 3 — Build the proposal around business problems

Write the proposal as a mapping:
- current friction
- proposed improvement
- expected operational benefit

Strong pattern:
- “Aujourd’hui … / Demain …”
- “Problème / Solution proposée / Impact”
- “Ce que nous avons compris / Ce que nous mettons en place”

### Step 4 — Write concrete usage flows

Always include the main journeys in simple language, for example:
- client books via website
- client books via Telegram / WhatsApp / form
- dispatcher/admin manages requests
- operator/driver/provider receives and confirms jobs

The goal is clarity, not exhaustive specs.

### Step 5 — List features with discipline

Include only features supported by the brief or clearly marked assumptions.

Feature lists should be grouped by theme, for example:
- website / visibility
- booking / qualification
- admin operations
- automation / notifications
- payment / invoicing
- multilingual / support

If something is uncertain, mark it:
- **À confirmer**
- **Selon l’outil retenu**
- **Option phase 2**

### Step 6 — End with next steps

Finish with a short delivery path, usually:
1. cadrage détaillé
2. validation du périmètre / design
3. production
4. lancement / prise en main

If pricing/timeline are unknown, say so clearly instead of guessing.

## Recommended output format

Use this skeleton.

### 1. Title block
- proposal title
- client/activity
- region/context
- format of the solution

### 2. Ce que nous avons compris / ce que nous proposons
A short intro + a table or bullets mapping:
- current state
- proposed response

### 3. Fonctionnement proposé
Mini user journeys:
- prospect/client
- internal team/admin
- field operator / driver / partner

### 4. Fonctionnalités clés
Grouped bullets or a compact matrix.

### 5. Vision opérationnelle
A concrete example of how the system is used day to day:
- calendar
- request dispatching
- notifications
- booking follow-up
- complaint handling

### 6. Points à clarifier
Always include this section if the brief has gaps.

### 7. Prochaines étapes
3 to 5 short steps.

## Writing rules

- Use short paragraphs.
- Prefer operational language over buzzwords.
- Sell outcomes, not technical vanity.
- Avoid overcommitting on AI.
- Avoid fake numbers, fake ROI, fake deadlines.
- If the brief is incomplete, do not hide it.
- When useful, mention that the final technical stack/payment provider/tooling will be chosen during cadrage.

## Good phrasing patterns

- “Nous avons compris que…”
- “Aujourd’hui, … ; demain, …”
- “L’objectif n’est pas d’automatiser pour automatiser, mais de…”
- “La version initiale peut rester simple sur … afin de lancer rapidement.”
- “Ce point reste à confirmer avant chiffrage définitif.”

## Pitfalls to avoid

- turning the proposal into a technical specification
- inventing detailed automations absent from the brief
- promising full autonomy where human validation is still needed
- mixing confirmed facts and assumptions
- writing a giant feature dump with no business narrative

## If the user asks for a proposal “like the PDF”

Reproduce the **structure and persuasion logic**, not the exact copy.
Use the PDF as a style reference for:
- section order
- concise business framing
- customer/admin/operator journeys
- feature grouping
- simple next-step close

## Deliverable options

Depending on the request, produce one of:
- clean chat-ready proposal text
- markdown proposal
- proposal + “questions ouvertes” appendix
- proposal + ultra-lean V1 / phase 2 split

## Template file

If needed, load `templates/proposal-template-fr.md` from this skill and fill it from the brief.
