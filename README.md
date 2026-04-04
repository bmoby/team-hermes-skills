# Team Hermes Skills

Shared repository for team-approved Hermes Agent skills.

## Purpose

This repo is the lightweight V0 workflow for sharing and evolving Hermes skills without modifying Hermes itself.

## Operating model

- `skills/canonical/` = validated skills the team can actually use
- `skills/proposals/` = new skills or major revisions under review
- `experiences/` = short usage feedback linked to a canonical skill
- `templates/` = reusable templates for creating skills and experiences

## Workflow

1. Create or improve a skill locally.
2. Open a PR into `skills/proposals/` for a new skill or major rewrite.
3. Review as a team.
4. Once approved, move or merge it into `skills/canonical/`.
5. After real usage, add short reports under `experiences/<skill-name>/`.
6. When repeated experiences converge, update the canonical skill via PR.

## Ground rules

- Do not edit canonical skills directly on `main`.
- Do not dump whole transcripts into `experiences/`.
- Keep experience notes short, factual, and reusable.
- Prefer a stable canonical skill plus small templates over giant monoliths.
- No scoring system in V0.
