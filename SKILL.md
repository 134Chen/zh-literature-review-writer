---
name: zh-literature-review-writer
description: Find, screen, write, or revise Chinese literature reviews, research-status chapters, domestic and foreign research progress summaries, and related work. Use when the user asks for 文献综述, 研究现状, 国内外研究进展, 相关研究, related work, or a Chinese academic synthesis of topic-specific papers.
---

# Zh Literature Review Writer

## Overview

Use this skill to find papers, screen them by topic relevance, and draft or revise Chinese academic literature review sections in a problem-driven style.

Aim for three qualities at the same time:

- Tight topic focus
- Low filler and low "AI feel"
- Concrete paper-level content rather than abstract summary verbs
- A final gap statement that genuinely supports the user's method choice

## Workflow

### 1. Lock the scope before searching or writing

- Extract the topic, research object, target task, key variable, and the contradiction the user's method is trying to solve.
- If the topic is specific, stay inside that topic and adjacent methods only.
- Do not slide from a specific topic into broad industry, policy, control, system, platform, or unrelated application discussion unless the user explicitly asks for that expansion.
- If the user provides papers, use those papers first.
- If the user does not provide papers, infer a method chain from the topic and keep the chain close to the topic itself.

### 2. Search and screen papers before drafting when needed

- If the user already provides a paper list, screen that list first instead of re-searching from scratch.
- If the user only provides a topic, generate search terms from five elements:
  1. research object
  2. target variable or task
  3. domain process
  4. core method family
  5. adjacent but still on-topic variants
- Search in layers:
  1. core exact-match papers
  2. adjacent papers that explain the method chain
  3. only then cautiously add near-neighbor papers that help fill a clear gap
- For technical questions, prioritize primary sources such as publisher pages, DOI pages, journal pages, conference proceedings, theses, and authors' institutional repositories.
- Verify title, authors, year, venue, and DOI or stable URL before relying on a paper.
- Do not keep a paper only because it uses a fashionable method. Keep it only if it is strongly tied to the topic, target task, or unresolved contradiction.
- Before drafting, classify each candidate as:
  - strong: directly matches the topic, task, or object
  - medium: does not exactly match the object but clearly supports the method chain or key contradiction
  - weak: related in method name only, with limited value for this review
  - exclude: off-topic, inflated by keywords, or mainly about control, platform, policy, diagnosis, or another task
- Prefer fewer strong papers over many loosely related papers.

### 3. Use the default structure unless the user asks otherwise

Default order:

1. 国外研究现状
2. 国内研究现状
3. 总结与本文切入点

Inside each part, use chronological or technical evolution only when it helps explain the problem chain. Do not force stage labels if the literature does not support them.

### 4. Write each paper in a problem-oriented way

For each cited work, prefer this order:

1. What concrete object, material, case, corpus, platform, event, group, or mechanism it studied
2. What it actually did to that object, such as conceptual definition, case analysis, survey, framework construction, comparative analysis, mechanism explanation, discourse analysis, or empirical test
3. What practical problem, explanatory gap, or limitation it addressed
4. If "practical problem" is not the right emphasis, replace it with what limitation remained and which later work improved it

Keep the conclusion concrete. State what was improved and in relation to what object, such as noise, delay, nonlinearity, variable coupling, sample size, operating-condition shift, or interpretability.

When rewriting a review paragraph, do not stop at "A discussed X" or "B enriched the perspective on Y". Push one level deeper and state the paper's actual content. In practice, each kept citation should answer at least two of the following:

- what object it studied
- what material, case, sample, platform, event, or corpus it used
- what question or mechanism it focused on
- what analytical path or argument it adopted
- what concrete finding, contribution, or remaining limitation it produced

If the available source only supports a coarse summary, stay at the highest verified specificity and do not invent details. In that case, explicitly write it as a background, overview, or macro discussion rather than pretending it contains fine-grained evidence.

Minimum execution rule for each kept citation:

- By default, each kept citation in the final prose must contain at least two slots:
  1. an object slot: what object, case, platform, event, group, corpus, or mechanism the paper studied
  2. a content slot: what the paper actually did, found, explained, compared, constructed, tested, or what specific issue it addressed
- If the paper is especially important to the review, prefer three slots:
  1. object
  2. action or analytical path
  3. problem addressed, finding, or remaining limitation
- If a sentence cannot satisfy at least "object + content", do not treat that citation as already written. Rewrite it until the reader can answer "this paper looked at what, and specifically did what."
- The only exception is a genuine macro background or overview paper whose available source does not support finer detail. In that case, mark it explicitly as background, overview, or policy-level discussion rather than letting it masquerade as a concrete study.

### 5. Close with a concrete method gap

- Summarize the unresolved contradiction in specific terms.
- Map the user's method components to that contradiction one by one.
- Do not end with generic lines such as "therefore this study has important significance" unless the user explicitly wants that style.

## Search and Screening Output

When the user asks to find or filter papers, produce a compact screening result before the full review when useful.

Include:

1. Search focus
2. Inclusion rules
3. Exclusion rules
4. Strong candidates
5. Medium candidates if they are needed to complete the method chain
6. Explicitly excluded directions when they are likely to cause topic drift

For each kept paper, briefly note:

- why it is relevant
- what role it will play in the review
- what concrete content from the paper should appear in the final prose
- whether it supports the topic directly or only supports the method chain

## Hard Rules

- Do not write a "author + method name"流水账.
- Do not mistake keyword overlap for topic relevance.
- Do not only say a paper proposed a method without saying what issue it addressed.
- Do not count a citation as "covered" if the sentence fails the minimum "object + content" rule.
- Do not summarize a paper only with abstract verbs such as "discussed", "analyzed", "explained", "enriched the perspective", or "provided support" unless the sentence immediately states what object, material, case, mechanism, or question that paper actually handled.
- Do not group several citations behind one vague clause if their research objects or contributions are different. Split them when needed so the reader can see what each paper actually did.
- Do not rewrite a literature review into broad labels like "macro background", "platform mechanism", or "social interaction" unless the sentence also states the concrete content that justifies that label.
- Do not present background or overview papers as if they had completed fine-grained event-level, mechanism-level, or causal analysis.
- Do not make unsupported claims such as "this proves the field has entered a mature stage" or "this marks a new stage" unless the source itself clearly supports that judgment.
- Do not exaggerate a paper's conclusion beyond its actual scope.
- Do not pad the review with empty phrases such as "has important significance", "greatly promoted development", "shows broad prospects", or "provides a new idea" without a concrete object.
- Do not define every method like a textbook. Expand the full name and abbreviation only at first mention when it helps readability.
- Do not invent predecessor-successor relations between papers. Only say one work improved another when the connection is textually supportable.
- Do not broaden from the user's topic to a larger field unless the user asks.
- Do not retain papers whose main task is control, diagnosis, optimization, platform construction, or general industrial intelligence when the user's topic is specifically about a measurement, prediction, or soft-sensing task.
- Do not read local files unless the user explicitly points to them.

## Writing Style

- Write in Chinese academic prose suitable for thesis proposals, literature review chapters, and research status sections.
- Prefer compact paragraphs instead of outline-like dumping unless the user explicitly asks for bullets.
- Keep transitions natural and restrained.
- Prefer concrete nouns and concrete problems over abstract praise.
- Let the "innovation rationale" land on a contradiction, not on a slogan.

## Final Self-Check

Before finalizing a review paragraph or rewrite, quickly check:

- Does each kept citation state at least "what it studied" and "what it concretely did"?
- If several citations are grouped together, can the reader still tell them apart by object or contribution?
- Are background papers clearly written as background rather than dressed up as detailed evidence?
- Does the gap statement follow from the reviewed papers' concrete limitations rather than from generic claims?

## Use These References

- For search term design, relevance grading, and candidate output format, read [references/paper-discovery.md](references/paper-discovery.md).
- For section skeletons and sentence patterns, read [references/writing-template.md](references/writing-template.md).
- For banned patterns and rewrite examples, read [references/anti-patterns.md](references/anti-patterns.md).
- Before finalizing, check [references/quality-checklist.md](references/quality-checklist.md).
