# Paper Discovery and Screening

## Goal

Find papers that are strongly tied to the user's topic, not merely papers that share a method keyword.

The workflow is:

1. Parse the topic
2. Build search terms
3. Collect candidates
4. Grade relevance
5. Keep only the papers needed for the review

## Parse the Topic

Extract these items first:

1. Domain or application scene
2. Research object
3. Target task
4. Key variable or output
5. Method path the user cares about
6. What must be excluded

Example abstraction:

- Domain: mineral processing
- Object: grinding process
- Task: soft sensing
- Target variable: particle size
- Method path: shallow ML -> ensemble learning -> temporal deep learning -> hybrid model
- Exclude: control, platform, diagnosis

## Build Search Terms

Build search terms in four rings.

### Ring 1: Exact-topic terms

Combine object + task + target variable.

Examples:

- `grinding particle size soft sensor`
- `磨矿 粒度 软测量`
- `overflow particle size soft sensor`

### Ring 2: Topic + method-family terms

Combine the exact topic with relevant method families.

Examples:

- `grinding particle size soft sensor SVM`
- `磨矿 粒度 软测量 神经网络`
- `grinding particle size prediction LSTM`

### Ring 3: Adjacent but still on-topic terms

Use when exact-topic results are sparse.

Examples:

- expand from one process unit to its direct upstream or downstream measurement task
- expand from one ore type to closely related ore-processing scenes
- expand from soft sensing of one target variable to prediction of the same variable

### Ring 4: Method-chain completion terms

Use only when the review needs a missing link in the technical chain.

Examples:

- a recurrent model paper in the same process family
- a hybrid model paper that explains how two method families are combined

Do not use Ring 4 to flood the review with loosely related method papers.

## Candidate Grading

Grade each paper into one of four buckets.

### Strong

Keep by default.

Conditions:

- directly matches the topic, object, task, or target variable
- or is one of the few clearly relevant papers for the topic's exact research question

### Medium

Keep only if needed.

Conditions:

- not an exact match to the object, but closely supports the topic's method chain
- helps fill a missing transition in the review
- still shares the same kind of task rather than merely the same method name

### Weak

Normally drop.

Conditions:

- overlaps only in method name
- application object differs too much
- useful only as distant background

### Exclude

Drop.

Common reasons:

- mainly about control rather than measurement or prediction
- mainly about optimization, diagnosis, scheduling, system design, or platform construction
- uses the same algorithm name but solves another task
- cannot verify bibliographic facts

## Inclusion Rules

Include a paper when at least one of these is true:

- it directly studies the user's target task
- it solves a contradiction central to the user's topic
- it fills an essential transition in the method chain
- it is needed to explain why the user's method choice is reasonable

## Exclusion Rules

Exclude a paper when one or more of these is true:

- it is outside the user's task boundary
- it is only loosely related through a shared buzzword
- its conclusion cannot be checked from reliable source pages
- it would cause the review to drift away from the topic

## Source Preference

Prefer sources in this order:

1. publisher or journal page
2. DOI page
3. conference proceedings page
4. thesis repository or university repository
5. reputable indexing page when primary source metadata is hard to access

Before using a paper, verify:

- title
- author list
- year
- venue
- pages or article number when available
- DOI or stable URL when available

## Compact Screening Output Template

Use this format when the user asks to search or screen papers:

`检索焦点：……`

`纳入标准：……`

`排除标准：……`

`强相关文献：`

- `[作者, 年份] 相关原因；在综述中的作用。`

`中相关文献：`

- `[作者, 年份] 补充哪一段方法链；为什么不是强相关。`

`排除方向：`

- `控制类研究：与当前测量/预测任务不一致。`
- `仅方法同名但任务不同的论文：会造成跑题。`

## Writing Hand-off

After screening, write the review only from the kept papers.

When the paper is medium rather than strong, do not present it as if it were a direct study of the user's exact topic. State its supporting role honestly.
