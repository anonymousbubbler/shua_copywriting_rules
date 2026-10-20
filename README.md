# Shua Copywriting Rules

Turn a rough idea or draft into clearer, stronger copy without losing your voice.

A reusable AI skill for posts, newsletters, captions, and short business writing. It combines sourced advice from **Sam Parr, Shaan Puri, and My First Million** with **No AI Slop**, plain-language editing, structure and flow checks, and research of public claims.

## What you get

- A stronger rewrite that keeps your meaning and voice.
- Original and rewritten scores using the same eight-part rubric.
- Simpler wording and better paragraph order built into the rewrite.
- Specific titles that tell readers what the copy is about.
- One clear version of each point, with repeated ideas combined and useful details preserved.
- Checks for generic AI phrasing, repetition, weak openings, and unsupported claims.
- Linked findings for public facts when browsing is available.
- A final editing review before the rewrite is returned.

The default output puts the **rewrite and its new score first**, followed by the scorecard. Changes are made in the copy rather than handed back as a long list of suggested edits.

## Use it

### In Codex

Clone this **new repository** into a skill folder. The command below creates a new destination and will fail if that destination already exists:

```sh
git clone https://github.com/anonymousbubbler/shua_copywriting_rules.git \
  "${CODEX_HOME:-$HOME/.codex}/skills/shua-copywriting-rules"
```

Start a new Codex chat and ask:

```text
Use $shua-copywriting-rules on this draft.
Audience: property developers.
Format: LinkedIn post.
Keep my cautious, conversational voice.
Research public claims, simplify the wording, and improve the structure.
Show the rewrite with its new score, then the original-versus-rewrite scorecard.

[Paste your draft]
```

For a rough idea, describe the point and any real facts you already have. For feedback only, say **“Review only; do not rewrite.”**

### In another AI assistant

Download the repository ZIP using GitHub's **Code → Download ZIP** menu. Give the assistant access to the extracted folder, or upload the ZIP if it supports reading archives, and ask:

```text
Read SKILL.md and the references it calls for.
Use this skill to improve the draft below.
Research public claims if browsing is available.
Give me the rewrite and its score first, then the scorecard.
Be explicit about anything you could not verify.

[Paste your draft]
```

The assistant needs access to the reference files as well as `SKILL.md`. This is a set of instructions and sources, not a hosted app or an automatic publishing service. It does not require an API key of its own; your assistant's normal usage limits and tool access apply.

## The scorecard

Each applicable criterion is assessed from 0 to 10.

| Criterion | Weight | What it checks |
|---|---:|---|
| Purpose and reader | 15% | A clear point for a recognizable reader |
| Opening and framing | 15% | A concrete reason to keep reading |
| Substance and specificity | 20% | Useful facts, examples, and reasoning |
| Structure and flow | 10% | Logical order and clear connections |
| Clarity and pace | 10% | Understandable wording and natural rhythm |
| Voice and connection | 10% | The writer's own perspective and tone |
| Payoff and next step | 10% | An earned ending; a CTA only when appropriate |
| Trust and fit | 10% | Accurate scope, honest uncertainty, and format fit |

The goal is to improve toward **92/100 or higher**, when the material supports it. Scores are editorial judgments, not predicted reach, sales, or scientific measurements. The skill must not invent facts, weaken checks, or inflate a score to reach that target. An already strong draft may need little change.

Uncommon words are not automatic failures. The skill replaces unnecessary jargon while keeping names, technical terms, qualifications, and the details readers need.

## Two firm editing rules

**Use specific titles.** A line such as “Seeing the connections. Shaping the concept.” does not tell readers what the work is. The skill replaces vague titles, headlines, and promotional subheadings with wording grounded in the actual subject, action, or takeaway. It removes optional headings that add nothing.

**Say the point once, clearly.** If a paragraph repeats an idea in several ways, the skill combines those versions into the clearest useful statement. It checks for repetition across the whole piece, including the opening and ending, while keeping distinct evidence and important caveats.

Both rules are checked before the rewrite is returned. See [structure and flow](references/structure-flow.md) for examples.

## Sources and scope

The research covers **13 selected MFM episodes and six public host sources**. It is a focused collection, not every episode or every piece of advice. Full podcast transcripts, audio, and paid course materials are not included.

- [Sourced writing principles](references/principles.md)
- [Episode notes and source links](references/episode-notes.md)
- [Research coverage](references/coverage.json)
- [Public host writing and interviews](references/host-media.json)
- [Plain-language guidance](references/plain-language.md)
- [Structure and flow](references/structure-flow.md)
- [Public claim research](references/claim-research.md)
- [Final rewrite checks](references/rewrite-gate.md)

This is an independent project, not an official MFM product or grading system.

## Credits and license

Original instructions and adaptations are provided under the [MIT license](LICENSE). Third-party materials retain their own included MIT notices. See [Third-party notices](THIRD_PARTY_NOTICES.md) for authors, pinned versions, and attribution.

No AI Slop is an editing checklist, not an AI-authorship detector. A check pass is an editorial result, not proof of authorship or a guarantee of factual accuracy.
