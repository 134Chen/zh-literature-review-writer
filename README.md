# zh-literature-review-writer

A Codex skill for finding, screening, drafting, and revising Chinese literature review sections in a problem-driven style.

## What This Skill Does

This skill is designed for tasks such as:

- Writing Chinese literature reviews
- Drafting `国内外研究现状`
- Organizing `related work`
- Screening papers by relevance before writing
- Rewriting existing review sections to reduce filler and improve topic focus

Compared with generic literature-review prompts, this skill emphasizes:

- staying close to the user's exact topic
- filtering papers by actual relevance instead of keyword overlap
- explaining what each paper did and what problem it solved
- ending with a concrete research gap that supports the user's method choice
- reducing empty praise, inflated conclusions, and "AI-like" filler

## Best Use Cases

Use this skill when you want help with:

- `文献综述`
- `研究现状`
- `国内外研究进展`
- `相关研究`
- screening a paper list before writing
- turning a topic into a Chinese academic narrative

It is especially useful for:

- graduation theses
- proposals
- research reports
- related-work sections in academic papers

## Repository Structure

```text
zh-literature-review-writer/
├─ SKILL.md
├─ agents/
│  └─ openai.yaml
└─ references/
   ├─ anti-patterns.md
   ├─ paper-discovery.md
   ├─ quality-checklist.md
   └─ writing-template.md
```

## Installation

### Option 1: Manual Install

If you use local Codex skills, copy this folder into your local skills directory and keep the folder name as `zh-literature-review-writer`.

Typical local target:

```powershell
C:\Users\<YourName>\.codex\skills\zh-literature-review-writer
```

### Option 2: Install with Skills CLI

If your environment supports the Skills CLI, you can try:

```bash
npx skills add 134Chen/zh-literature-review-writer -g -y
```

If your setup expects a different install format, use the manual install method above.

## How to Trigger It

This skill is intended for requests like:

- `帮我写一段关于软测量的中文文献综述`
- `根据这些论文整理国内外研究现状`
- `先筛选这些文献，再写相关研究`
- `把这段文献综述改得更聚焦问题，不要空话`

You can also invoke it more explicitly:

```text
Use $zh-literature-review-writer to find, screen, and draft a Chinese literature review section for the topic ...
```

## Example Requests

### Example 1: Write from a Topic

```text
请用 zh-literature-review-writer 帮我写“面向工业过程软测量的多工况建模”相关的中文文献综述，
先给出检索重点和筛选标准，再输出国外研究现状、国内研究现状和总结。
```

### Example 2: Screen Papers First

```text
下面是我整理的一批论文，请先按 strong / medium / weak / exclude 分类，
说明每篇为什么保留或排除，然后再决定是否值得写成文献综述。
```

### Example 3: Rewrite an Existing Draft

```text
这是一段我已经写好的研究现状，请帮我改写。
要求保留事实和引用，不要堆方法名，不要写空泛总结，
最后要自然落到我的研究切入点上。
```

## Output Style

This skill tends to:

- keep the topic tight
- avoid drifting into unrelated broad background
- prefer fewer but more relevant papers
- explain papers through problem, method, and limitation
- end with a concrete gap statement instead of a slogan

## Notes

- This skill is optimized for Chinese academic writing.
- It works best when the user provides a clear topic, object, task, or paper list.
- It is not meant for broad, unfocused surveys full of loosely related papers.

## License

No license file is included yet. Add one if you want others to reuse or modify the repository under explicit terms.
