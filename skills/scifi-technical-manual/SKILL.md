---
name: scifi-technical-manual
description: >
  Create complete in-universe technical manuals for science fiction franchises:
  fleet doctrine, starship spec sheets, threat dossiers, hazard bestiaries, and
  appendices. Follows the house format proven across a 21-volume reference
  library. Use when asked to write a sci-fi technical manual, series bible,
  ship recognition guide, or faction dossier collection.
license: MIT
metadata:
  version: "1.0.0"
  tags: [writing, science-fiction, worldbuilding, technical-manuals]
---

# Sci-Fi Technical Manual — Authoring Skill

Produce a complete, internally consistent technical manual for a science
franchise: written as if it were an internal document of that universe,
consolidating established canon with honestly marked extrapolation.

## The Contract

Every volume follows one structure. Adapt titles to the franchise; never drop
a part.

| Part | Content |
|---|---|
| Front matter | Title, edition pin (exact in-universe moment), conventions table |
| PART ONE | Strategic theater: situation table, consolidated timeline, powers assessment, **status quo snapshot** |
| PART TWO | Central installation/ship deep-dive: overview spec table, ASCII schematic, systems-by-station tables, command systems, power deep-dive, defenses, propulsion, sensors/comms, environment, medical, emergency ops |
| PART THREE | Travel/network operations doctrine |
| PART FOUR | VESSELS: full spec table per hull class (friendly and hostile), doctrine notes |
| PART FIVE | Weapons & equipment, incl. strategic materials |
| PART SIX | THREAT DOSSIERS: biology/society/tactics/engagement-rules per faction |
| PART SEVEN | Command org chart (ASCII) + personnel policies |
| PART EIGHT | BESTIARY: 6–12 phenomena, each as What / Where / Cost of contact |
| APPENDICES A–D | Glossary · Units/travel times · Canon discrepancy log · Alphabetical index |

Optional (Okuda/Sternbach tradition): a **Technical Memoranda** appendix of short essays on the franchise's most misunderstood system ("The Transporter: Once And For All" style), and a **speed/time conversion chart** in Appendix B whenever the setting has an FTL scale.

## Honesty Markers

- Unmarked = broadcast/game/book canon.
- **[E]** = engineering extrapolation where canon was silent. Consistent;
  refined never casually contradicted.
- **[W]** = writer's latitude note: how hard the rule binds future stories.
- Where the manual conflicts with source material, source wins; log it in
  Appendix C.

## Depth Rules

1. Depth comes from **canon coverage breadth**, not invented detail. Cover
   more real objects/factions/systems before elaborating existing ones.
2. If canon is silent on a number, either pin it as **[E]** once or state
   "canon does not specify." Never fabricate specs presented as fact.
3. Every miracle bills somewhere: each capability needs a cost, limit, or
   liability recorded beside it.
4. Systems get "systems-by-station" tables; vessels get full spec sheets with
   a doctrine paragraph; threats get engagement rules.
5. Voice variants are allowed (corporate PR, propaganda, liturgical) when the
   franchise warrants; flag the variant in the front matter.

## Research Pass (before writing)

1. Verify contested dimensions/stats against wiki sources; record which
   figures are production-verified vs fan-derived.
2. List every technology/faction/phenomenon from episodes/games/books; diff
   against planned coverage; gaps become sections.
3. Note contradictions between sources; resolve in Appendix C with a ruling.

## Prose Rules (anti-AI-writing)

- Zero em dashes in prose (tables may keep them in cells; bolded list leads
  excepted).
- Sentence case for subheadings below the volume title.
- No Tier-1 vocabulary: delve, robust, comprehensive, leverage, seamless,
  pivotal, showcase, intricate, realm, landscape-as-metaphor.
- No rule-of-three padding; no copula avoidance (use "is"/"has"); vary
  paragraph length; no generic conclusions.
- Clinical or in-universe voices still follow these rules; the voice lives in
  word choice, not in AI tells.

## Recognition Plate Pipeline

End the manual with an HTML comment:

```
<!-- PLATE-DATA
Name|Length_m|canon_or_E|style(dart|boxy|disc|organic|arrowhead|saucer|spider)
...5–9 rows...
-->
```

A matplotlib builder parses this block and renders a to-scale silhouette
plate per volume.

## Assembly Pipeline

For long outputs, write numbered chunk files, then concatenate with UTF-8
(no-BOM) and strip any build sentinels. Verify: section count, sentinel scan,
EOF check, detector score (avoid-ai-writing engine).

## Quality Bar

- Spec table density: every vessel and major system has one.
- Threat dossiers end in engagement rules.
- Appendix D indexes ~50+ entries for full-size volumes.
- Believability over consistency-with-nothing: if a new capability is needed,
  ask what it costs before explaining how it works.
