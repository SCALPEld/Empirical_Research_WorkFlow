# Review Rubric

Use this rubric to make the review sharp rather than merely descriptive. The default posture is constructive skepticism: identify what the paper proves, what it suggests but does not prove, and what remains open.

## Contribution

| Question | Strong Paper | Warning Sign |
|---|---|---|
| What is new? | Clear incremental contribution to a named literature | Only claims a new setting without new mechanism or identification |
| Why does it matter? | Links theory, institution, and measurable outcome | Motivation is policy-fashion or data availability only |
| Who should care? | Economists, finance scholars, policymakers, or practitioners can use the result | Audience is unclear |

## Literature Positioning

- Identify the closest literatures, not just broad fields.
- Explain whether the paper changes a mechanism, identifies a new causal effect, introduces new data, reconciles conflicting findings, or extends external validity.
- For VC/PE papers, check whether it speaks to fund structure, GP/LP incentives, staged financing, monitoring, governance, syndication, exits, valuation, or cross-border capital.

## Theory and Mechanism

- State the causal or theoretical chain in one sentence.
- Separate assumptions from predictions.
- Ask whether the mechanism is necessary for the results or merely consistent with them.
- For theoretical models, evaluate whether the assumptions are minimal, realistic, and tied to testable implications.
- For policy papers, ask whether the mechanism distinguishes intended effects from compliance, avoidance, substitution, and political-economy channels.

## Data, Variables, and Sample

| Dimension | Check |
|---|---|
| Data source | Is it authoritative, complete, and suitable for the research question? |
| Sample construction | Are exclusions, winsorization, matching, and missing values transparent? |
| Outcome variables | Do they measure the theoretical object or only a proxy? |
| Treatment/exposure | Is treatment timing, intensity, or eligibility measured cleanly? |
| Controls | Are controls post-treatment, bad controls, or mechanically related to outcomes? |

## Identification and Econometrics

### DID and event study

- Check treatment timing, staggered adoption, treatment-effect heterogeneity, and whether the estimator is appropriate.
- Evaluate pre-trends visually and statistically; do not treat a noisy insignificant pre-trend as proof.
- Ask whether anticipation, spillovers, or concurrent policies threaten interpretation.

### IV

- State relevance and exclusion restriction separately.
- Ask what economic behavior the instrument changes and why it affects the outcome only through the endogenous variable.
- Interpret LATE, not necessarily ATE.

### RDD

- Check manipulation around the cutoff, bandwidth sensitivity, covariate balance, and functional form.
- Confirm the estimand is local.

### Panel fixed effects and OLS

- Ask what variation identifies the coefficient after fixed effects.
- Check whether omitted time-varying factors remain plausible.
- Distinguish statistical significance from economic magnitude.

### GMM, structural, and dynamic models

- Check moment validity, weak instruments, over-identification tests, calibration targets, and parameter interpretation.
- Ask whether the model is identified by data variation or by assumptions.

## Results, Robustness, and Interpretation

- Summarize the main coefficient in sign, magnitude, and economic meaning.
- Treat robustness as evidence only when it targets a real threat.
- Separate robustness checks, mechanism tests, heterogeneity tests, and placebo tests.
- Ask whether multiple testing, specification search, or selective reporting is possible.
- Interpret null results with care; absence of significance is not proof of no effect.

## External Validity

- Identify the institutional scope: country, period, market structure, regulation, firm type, investor type.
- For China-facing implications, state what must hold for the result to transfer to China.
- For VC/PE, distinguish venture capital, growth equity, buyout, government-guided funds, corporate venture capital, and cross-border funds.

## Policy and Practice Implications

- Translate findings into policy only after stating identification limits.
- Discuss tradeoffs: efficiency vs fairness, innovation vs risk, market discipline vs state support, short-term funding vs long-term productivity.
- Avoid generic policy advice; connect recommendations to the paper's actual mechanism.

## Review Voice

- Be precise: "the design identifies..." instead of "the paper proves..." when assumptions are required.
- Be generous about what the paper does well.
- Be explicit about the one or two issues that most affect credibility.
- When proposing extensions, give feasible data and identification ideas rather than broad slogans.

## Common Failure Modes to Flag

| Failure Mode | How to Phrase It |
|---|---|
| Overclaimed causality | "这一结论依赖于...假设；原文目前更能支持相关性/局部因果解释。" |
| Weak mechanism evidence | "机制检验与主结论一致，但尚不能排除..." |
| Bad controls | "部分控制变量可能位于处理变量之后，存在吸收真实效应的风险。" |
| External validity leap | "该结果能否推广到中国市场，取决于..." |
| Policy overreach | "政策含义应限定在作者识别的制度环境内。" |

## Research Extension Prompts

- What new dataset would directly observe the mechanism?
- What policy shock or institutional discontinuity could improve identification?
- Can the result be tested in China using listed firms, PE/VC deal data, patent data, customs data, industrial enterprise data, or local policy variation?
- Could a theory model explain heterogeneity in the empirical results?
- Could the paper's mechanism generate opposite effects in early-stage VC vs buyout PE?
