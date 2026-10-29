<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/logo-dark.png">
    <source media="(prefers-color-scheme: light)" srcset="assets/logo-light.png">
    <img alt="Deep Research logo" src="assets/logo-light.png" width="140">
  </picture>
</p>

<h1 align="center">Deep Research</h1>

<p align="center">
  A Claude skill that does thorough, multi-source web research,
  checks the claims that matter, and delivers a clear, cited report.
</p>

---

## What it does

Ask a big question and Claude plans the research, searches each part of it separately, reads the original sources, cross-checks the important claims, and then writes up what it found, including how confident it is and where sources disagree.

It is built for questions that need more than one quick search: deep dives, comparisons, literature reviews, fact-checks, and "what's the current state of X" scans.

## How it works

| Step | What happens |
|---|---|
| **1. Frame** | Restates the question, picks the research type and depth, splits it into sub-questions |
| **2. Map** | A few broad searches to see the landscape and spot debates |
| **3. Deep dive** | One search per sub-question, full pages opened, primary sources preferred |
| **4. Verify** | Key claims confirmed by independent sources, plus a deliberate search for counter-evidence |
| **5. Gap check** | Compares findings against the sub-questions and fills what's missing |
| **6. Deliver** | A structured report with confidence labels and sources |

## Depth levels

| Depth | Best for | Searches |
|---|---|---|
| **Quick** | Narrow questions, fast answers | 3 to 5 |
| **Standard** | Most research requests | 6 to 10 |
| **Deep** | Complex, contested, or high-stakes topics | 10 to 20 |

## Features

- Plans before searching, so the research covers the whole question
- Confidence labels (High, Medium, Low) on each key finding
- Checks that sources are truly independent, not copies of one origin
- Looks for criticism and counter-evidence on purpose
- Reports conflicts between sources instead of hiding them
- Fact-check mode that opens with a clear verdict
- Comparison mode with a side-by-side table
- Paraphrases sources and keeps quotes short
- Even-handed on contested topics
- Output as a chat report by default, or a document if you ask

## Example prompts

- "Research the impact of AI on healthcare in depth"
- "Do a deep dive on whether remote work hurts productivity"
- "Compare solid-state batteries and lithium-ion right now"
- "Fact-check this claim: we only use 10% of our brains"
- "What's the current state of quantum computing? Be thorough"

## Report format

```
# Topic

## Bottom line
## Key findings          (each with a confidence label)
## Detailed analysis
## Where sources disagree
## Uncertainties and gaps
## Sources
```

## Install

### Claude (web and apps)

1. Download this repo as a ZIP (or zip the `deep-research` folder yourself). Make sure `SKILL.md` sits at the top level of the folder inside the ZIP.
2. Open Claude's settings and find the Skills section.
3. Upload the ZIP and turn the skill on.

Web search needs to be enabled in Claude for this skill to do its job.

### Claude Code

Copy the folder into your skills directory:

```bash
git clone https://github.com/zakiuhh/deep-research.git
cp -r deep-research ~/.claude/skills/
```

(Change the clone URL if your repo lives somewhere else.)

## Repo structure

```
deep-research/
├── assets/
│   ├── logo-dark.png    # for dark backgrounds
│   └── logo-light.png   # for light backgrounds
├── LICENSE
├── README.md
└── SKILL.md             # the actual skill
```

## Customizing

All the behavior lives in `SKILL.md`. Edit the depth levels, the report template, or the source-quality rules to fit your research style. Keep the `name` in the frontmatter the same as the folder name.

## License

MIT. See [LICENSE](LICENSE).
