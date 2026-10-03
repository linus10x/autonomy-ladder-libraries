# Autonomy Ladder™ — Reference Libraries

**Six open, DOI-archived governance libraries for autonomous AI in regulated operations.** One framework (A0→A4), six co-equal regulated verticals, a common evidence discipline. This is the single landing page for the family — start here.

**Framework + whitepaper:** [autonomy-ladder.io](https://autonomy-ladder.io)

> **What this family is:** reference implementations of deployment-authority governance for AI agents — the A0→A4 rungs, a non-overridable sovereign veto, a hash-chain audit ledger, hard envelopes, and mechanical demotion — encoded per regulated decision class as runnable, tested Python.
> **What it is not:** deployed production controls. These are reference IP for adoption and inspection — never represented as a control running in any institution's production.

---

## The six libraries

| Library | Vertical | Decision classes encoded | Primary regulator / rule | Tests · coverage | DOI | Start here |
|---|---|---|---|---|---|---|
| [**finserv-agent-audit**](https://github.com/linus10x/finserv-agent-audit) | Cross-vertical financial services | Lending, core FS decisioning | EU AI Act Art. 14 · SR-letters · FCRA | 722 · 94% | [10.5281/zenodo.20434570](https://doi.org/10.5281/zenodo.20434570) | DEFCON + Sovereign-Veto demo |
| [**banking-agent-audit**](https://github.com/linus10x/banking-agent-audit) | Banking | Model risk · ECOA/Reg B adverse action · BSA/AML/OFAC | ECOA 12 CFR §1002.9 · FINRA 3110 | 182 · ~99% | [10.5281/zenodo.20564584](https://doi.org/10.5281/zenodo.20564584) | `tests/` ECOA adverse-action |
| [**payments-agent-audit**](https://github.com/linus10x/payments-agent-audit) | Payments | OFAC screening · BSA/AML · Reg E · rail finality | OFAC · Reg E · rail-finality (AL-PROBE-06) | 183 · 98.97% | [10.5281/zenodo.20592773](https://doi.org/10.5281/zenodo.20592773) | AL-PROBE-06 irreversibility gate |
| [**payer-agent-audit**](https://github.com/linus10x/payer-agent-audit) | Health-insurance payer | Utilization mgmt · prior auth · claims/appeals | NAIC Model Bulletin (no medical-necessity call) | 156 · 100% | [10.5281/zenodo.20564377](https://doi.org/10.5281/zenodo.20564377) | Funding-type obligation routing |
| [**private-capital-agent-audit**](https://github.com/linus10x/private-capital-agent-audit) | SEC-registered investment advisers | Best execution · MNPI · custody · marketing · allocation | Advisers Act §206 | 181 · 98.7% | [10.5281/zenodo.20564496](https://doi.org/10.5281/zenodo.20564496) | Golden corpus of real SEC matters |
| [**cre-agent-audit**](https://github.com/linus10x/cre-agent-audit) | Commercial real estate | Tenant screening · lease provenance · PII residency | Fair-housing · FCRA §607(b) | 369 · 87% | [10.5281/zenodo.20437081](https://doi.org/10.5281/zenodo.20437081) | Fair-Housing Pre-Flight |

*All six: zero runtime dependencies · `mypy --strict` · SHA-pinned CI · golden corpora of real, primary-sourced enforcement actions. Released as a coordinated family.*

---

## The framework they all implement (A0 → A4)

Every library encodes the same five rungs of deployment authority. The *decision class* changes by vertical; the rungs, the climbing rule, and the controls do not.

```
A4  Production Autonomous   ── writes across coordinating agents; monitor-led promotion + validated escalation
A3  Supervised Autonomous   ── writes one decision class autonomously; non-overridable sovereign veto + live ledger
A2  Delegated               ── writes inside a hard, mechanically-enforced envelope; sampled review
A1  Assisted                ── drafts; a human approves every write
A0  Informational           ── reads & recommends; no write authority
        ▲ climb one rung at a time, only on evidence ·  ▼ demote the moment assurance degrades (routine, not crisis)
```

Three controls make each rung a control and not a slide: a **sovereign veto** the agent cannot switch off, a **hash-chain audit ledger** (every action reconstructable for a safety case), and a **mechanical demotion trigger**.

---

## Which library should I read first?

- **A bank, lender, or fair-lending / model-risk team** → [`banking-agent-audit`](https://github.com/linus10x/banking-agent-audit) (ECOA/Reg B adverse action) or [`finserv-agent-audit`](https://github.com/linus10x/finserv-agent-audit) for cross-vertical.
- **A payments company / fintech moving money on irreversible rails** → [`payments-agent-audit`](https://github.com/linus10x/payments-agent-audit) (OFAC screening + the rail-finality gate).
- **A health plan / payer (UM, prior auth, appeals)** → [`payer-agent-audit`](https://github.com/linus10x/payer-agent-audit) (governs the audit record, not the medical-necessity call).
- **An asset manager, allocator, or RIA** → [`private-capital-agent-audit`](https://github.com/linus10x/private-capital-agent-audit) (Advisers Act §206).
- **A CRE owner / proptech / screening platform** → [`cre-agent-audit`](https://github.com/linus10x/cre-agent-audit) (fair-housing pre-flight, lease provenance).
- **A frontier lab or cloud platform deploying agents *into* regulated customers** → start with [`finserv-agent-audit`](https://github.com/linus10x/finserv-agent-audit); the A0→A4 control surfaces are domain-agnostic (see each repo's "Why this exists for frontier autonomy stacks").

---

## How to read these (the 30-second version)

1. Open the library matching your decision class (above).
2. Read its **"Read me first"** pointer — the single most concrete regulator-mapped test + the worked example.
3. The **test suite is the falsifiability proof** — each qualitative rule is a runnable check.
4. The framework behind all six: **[autonomy-ladder.io](https://autonomy-ladder.io)**.

---

*Authored by Kunjar Bhaduri. Each library is MIT-licensed or dual MIT OR Apache-2.0 (see each repo), DOI-archived for citation, and maintained as living research. Comments and critique welcome — open an issue on the relevant library.*
