# CrowdRE 2026 Submission Archive

**Beyond App Reviews: Mining Crowd Feedback for Smart Connected Product Requirements**  
*A Platform-Aware Experience Report Toward CrowdRE 2030*

## Project Information

| Item | Description |
|---|---|
| Venue | CrowdRE 2026 Workshop @ IEEE RE'26, August 2026, Lisbon |
| Type | Full Paper, Experience Report, 6 pages |
| Author | Zhimin Wang, Shanghai Jiao Tong University |
| Email | myra0406@sjtu.edu.cn |
| Submitted | 2026-05-25, EasyChair Submission 3, Version 3 |
| Status | Under review |
| Primary code repository | [Auto-sentiment-copilot-V1](https://github.com/MyraWang0406/Auto-sentiment-copilot-V1) |

## What This Repository Is

This repository is a **submission archive**.

It stores the paper PDF, LaTeX source, figures, analysis outputs, and submission history for the CrowdRE 2026 submission.

It is a backup and traceability record, not the primary code repository.

For crawler scripts, NLP pipeline, platform-specific processing logic, and domain-specific code, see:

[Auto-sentiment-copilot-V1](https://github.com/MyraWang0406/Auto-sentiment-copilot-V1)

## Relationship to the Primary Code Repository

| Repository | Role |
|---|---|
| [Auto-sentiment-copilot-V1](https://github.com/MyraWang0406/Auto-sentiment-copilot-V1) | Primary code artifact for crawlers, NLP processing, platform-aware analysis, and prototype interface |
| [UsedCarInsightForManus](https://github.com/MyraWang0406/UsedCarInsightForManus) | Supporting vehicle NLP pipeline and second-hand vehicle feedback analysis |
| [CrowdRE2026-Beyond-App-Reviews-Archive](https://github.com/MyraWang0406/CrowdRE2026-Beyond-App-Reviews-Archive) | Paper archive, analysis-output backup, submission record, and traceability materials |

This separation is intentional.

The archive repository preserves the submitted research artifact. The primary code repository preserves the executable system and processing pipeline.

## What This Paper Argues

CrowdRE has spent its first decade primarily mining app store reviews.

Smart connected products, such as smartphones and new-energy vehicles, generate crowd feedback that is distributed across structurally different platforms, spans multiple languages, and covers concerns that app-review taxonomies cannot fully express.

Examples include:

- battery degradation
- dealer trust
- OTA reliability
- second-hand EV transaction transparency
- lifecycle maintenance
- platform trust
- post-purchase service experience

## Contributions

### C1. Smart Connected Products as a Distinct CrowdRE Context

Smart connected products combine hardware lifecycle, software quality, service trust, and transaction integrity in the same user feedback space.

### C2. Evidence-to-Requirement-Signal Workflow

The paper proposes a workflow that links every requirement candidate to an inspectable evidence chain:

**source platform → topic cluster → evidence sample → requirement signal**

### C3. Platform Identity as a Requirement Variable

Platform identity substantially shifts the observed requirement vocabulary.

Merging platforms without stratification creates a synthetic corpus that may represent no real user group.

## Repository Structure

| Path | Description |
|---|---|
| `README.md` | Repository overview |
| `paper/CrowdRE2026_Beyond_App_Reviews_FINAL.pdf` | Submitted PDF, Version 3 |
| `paper/CrowdRE2026_Beyond_App_Reviews_FINAL.tex` | LaTeX source |
| `figures/CrowdRE2026_pipeline_figure.pdf` | Pipeline figure used in the paper |
| `data/crowdre_raw_analysis/` | Smartphone corpus analysis outputs |
| `data/vehicle_nlp_artifacts/` | Vehicle corpus analysis outputs |
| `docs/SUBMISSION_LOG.md` | Submission version history |

## Analysis Output Files

### Smartphone Corpus Outputs

| File | Description |
|---|---|
| `data/crowdre_raw_analysis/counts_by_platform_clean.csv` | Cleaned feedback counts by platform |
| `data/crowdre_raw_analysis/sentiment_by_platform_clean.csv` | Sentiment distribution by platform |
| `data/crowdre_raw_analysis/topic_distribution_clean.csv` | Topic distribution across the smartphone corpus |
| `data/crowdre_raw_analysis/topic_by_platform_clean.csv` | Topic distribution stratified by platform |
| `data/crowdre_raw_analysis/evidence_samples_by_topic.csv` | Evidence samples grouped by topic |
| `data/crowdre_raw_analysis/combined_crowdre_summary.json` | Combined analysis summary |

### Vehicle Corpus Outputs

| File | Description |
|---|---|
| `data/vehicle_nlp_artifacts/complaints_by_issue_type.csv` | Complaint categories and issue-type counts |
| `data/vehicle_nlp_artifacts/complaints_by_brand_model.csv` | Complaints grouped by brand and model |
| `data/vehicle_nlp_artifacts/nlp_summary.json` | Vehicle NLP summary output |

## Data Notes

| Table in Paper | Source File | Status |
|---|---|---|
| Table I: collection protocol | Documented in paper; scripts in Auto-sentiment-copilot-V1 | Reproducible |
| Table II: sentiment by platform | `vehicle_nlp_artifacts/nlp_summary.json` | Automated labels |
| Table III: complaints and requirement candidates | `vehicle_nlp_artifacts/complaints_by_issue_type.csv` | Exploratory, automated NLP artifact |
| Table IV: traced examples | Paraphrased from corpus | Manual coding |
| Tables V–VI: sanity check | Paraphrased; full list in Auto-sentiment-copilot-V1 | 50-item author inspection |
| Table VII: cross-domain topics | `crowdre_raw_analysis/topic_distribution_clean.csv` | Exploratory |

All complaint and topic counts are exploratory NLP artifacts, not benchmark-quality annotations.

Raw comment text is not included. See the data ethics statement in the paper for details.

## Submission History

| Version | Date | Time | Change |
|---|---|---|---|
| v1 | 2026-05-25 | 08:11 | Initial submission |
| v2 | 2026-05-25 | 08:24 | Fixed reference [12] venue and reference [13] arXiv number |
| v3 | 2026-05-25 | 11:36 | Fixed reference [10] pp. 298–305, reference [12] pp. 82–87, and reference [14] pp. 216–225 |

## Key Findings

### Platform Identity Shapes What Requirements Are Observable

The same product category produces different requirement vocabularies across platforms.

Examples from the paper:

| Platform | Negative Share | Interpretation |
|---|---:|---|
| GSMArena | 16.1% | More technically engaged reviewers |
| Reddit | 8.9% | Discussion-seeking users |
| Bilibili | 5.7% | Mixed effect of noise and purchase-intent framing |

These differences partly reflect platform culture, user composition, discussion norms, and purchase-intent framing.

### Ownership-Phase Concerns Dominate the Vehicle Corpus

In the vehicle corpus, ownership-phase concerns ranked above more commonly discussed product features.

| Issue Type | Count |
|---|---:|
| Reliability / maintenance | 469 |
| Dealer / platform trust | 372 |
| Battery / range | 77 |
| Software / infotainment | 33 |

This suggests that post-purchase service and lifecycle trust are important requirement sources for smart connected products.

### Second-Hand Buyers Are an Invisible CrowdRE Stakeholder

The paper identifies second-hand vehicle buyers as an often invisible stakeholder group in requirements pipelines.

Observed requirement candidates include:

- battery health certification
- service history access
- charging infrastructure information at resale

These requirements are often absent from OEM new-car requirement pipelines.

## Open Research Questions

### RQ1

How can cross-platform sentiment be normalized without discarding variation that is itself a requirement signal?

### RQ2

Who in the requirements engineering process should own lifecycle-phase and post-purchase requirement categories?

### RQ3

Can a unified CrowdRE ontology include a shared economic layer, such as price and value, while preserving domain-specific vocabularies above it?

## Relation to Broader Research Portfolio

This archive is part of a broader research portfolio on traceable AI-assisted decision-making.

| Repository | Research Role |
|---|---|
| [Auto-sentiment-copilot-V1](https://github.com/MyraWang0406/Auto-sentiment-copilot-V1) | Studies how crowd feedback becomes requirement evidence |
| [UserResearchAgent-CF](https://github.com/MyraWang0406/UserResearchAgent-CF) | Studies how decision memory and falsified assumptions constrain future requirements decisions |
| [MatrixMirix.WhatIf](https://github.com/MyraWang0406/MatrixMirix.WhatIf) | Studies how multi-agent reflection supports pre-decision reasoning |
| [ADX-Mirix-1.15-cursor](https://github.com/MyraWang0406/ADX-Mirix-1.15-cursor) | Studies traceable diagnosis in automated advertising workflows |

The shared design principle is:

> No decision without inspectable evidence.

## Citation

Zhimin Wang.  
"Beyond App Reviews: Mining Crowd Feedback for Smart Connected Product Requirements: A Platform-Aware Experience Report Toward CrowdRE 2030."  
CrowdRE 2026 Workshop @ IEEE RE'26, 2026. Under review.

## License

Paper and LaTeX source: all rights reserved until publication.

Analysis output CSVs: available for research reference; not for redistribution.

Raw platform data: not included. Contact myra0406@sjtu.edu.cn for access requests.
