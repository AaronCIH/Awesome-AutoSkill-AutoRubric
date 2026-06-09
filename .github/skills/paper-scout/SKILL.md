---
name: paper-scout
description: 'Daily paper scout for Auto-Skill and Auto-Rubric research. Use when: searching for new papers on self-evolving agents, skill evolution, rubric learning, preference alignment, reward modeling, agentic evolution. Searches arxiv for latest papers, recommends noteworthy ones, and updates the Awesome-AutoSkill-AutoRubric repo README.'
argument-hint: 'Optional: specific topic focus, e.g. "rubric reward modeling" or "skill evolution benchmark"'
user-invocable: true
---

# Paper Scout: Daily Auto-Skill & Auto-Rubric Paper Finder

## When to Use

- Daily check for new papers in the Auto-Skill / Auto-Rubric domain
- When you want to update the awesome list with recent publications
- When you want a summary of noteworthy new papers on self-evolving agents or rubric learning

## Search Topics

Search arxiv for papers matching these keyword groups. Combine multiple queries to maximize coverage.

### Auto-Skill Keywords
- `"self-evolving" agent skill`
- `"skill evolution" LLM agent`
- `"skill creation" agent`
- `"skill library" agent`
- `"skill discovery" agent`
- `"agentic evolution"`
- `"self-improving" agent skill`
- `"harness evolution"`
- `"skill reuse" LLM`

### Auto-Rubric Keywords
- `"Auto-Rubric" reward`
- `"rubric" "preference" reward LLM`
- `"rubric learning" alignment`
- `"rubric-based" reward`
- `"rubric generation" LLM`
- `"criteria" "preference" reward modeling`

## Procedure

### Step 1: Search for New Papers

Search arxiv for recent papers using the keyword groups above. Use the fetch_webpage tool to query:

```
https://arxiv.org/search/?query=KEYWORDS&searchtype=all&order=-announced_date_first
```

Run multiple searches across both Auto-Skill and Auto-Rubric keyword groups. Focus on papers from the last 7-14 days.

### Step 2: Filter and Evaluate

For each candidate paper found:
1. Fetch the arxiv abstract page to get full details (title, authors, date, abstract)
2. Evaluate relevance — must be directly about:
   - Self-evolving agent skills / skill libraries / skill creation / skill evolution, OR
   - Rubric learning from preferences / rubric-based reward modeling / auto-rubric generation
3. Skip papers that only tangentially mention these topics

### Step 3: Present Recommendations

Present findings to the user in this format:

```
## New Papers Found (Date Range)

### Auto-Skill
1. **Paper Name** (arXiv:XXXX.XXXXX, Date)
   - TL;DR: One-sentence summary
   - Why it's relevant: Brief note

### Auto-Rubric
1. **Paper Name** (arXiv:XXXX.XXXXX, Date)
   - TL;DR: One-sentence summary
   - Why it's relevant: Brief note

### Verdict
- 🔥 Must-add: [list]
- 👀 Worth watching: [list]
- ⏭️ Skip: [list with reasons]
```

### Step 4: Update the Repo (upon user confirmation)

After the user confirms which papers to add:

1. Read the current README.md at `c:\Users\t-ihchen\Downloads\IHChen\Github\Awesome-AutoSkill-AutoRubric\README.md`
2. Determine the correct section for each paper:
   - **Auto-Skill > Skill Learning & Evolution**: Papers about skill creation, evolution, reuse
   - **Auto-Skill > Benchmarks & Evaluation**: Benchmarks for skill evaluation
   - **Auto-Skill > Surveys & Frameworks**: Survey papers, frameworks
   - **Auto-Rubric > Rubric Learning from Preference Data**: Papers on learning rubrics from preferences
   - **Auto-Rubric > Rubric-Guided RL & Reward Modeling**: Papers using rubrics for RL/reward
   - **Auto-Rubric > Rubric-Based Evaluation & Judges**: Papers on rubric-based evaluation
3. Insert the new entry in chronological order within the section
4. Follow the table format: `| **Name** | Date | [arXiv:ID](link) | [Code](link) or - | TL;DR |`
5. Commit and push:
   ```
   git add .
   git commit -m "Add: Paper1, Paper2, ..."
   git push
   ```

## Important Notes

- Always check if a paper is already in the README before adding
- Use the paper's v1 submission date for the "Date" column
- If a paper has a GitHub repo, include it; otherwise use `-`
- Note venue acceptance if mentioned (e.g., ICML 2026, ACL 2026)
- TL;DR should be 1-2 sentences, focusing on the key contribution
