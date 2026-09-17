# Crypto Due Diligence Framework

**Author:** Joe Nasr  
**Identity:** https://linktr.ee/joenasr/  
**Live page:** https://joenasriani.github.io/crypto-forensic-framework/

An independent research framework for structuring open-source due diligence on cryptocurrency projects, exchanges, tokens, and DeFi protocols.

The repository is a research and methodology artifact. It does **not** contain a live blockchain scanner, automated fraud detector, wallet-clustering engine, real-time alerting system, smart-contract auditor, exchange surveillance service, or incident-response platform.

## Research question

How can publicly accessible evidence from legal-entity records, deployed code, smart contracts, on-chain activity, infrastructure, market data, and public claims be organized into a reproducible due-diligence process without converting warning signals into unsupported accusations?

## Core research rule

**A red flag is not proof of fraud, and the absence of a red flag is not proof of legitimacy.**

The framework separates:

- verified observation
- source-backed fact
- analytical inference
- allegation or third-party claim
- alternative explanation
- unresolved / unknown

No attribution of ownership, coordination, fraud, insolvency, manipulation, sanctions status, or regulatory status should exceed the evidence available for that specific claim.

## Method

For each investigated claim or entity:

1. **Define the target** — exact entity, token, contract, exchange, domain, wallet, or public claim.
2. **Fix the jurisdiction and date** — legal and regulatory conclusions are jurisdiction- and time-specific.
3. **State the claim being tested** — do not begin with a verdict.
4. **Collect primary evidence first** — deployed contracts, transaction records, official registries, court or enforcement records, corporate filings, signed/public technical documents, and first-party statements.
5. **Record provenance** — URL, registry identifier, contract address, chain, transaction hash, block number, timestamp, archive date, document version, or commit where applicable.
6. **Corroborate independently** — distinguish source agreement from source independence.
7. **Separate observation from interpretation** — wallet interaction does not prove common ownership; concentration does not prove manipulation; a young domain does not prove fraud.
8. **Test alternatives** — record plausible non-malicious explanations and contradictory evidence.
9. **Assign bounded confidence** — confidence applies to the specific claim, not to the project as a whole.
10. **State falsifiers and unknowns** — identify what evidence would weaken, overturn, or leave the conclusion unresolved.

## Source hierarchy

### Tier 1 — Primary records

- blockchain transactions, blocks, verified deployed bytecode and contract state
- official corporate and beneficial-ownership records where lawfully public
- official regulator registers, enforcement notices, sanctions lists, court records, and government publications
- project-controlled repositories, signed releases, technical documentation, governance records, and first-party disclosures

### Tier 2 — Direct technical evidence

- reproducible contract analysis
- public audit reports with scope/version/date verified against deployed code
- archived websites and release histories
- DNS, certificate, package, repository, and infrastructure metadata obtained lawfully from public sources

### Tier 3 — Independent analysis

- peer-reviewed research
- established market or blockchain analytics providers
- reputable investigative reporting with transparent sourcing

Third-party wallet labels, risk scores, clustering outputs, exchange ratings, and scanner warnings remain **claims or analytical outputs** until independently supported.

### Tier 4 — Promotional / social signals

- marketing pages
- testimonials
- influencer claims
- follower counts and engagement metrics
- community posts

These can generate questions but should not independently establish legitimacy, fraud, ownership, or coordination.

## Analytical dimensions

1. **Entity identity and regulatory claims** — legal entity, jurisdiction, controlling persons, licenses, registrations, affiliations.
2. **Smart-contract and code review** — contract identity, upgradeability, privileged functions, minting, pausing, blacklisting, fee changes, custody and withdrawal controls.
3. **Token, liquidity, and asset-control structure** — supply, vesting, treasury, liquidity control, multisig configuration, concentration, custody and liabilities.
4. **On-chain behavior** — transaction flows, funding origins, related-wallet hypotheses, circular flows, concentration changes, governance activity.
5. **Infrastructure and history** — domains, archived pages, repositories, release chronology, package metadata, public documentation.
6. **Public and market claims** — partnerships, audits, certifications, customer/volume claims, rankings, returns, promotional statements and social amplification.

## Evidence record

A reproducible finding should record, where applicable:

| Field | Record |
| --- | --- |
| Claim under test | Exact proposition being evaluated |
| Observation | What the source directly shows |
| Source | Primary URL / identifier |
| Date captured | UTC date/time where material |
| Chain / contract | Network + address |
| Transaction / block | Hash + block number |
| Interpretation | What is inferred from the observation |
| Alternative explanation | Plausible competing interpretation |
| Confidence | High / medium / low, scoped to this claim |
| Falsifier | Evidence that would materially weaken the inference |
| Status | Verified / supported inference / unresolved / rejected |

## Case-study protocol

Historical cases may be used to test whether the framework would have surfaced relevant evidence **without hindsight leakage**. A case study should therefore distinguish:

- information publicly available before the event
- evidence disclosed only after collapse, enforcement, litigation, or investigation
- signals that were genuinely discriminating from common benign features
- false positives the same rule would create in legitimate projects

The framework should not claim that a historical failure was predictably detectable unless the relevant evidence was actually public and available at the tested time.

## Research anchors

These are methodological or regulatory reference points, not evidence that any named crypto project is compliant, non-compliant, solvent, fraudulent, or controlled by a particular actor.

### Regulatory and standards context

- FATF — **Seventh Targeted Update on Implementation of the FATF Standards on Virtual Assets/VASPs** (16 July 2026): https://www.fatf-gafi.org/en/publications/Fatfrecommendations/targeted-updated-virtualassets-vasps-2026.html
- IOSCO — **Policy Recommendations for Crypto and Digital Asset Markets** (Final Report, 16 November 2023): https://www.iosco.org/library/pubdocs/pdf/IOSCOPD747.pdf
- U.S. Treasury / OFAC — **Sanctions Compliance Guidance for the Virtual Currency Industry** (15 October 2021, U.S.-specific): https://ofac.treasury.gov/recent-actions/20211015

FATF and IOSCO materials provide international standards/recommendations; they are not substitutes for the current law or regulator record of the jurisdiction being investigated. OFAC guidance is U.S.-specific.

### Technical research context

- Meiklejohn S, Pomarole M, Jordan G, et al. **A Fistful of Bitcoins: Characterizing Payments Among Men with No Names**. IMC 2013. DOI: https://doi.org/10.1145/2504730.2504747 — foundational work showing how transaction-graph heuristics can support address clustering while remaining heuristic rather than proof of real-world identity.
- Dagher GG, Buenz B, Bonneau J, Clark J, Boneh D. **Provisions: Privacy-preserving proofs of solvency for Bitcoin exchanges** (2015): https://eprint.iacr.org/2015/1008 — a proof-of-solvency approach that explicitly treats reserves and customer liabilities as part of the solvency question.
- Lazirko M, Appelbaum D, Vasarhelyi M. **Proof of reserves: a double-helix framework**. *The British Accounting Review* (2025). DOI: https://doi.org/10.1016/j.bar.2025.101730 — recent work emphasizing the incompleteness of reserve-only verification and the need to connect on-chain and off-chain obligations.

These papers support methodological questions; they do not validate a particular wallet attribution, exchange solvency claim, or fraud allegation without target-specific evidence.

## Limitations

This framework is not financial advice, legal advice, a regulatory determination, a forensic certification, or a substitute for qualified smart-contract/security review. It does not establish criminal intent, beneficial ownership, insolvency, market manipulation, sanctions exposure, or fraud from pattern matching alone.

Public-source availability varies by jurisdiction and chain. Wallet attribution can be uncertain. Smart-contract behavior can change through proxies, upgrades, governance, or external dependencies. Archived material can be incomplete. Third-party datasets may contain labeling errors. Findings should therefore preserve provenance, uncertainty, and alternative explanations.

**Research audit updated:** 17 September 2026.

Repository: https://github.com/Joenasriani/crypto-forensic-framework
