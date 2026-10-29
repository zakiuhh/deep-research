---
name: deep-research
description: Conducts thorough, multi-source web research with systematic searching, cross-checking, fact-checking, and a structured, cited report. Use this skill whenever the user asks for in-depth research, a deep dive, detailed analysis, a literature review, a comparison across sources, fact-checking, "research this properly", "investigate thoroughly", "analyze comprehensively", "what's the current state of X", or any question that clearly needs many searches rather than one quick lookup. Also use it for market or technology landscape scans, comparing options before a decision, and checking whether a claim is true. Do not use it for simple facts that one search can answer.
---

# Deep Research

Research like a careful analyst: plan the question, search widely, verify what matters, say how confident you are, and report clearly with sources. Do the whole job in one go, without stopping midway to ask permission.

## Workflow

### Step 1: Frame the question

Before any searching:

1. **Restate the question in one line** so the scope is clear to you (and to the user, in the report).
2. **Pick the research type**, because it changes what to look for:

| Type | What matters most |
|---|---|
| Explainer / overview | Clear structure, consensus view, key debates |
| Current state / news | Recency, latest figures, what changed lately |
| Comparison / decision | Same criteria across options, trade-offs, a clear verdict if one exists |
| Fact-check | The exact claim, original source, evidence for and against |
| Literature / evidence review | Primary studies, methods, strength of evidence, consensus |

3. **Pick the depth** from the request (default to Standard if unclear):

| Depth | When | Searches |
|---|---|---|
| Quick | Narrow question, user wants a fast answer | 3 to 5 |
| Standard | Most research requests | 6 to 10 |
| Deep | Complex, contested, high-stakes, or "be thorough" | 10 to 20 |

4. **Break it into 3 to 6 sub-questions** that together would fully answer the main question. This is your checklist for the rest of the workflow.

Only ask the user a clarifying question if the answer would change the research direction (for example, the topic has two very different meanings). Ask at most one. Otherwise state your assumptions in one line and start.

### Step 2: Map the landscape (2 to 3 searches)

Start broad to see the terrain:
- Search the main topic for an overview
- Note the key subtopics, major players, and common terms
- Spot debates or conflicting viewpoints early
- Check what's recent, since the picture may have changed

If the user mentioned their own files, company, or documents ("our", "my"), check any connected internal tools first, then the web.

### Step 3: Deep dive, one sub-question at a time

Search each sub-question separately. Combined queries return shallow results for everything.

- Keep queries short and specific, and make each one meaningfully different from the last. If a query misses, change the terms, the angle, or the source type instead of repeating it.
- Include the current year for time-sensitive topics.
- When a result looks important, **open the full page** instead of relying on the snippet. Snippets are often too thin to support a claim.
- Prefer primary sources: original studies, official data, company filings, documentation, and the original statement over articles about it.
- Follow the trail. If sources keep citing the same report, study, or person, go read that original.

### Step 4: Verify and stress-test

For every claim the conclusion depends on:

- **Confirm with 2 or more independent sources.** Check they are actually independent. Ten articles repeating one press release or one study count as one source.
- **Check dates and credibility.** Is it current? Who wrote it, and what do they gain?
- **Look for the other side on purpose.** Search for criticism, limitations, failed replications, or counter-evidence. If more than one answer could fit, test the alternatives against the most specific facts available instead of only collecting support for the one you favor.
- **Resolve conflicts if you can.** Differences often come from date, definition, method, or region. Say which and why. If you can't resolve it, report both sides and don't pick one quietly.
- **Flag the weak spots.** Mark anything single-sourced, outdated, or contested.

### Step 5: Gap check

Compare what you found against your sub-questions from Step 1:

- Is each sub-question answered with evidence you retrieved?
- Are there figures, quotes, or details you would otherwise fill in from memory? Search for them instead.
- Does anything important remain unverified?

Run targeted searches for the gaps, then stop. Don't keep searching once every part of the answer is grounded in a source. If something genuinely can't be found, say so in the report instead of padding.

### Step 6: Synthesize and deliver

Write the report using the structure below. Lead with the answer, not the process. Scale length to the depth: Quick gets a short summary, Deep gets the full structure.

## Output structure

```markdown
# [Research topic]

## Bottom line
[2 to 4 sentences: the direct answer and the main conclusion.]

## Key findings

### 1. [Clear statement of the finding]  (Confidence: High / Medium / Low)
- Evidence from [Source A]
- Supporting data from [Source B]
- Context or nuance

### 2. [Next finding]  (Confidence: ...)
- ...

## Detailed analysis

### [Subtopic 1]
[Explanation with citations]

### [Subtopic 2]
[Explanation with citations]

## Where sources disagree
[Conflicts, and what likely explains them. Omit if none.]

## Uncertainties and gaps
[What couldn't be verified, what is thin or outdated, what to watch.]

## Sources
[The sources actually used, with titles and dates where relevant.]
```

**Confidence labels:**
- **High**: several independent, credible sources agree, ideally including a primary one.
- **Medium**: credible but limited sources, or minor disagreement.
- **Low**: single source, weak sourcing, outdated, or heavily contested.

For comparisons and decisions, add a short side-by-side table on the same criteria, and say plainly which option fits which situation.

For fact-checks, start with the verdict (true, false, misleading, or unproven), then show the evidence.

## Source quality

**Strong:** peer-reviewed research, official statistics and government agencies, original documentation and filings, established news organizations, expert consensus statements.

**Use with care:** press releases (verify the claims), opinion pieces (label as perspective), company blogs (note the interest), blogs by individuals (check credentials), social media (confirm elsewhere).

**Red flags:** no author or date, no evidence behind big claims, sensational tone, a single source behind many copies, old information presented as current.

On contested political or social topics, stay even-handed. Report what each side actually says, use separate searches to cover each side fairly, and don't add your own verdict on what is genuinely disputed.

## Writing and citation rules

- **Cite the specific source for each major claim**, for example "According to [Source], ..." or "Data from [Year] shows ...". Note the date when it matters.
- **Use your own words.** Paraphrase instead of copying. If a quote is truly needed, keep it under 15 words, use at most one quote per source, and never reproduce song lyrics, poems, or long passages. Don't rebuild an article's structure point by point.
- **Separate fact from opinion.** Label perspectives as perspectives.
- **State uncertainty plainly.** "Evidence is limited" is a valid finding.
- **Never invent sources, numbers, or quotes.** If you didn't retrieve it, don't cite it.
- **Don't mention your knowledge cutoff.** Search instead, and lead with the most recent information.

## Delivering the result

- **Default:** a structured report in the chat reply.
- **If the user asks for a file** (Word, PDF, slides, spreadsheet, or a doc to share), create it, using the matching skill or tool for that format.
- For long reports in chat, end with one line offering to turn it into a document.
- Close with one short line offering a useful next step, such as going deeper on a subtopic or comparing options. Ask at most one question.

## You're done when

- The main question and every sub-question are answered with retrieved evidence
- Key claims are verified with independent sources
- Major perspectives are represented, including the counter-case
- Conflicts and gaps are stated honestly
- The user has something they can act on

## Examples

### Example 1: Standard depth, explainer

User: "Research how solid-state batteries compare to lithium-ion right now."

Approach: frame as a comparison plus current-state question at Standard depth. Sub-questions: energy density, safety, cost, charging speed, who is producing what, realistic timelines. Run a landscape search, then one search per sub-question, open the manufacturer and independent test sources, search for criticism and delays, then report with a comparison table and confidence labels (for instance, High on the safety advantage, Low on commercialization dates because sources conflict and many are company claims).

### Example 2: Fact-check

User: "Is it true that we only use 10% of our brains?"

Approach: type is fact-check, depth Quick. Search the claim's origin and the neuroscience evidence, open a primary or review source, search for why the myth persists. Lead with the verdict ("False"), then the evidence, the myth's likely origin, and sources. Short, no padding.

### Example 3: Deep, contested topic

User: "Do a deep dive on whether remote work hurts productivity."

Approach: Deep depth, evidence review. Sub-questions: large-scale studies, hybrid versus fully remote, measurement methods, differences by job type, employer versus employee findings. Search each, open the original studies, search specifically for studies that disagree, note that results depend on how productivity is measured and on the type of work, and give a balanced report where the confidence labels reflect that mixed picture. No verdict beyond what the evidence supports.
