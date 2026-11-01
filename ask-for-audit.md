
## Auditing Process

You can message me on twitter, discord, or telegram to ask for it.

**Contact:** [X / Twitter](https://x.com/Wojack0x0) · [LinkedIn](https://www.linkedin.com/in/wojack0x0/) · Telegram: `Wojack0x0` · Discord: `Wojack0x0` · Email: `kkgg123600@gmail.com`

### 1. Scoping (free)

Usually a few hours, at most one day. I go through the codebase and documentation to assess:

- Size (nSLOC) and code complexity
- External integrations (oracles, AMMs, bridges, lending markets, etc.)
- Access control and the degree of centralization
- Test coverage and how ready the code is for review

You receive a short scoping note with a quote, an estimated timeline, and any readiness gaps worth fixing before the review starts.

### 2. Security Review

Once scope, price, and dates are agreed:

- Manual line-by-line review, starting from the protocol's core invariants and value flows
- Foundry PoCs for High and Medium findings wherever feasible, using your real contracts
- Fuzz / invariant / fork testing where it adds signal
- A direct channel with your developers for questions about intended behavior

Findings are delivered as issues in a **private** GitHub repository, each with severity, root cause, impact, PoC, and a recommended fix. Your team can discuss validity and severity directly on each issue.

### 3. Mitigation Review

After your team pushes fixes:

- Each fix is verified against the original issue
- Fixes are checked for regressions or newly introduced issues
- A final report is delivered with the status of every finding (Fixed / Acknowledged / Partially Fixed)

---

## Pricing and Duration

### Pricing

The quote is based on:

1. **Size** — nSLOC in scope, measured with [solidity-metrics](https://github.com/Consensys/solidity-metrics)
2. **Complexity** — external integrations, heavy math, assembly / Yul, upgradeability, cross-chain logic

Indicative range: **`<X>`–`<Y>` USDC per nSLOC**, adjusted for complexity. The final price is fixed in the scoping note before work starts.

### Duration

Typical timelines for standard-complexity code:

| nSLOC | Estimated duration |
|:--:|:--:|
| ≤ 500 | up to 4 days |
| 501 – 1,000 | up to 7 days |
| 1,001 – 1,500 | up to 10 days |
| 1,501 – 2,000 | up to 14 days |
| > 2,000 | quoted individually |

High-complexity code may need more time; this is agreed during scoping, not after.

---

## Terms

- **Payment:** `<50% before the review starts, 50% on delivery of the findings>`. Payment in USDC / USDT on `<chains>`.
- **Frozen scope:** the review covers a fixed commit hash. Changes made during the review are out of scope unless agreed.
- **Mitigation window:** the mitigation review is included if fixes are submitted within **2 weeks** of findings delivery. After that, it is rescheduled based on availability.
- **Mitigation scope:** fixes for reported issues only. New features or large redesigns (for example, a fix that adds hundreds of lines) are quoted separately.
- **Confidentiality:** code and findings stay private. The final report is published only with your written consent.

---

## Disclaimer

A security review is a time-boxed, best-effort assessment of the code at a specific commit. It cannot guarantee that the protocol is free of vulnerabilities. It does not cover off-chain components, deployment and key-management practices, or economic and market risks unless they are explicitly in scope. Multiple independent reviews, contests, bug bounties, and monitoring are recommended for any protocol that holds user funds.
