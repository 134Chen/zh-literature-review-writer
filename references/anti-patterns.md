# Anti-Patterns

## 1. Unsupported Stage Claims

Bad:

`国外研究已经进入深度智能化阶段。`

Why it fails:

- It assigns a stage label without evidence.
- It sounds broad and inflated.

Better:

`近年来开始出现基于深度学习的相关研究，但公开成果的研究对象和任务侧重并不完全一致。`

## 2. Method-Name流水账

Bad:

`A提出了SVM方法，B提出了LSTM方法，C提出了混合模型。`

Why it fails:

- It lists methods but hides the problem chain.

Better:

`A采用SVM处理小样本条件下的非线性建模问题；随后B转向LSTM，以增强对过程时序依赖的表达；C则进一步尝试融合两类模型，以兼顾非线性特征提取与动态建模。`

## 3. Empty Praise

Bad:

`该方法具有重要意义，并显著推动了该领域的发展。`

Why it fails:

- It does not say what changed.

Better:

`该方法降低了模型对人工经验选参的依赖，但在工况迁移时仍存在精度波动。`

## 4. Topic Drift

Bad:

When the topic is very specific, the review suddenly expands into policy, system architecture, control strategy, or unrelated applications.

Better:

Stay inside the topic. Expand only to adjacent methods that help explain the topic's method chain or unresolved contradiction.

## 5. Over-Defining Methods

Bad:

Large textbook-style explanations of SVM, LSTM, GRU, XGBoost, etc.

Why it fails:

- It inflates the review without improving the literature logic.

Better:

Give the full name and abbreviation at first mention when useful, then move back to the paper's problem, object, and limitation.

## 6. Invented Improvement Chains

Bad:

`后来的某文献对前文进行了改进。`

Why it fails:

- The relation may not exist in the source.

Better:

Only write a direct improvement chain when the later work clearly addresses the earlier limitation. Otherwise use a weaker transition such as:

`与前述研究相比，后续工作将关注点进一步转向……`

## 7. Generic Endings

Bad:

`因此，开展相关研究具有重要理论意义和应用价值。`

Better:

`因此，若研究对象同时存在强非线性、时滞和工况波动，则需要进一步考虑兼顾非线性特征表达与时序建模能力的融合方法。`
