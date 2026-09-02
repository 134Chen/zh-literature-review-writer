---
name: zh-literature-review-writer
description: Find, screen, write, or revise Chinese literature review sections, research status chapters, domestic/foreign research progress summaries, and related work. Use when the user asks for 文献综述, 研究现状, 国内外研究进展, 相关研究, related work, or wants papers for a specific topic to be searched, filtered by relevance, and reorganized into a Chinese academic narrative. First lock the topic, object, and core research problem; search close to that topic; classify papers into strong, medium, weak, or exclude; keep only papers that directly serve the topic, method chain, or unresolved contradiction; organize each kept paper around what it did and what practical problem it solved, or what limitation remained and which later work improved it; avoid unsupported stage claims, inflated conclusions, and empty filler; and end with a concrete gap statement that supports the user's method choice.
---

# Zh Literature Review Writer

## Overview

Use this skill to find papers, screen them by topic relevance, and draft or revise Chinese academic literature review sections in a problem-driven style.

Aim for three qualities at the same time:

- Tight topic focus
- Low filler and low "AI feel"
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

1. It did what
2. It solved what practical problem
3. If "practical problem" is not the right emphasis, replace it with what limitation remained and which later work improved it

Keep the conclusion concrete. State what was improved and in relation to what object, such as noise, delay, nonlinearity, variable coupling, sample size, operating-condition shift, or interpretability.

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
- whether it supports the topic directly or only supports the method chain

## Hard Rules

- Do not write a "author + method name"流水账.
- Do not mistake keyword overlap for topic relevance.
- Do not only say a paper proposed a method without saying what issue it addressed.
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
- For Chinese journal manuscripts, prefer a synthesized review paragraph: classify papers by research line, method link, or unresolved problem before naming individual authors.
- Keep each literature sentence tied to one author team or one named document. Use an uncited topic sentence to group a research direction, then give each author team its own sentence.
- Do not combine several author teams into one sentence with commas, enumeration punctuation, `分别`, or `等研究了`. Joint authors of the same cited paper count as one author team.

## Low-AI Chinese Literature Review Method

Use this section when the user asks for prose that is "不像 AI", has failed AIGC checks, or needs a thesis literature-review section to sound more like a human researcher wrote it.

### Core Move

Do not polish a literature review by adding more smooth transitions. Rebuild each paragraph around the concrete research chain:

`research object -> data or condition -> method used -> problem addressed -> remaining boundary -> relation to this study`

The paragraph does not need all six parts every time, but at least three must be concrete. If a paragraph only contains broad field labels, method names, and praise words, it will read like generated text.

### Replace Template Review Rhythm

Avoid repeating the same skeleton:

- `近年来，随着...的发展，...受到广泛关注。`
- `某某提出了...方法，取得了较好效果。`
- `该研究为...提供了参考。`
- `综上，现有研究已经取得丰富成果，但仍存在不足。`

Prefer writing from the actual research object:

- `钻机运行曲线需要先转换成工况标签，孔深累计才有阶段边界。已有研究通常从转速、钻压、泵压和深度中提取特征，用于识别钻进、循环、起下钻和静止等状态。`
- `原始高频文件中的毛刺会放大差分结果。稳健统计研究中，中位数和MAD常用于削弱短时极端值对局部趋势判断的影响。`

### Citation Sentence Discipline

- Keep one citation sentence focused on one paper, one author team, or one named document.
- Avoid stacking many citations after a generic claim. If several papers belong to the same direction, introduce that direction in a separate topic sentence, then write one sentence for each representative author team or document.
- Do not put a citation on a sentence that merely says `研究较多`, `发展较快`, `应用广泛`, or `具有重要意义`.
- If the user's school requires one reference per sentence, keep that rule even while rewriting for fluency.
- Do not place a multi-reference cluster after several unrelated names, policies, or claims. If a sentence mentions distinct authors or documents, attach each citation to the specific author, document, or claim.
- Multi-reference clusters such as `[6-8]` should be avoided in Chinese journal prose unless the user explicitly asks for compressed citation style. Write `Xiao和Wang[6]...。Jiang等[7]...。Zhang等[8]...。`, with one author team in each sentence.
- For policy and background sources, avoid a terminal cluster such as `政策背景[15-18]`; instead write the common policy line first, then separate different policy or empirical sources if they support different points.

### Chinese Journal Synthesis Paragraphs

Use this pattern when rewriting a single literature-review paragraph for Chinese journals:

1. Start with the research chain or practical problem, not with a list of authors. For example: `公共体育设施低碳可达性评价涉及设施供给、交通网络和出行替代三个环节`.
2. Group close papers at the paragraph level, not inside one citation sentence. A useful paragraph rhythm is `方向主题句 -> 作者A单独一句 -> 作者B单独一句 -> 作者C单独一句 -> 小结句`.
3. In a journal-style single paragraph, keep one author team or one named document in each sentence. For example: `在体育设施领域，相关研究主要关注服务覆盖和空间配置。Xiao和Wang[6]测算了社区体育设施服务可达性。Jiang等[7]比较了街道尺度的全民健身资源配置。Zhang等[8]解释了全国公共体育场馆的分布特征。`
4. Do not write `A[1]、B[2]、C[3]等研究了...` or `A[1]认为...，B[2]则指出...`. Rewrite them as separate sentences, even when the papers belong to the same direction or reach related conclusions.
5. Use single citations for distinct policy files, distinct named findings, or different claims. Do not write `政策背景[15-18]`; write the policy file and each empirical direction separately if they support different points.
6. When the user provides a target journal example, preserve that example's review logic: classify the literature first, cite by group where justified, then use `总体来看/综上` to state the exact unresolved issue and the present study's method route.
7. Close with a concrete gap that points to the user's method chain, such as `仍缺少把设施供需、低碳交通条件和可替代小汽车里程连续衔接的测算框架`.
8. Keep a requested single paragraph as one paragraph, but use sentence boundaries to separate author teams. One-author-team-per-sentence does not require splitting the paragraph into multiple paragraphs.

### Human-Like Paragraph Construction

For a review paragraph:

1. Start with the research problem or data condition, not a grand field background.
2. Introduce papers by what they actually did, not only by the method name.
3. Use method names only when they explain the technical route.
4. Put limitations in concrete terms: sample size, noise, delay, operating-condition shift, sensor placement, weak labels, interpretability, field deployment, or unit mismatch.
5. End with the user's need only when the connection is real. Avoid every paragraph ending with `为本文研究提供基础`.

Good paragraph rhythm can be uneven. One sentence can be data-heavy, the next can explain the boundary. Do not make every sentence the same length or every paragraph the same shape.

### Engineering Thesis Review Voice

For engineering, equipment, software platform, data acquisition, measurement, and algorithm chapters:

- Write from the field chain and data chain. Mention sensors, signals, files, windows, variables, units, stages, and results when they matter.
- Prefer `转速、钻压、泵压和深度变量用于识别钻进、循环和静止状态` over `多源数据技术推动了智能钻井发展`.
- When reviewing algorithms, explain why the method matches the data problem. For example, use `MAD适合处理短时尖峰` instead of `MAD具有良好的鲁棒性`.
- When reviewing software or platform work, connect architecture to data flow, not to broad informatization claims.

### Anti-Detection Revision Pass

After drafting or revising, run this pass:

- Remove opening phrases that could be deleted without changing meaning.
- Search for repeated endings such as `提供参考`, `奠定基础`, `提供支撑`, `具有重要意义`.
- Search for connector clusters: `此外`, `同时`, `进一步`, `因此`, `综上`.
- Search for turn-based contrast frames: `不是...而是`, `不仅...而且`, `不在于...而在于`.
- Search for paragraphs where every sentence begins with `某某等`.
- Replace broad nouns such as `体系`, `平台`, `能力`, `水平`, `价值`, `意义` with concrete objects when possible.
- If a paragraph remains too close to a previous version or detection snippet, change the sentence order and subject focus instead of swapping synonyms.

### Sub-10 AIGC Pass for Review and Thesis Sections

Use this pass when a Chinese thesis or review section has already been reduced but the detector still reports around 10%-13%.

- First compare repeated reports. If the same paragraphs are repeatedly flagged while total rate moves only slightly, treat the task as a convergence pass rather than a full rewrite.
- Do not broaden the review or add unrelated citations to dilute the score. Extra generic literature often raises the AI feel.
- For each repeated paragraph, change its job:
  - from `field background` to `specific data condition`;
  - from `paper list` to `what problem each paper handled`;
  - from `method praise` to `why the method matched the data problem`;
  - from `gap slogan` to `which sensor, sample, operating condition, label, or deployment issue remains`;
  - from `therefore this study...` to `this study needs this boundary because...`.
- Keep one paragraph as one paragraph when Word structure must be preserved. Rewrite the internal order instead of splitting it.
- If a paragraph is mostly formulas, variables, or result statistics, keep the numbers and units. Move the explanation from generic mathematical language to variable source, data window, and engineering meaning.
- When a report is already below 10%, rewrite the remaining matched paragraphs once more only for margin. Do not remove citations, tables, formulas, or result values.

### Low-AI Sentence Moves

Use these moves for stubborn review paragraphs:

- Start with the measurement or data problem, not the field trend.
- Put the cited work after the problem sentence, not before every sentence as `某某等`.
- Use fewer summary verbs: `提出`, `构建`, `实现`, `验证`, `表明`. Replace them with the actual operation, such as `用转速和钻压窗口识别钻进段` or `用中位数削弱单点尖峰`.
- Avoid ending several paragraphs with `为本文提供参考/基础/支撑`. End with a concrete boundary or need.
- Keep some unevenness. A human review can have one short boundary sentence after a longer technical sentence.

### Before/After Pattern

Weak:

`国内外学者对智能钻井工况识别进行了大量研究，提出了多种机器学习和深度学习方法，取得了良好效果，为本文研究提供了理论基础。`

Stronger:

`钻机工况识别通常依赖转速、钻压、泵压和深度等时序变量。已有研究把这些变量用于识别钻进、循环、起下钻和静止等状态，解决的是连续曲线与现场动作之间的对应问题。本文后续的阶段识别和孔深累计也需要先确定这一边界。`

Weak:

`异常检测方法能够有效提高数据质量，因此被广泛应用于工业数据处理中。`

Stronger:

`高频采集文件中的单点尖峰会直接影响差分结果。中位数和MAD一类稳健统计量适合先削弱这类短时极端值，再进入阶段识别。`

## Use These References

- For search term design, relevance grading, and candidate output format, read [references/paper-discovery.md](references/paper-discovery.md).
- For section skeletons and sentence patterns, read [references/writing-template.md](references/writing-template.md).
- For banned patterns and rewrite examples, read [references/anti-patterns.md](references/anti-patterns.md).
- Before finalizing, check [references/quality-checklist.md](references/quality-checklist.md).
