# Writing Template

## Default Structure

Use this structure unless the user requests another one:

1. 国外研究现状
2. 国内研究现状
3. 总结与本文切入点

The organizing logic inside each section can be:

- By technical evolution
- By time evolution
- By problem chain

Pick the one that best explains the topic itself. Do not force all three at once.

## Before Writing

Lock these five items first:

1. Topic
2. Research object
3. Core task or target variable
4. Main contradiction
5. The user's intended method path

If any sentence stops serving these five items, cut it.

## Per-Paper Sentence Patterns

### Pattern A: Do what + solve what problem

`[作者]围绕[对象/任务]，采用[方法]建立[模型/框架]，主要针对[实际问题]展开研究。`

`该研究的重点在于[具体改进点]，从而缓解了[测量滞后/小样本/强噪声/非线性耦合/时滞/工况波动等具体问题]。`

### Pattern B: Do what + limitation + later improvement

`[作者]采用[方法]对[对象/任务]进行建模，较好描述了[某一方面]。`

`但该研究在[时序表达/鲁棒性/泛化性/可解释性/工况迁移等]方面仍存在不足，随后[后续作者]通过[改进方法]对这一问题进行了完善。`

### Pattern C: Suitable when the paper's conclusion is modest

`[作者]将[方法]引入[对象/任务]，其意义主要在于为[具体问题]提供了可行的数据驱动建模思路。`

`不过，该研究对[另一关键矛盾]讨论较少，因此其适用范围仍受[数据条件/工况变化/变量选择]限制。`

## Transition Patterns

### From early methods to later methods

`随着[数据条件/建模需求/工况复杂性]的变化，相关研究逐步由[前一类方法]转向[后一类方法]。`

`与前期方法相比，后续研究更关注[具体问题]。`

### Between papers

`在此基础上，[作者]进一步……`

`相较于前述研究，该工作重点解决了……`

`这一研究改善了……，但在……方面仍留有不足。`

Avoid transitions that claim a field has "entered a new stage" unless the source explicitly supports that.

## Summary Template

`综上，现有研究已从[方法链条A]逐步扩展到[方法链条B]。`

`已有成果在[具体方面]取得了一定进展，但对于[更具体的矛盾1]、[更具体的矛盾2]和[更具体的矛盾3]仍缺乏兼顾。`

`基于此，本文考虑采用[方法1]处理[哪一类问题]，并结合[方法2]刻画[哪一类动态/结构特征]，以提升[目标任务]在[具体工况]下的[精度/稳定性/鲁棒性]。`

## Example of a Good Closing Logic

Do this:

`传统浅层模型对复杂非线性具有一定刻画能力，但对长时序动态依赖表达不足；单一时序神经网络虽能表征动态过程，但在小样本和强噪声条件下鲁棒性有限。因此，本文考虑将前者用于稳定提取非线性关系，将后者用于刻画时间依赖。`

Do not do this:

`因此本文方法更加先进，具有重要理论意义和应用前景。`
