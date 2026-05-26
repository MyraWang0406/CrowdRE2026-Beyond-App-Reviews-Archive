# CrowdRE 2026 — Submission Archive

> **Beyond App Reviews: Mining Crowd Feedback for Smart Connected Product Requirements**  
> A Platform-Aware Experience Report Toward CrowdRE 2030

| | |
|---|---|
| **Venue** | CrowdRE 2026 Workshop @ IEEE RE'26 (August 2026, Lisbon) |
| **Type** | Full Paper — Experience Report (6 pages) |
| **Author** | Zhimin Wang · Shanghai Jiao Tong University · myra0406@sjtu.edu.cn |
| **Submitted** | 2026-05-25 · EasyChair Submission 3 · Version 3 (final) |
| **Status** | Under review |
| **Primary code repo** | [Auto-sentiment-copilot-V1](https://github.com/MyraWang0406/Auto-sentiment-copilot-V1) |

---

## What This Repository Is

This is the **submission archive** — it stores the paper PDF, LaTeX source, analysis outputs, and submission history. It is a backup and traceability record, not the primary code repository.

For crawler scripts, NLP pipeline, and domain-specific code, see [Auto-sentiment-copilot-V1](https://github.com/MyraWang0406/Auto-sentiment-copilot-V1).

---

## What This Paper Argues

CrowdRE has spent its first decade primarily mining app store reviews. Smart connected products — smartphones and new-energy vehicles — generate crowd feedback that is distributed across structurally different platforms, spans multiple languages, and covers concerns that app-review taxonomies (bug / feature request / praise) cannot express: battery degradation, dealer trust, OTA reliability, second-hand EV transaction transparency.

**Three contributions:**

- **C1** Smart connected products are a distinct CrowdRE context where hardware lifecycle, software quality, service trust, and transaction integrity co-exist in the same crowd.
- **C2** An evidence-to-requirement-signal workflow that links every requirement candidate to its source platform, topic, and inspectable evidence.
- **C3** Platform identity substantially shifts the observed requirement vocabulary — merging platforms without stratification creates a synthetic corpus representing no real user group.

---

## Repository Structure

```
CrowdRE2026-Beyond-App-Reviews-Archive/
├── README.md
├── paper/
│   ├── CrowdRE2026_Beyond_App_Reviews_FINAL.pdf   ← submitted PDF (v3)
│   └── CrowdRE2026_Beyond_App_Reviews_FINAL.tex   ← LaTeX source
├── figures/
│   └── CrowdRE2026_pipeline_figure.pdf            ← Fig. 1 in paper
├── data/
│   ├── crowdre_raw_analysis/                      ← smartphone corpus outputs
│   │   ├── counts_by_platform_clean.csv
│   │   ├── sentiment_by_platform_clean.csv
│   │   ├── topic_distribution_clean.csv
│   │   ├── topic_by_platform_clean.csv
│   │   ├── evidence_samples_by_topic.csv
│   │   └── combined_crowdre_summary.json
│   └── vehicle_nlp_artifacts/                     ← vehicle corpus outputs
│       ├── complaints_by_issue_type.csv            ← source of Table III
│       ├── complaints_by_brand_model.csv
│       └── nlp_summary.json
└── docs/
    └── SUBMISSION_LOG.md                          ← version history
```

---

## Data Notes

| Table in paper | Source file | Status |
|----------------|-------------|--------|
| Table I (collection protocol) | Documented in paper; scripts in Auto-sentiment-copilot-V1 | Reproducible |
| Table II (sentiment by platform) | `vehicle_nlp_artifacts/nlp_summary.json` | Automated labels |
| Table III (complaints + req. candidates) | `vehicle_nlp_artifacts/complaints_by_issue_type.csv` | **Exploratory, automated NLP artifact** |
| Table IV (traced examples) | Paraphrased from corpus | Manual coding |
| Tables V–VI (sanity check) | Paraphrased; full list in Auto-sentiment-copilot-V1 | 50-item author inspection |
| Table VII (cross-domain topics) | `crowdre_raw_analysis/topic_distribution_clean.csv` | Exploratory |

All complaint and topic counts are **exploratory NLP artifacts**, not benchmark-quality annotations. See paper Section VIII (Limitations) for full discussion. Raw comment text is not included — see data ethics statement in paper Section VI.

---

## Submission History

| Version | Date | Time | Change |
|---------|------|------|--------|
| v1 | 2026-05-25 | 08:11 | Initial submission |
| v2 | 2026-05-25 | 08:24 | Fixed ref [12] venue, ref [13] arXiv number |
| v3 | 2026-05-25 | 11:36 | Fixed ref [10] pp.298–305, ref [12] pp.82–87, ref [14] pp.216–225 |

---

## Key Findings

**Platform identity shapes what requirements are observable.**  
GSMArena: 16.1% negative (technically engaged reviewers). Reddit: 8.9% negative (discussion-seeking users). Bilibili: 5.7% negative (partly reflects noise, partly purchase-intent framing). Same products, three different requirement vocabularies.

**Ownership-phase concerns dominate the vehicle corpus.**  
`reliability/maintenance` (469 complaints) and `dealer/platform trust` (372) rank far above `battery/range` (77) and `software/infotainment` (33) — inverting typical EV product coverage emphasis.

**Second-hand buyers are an invisible CrowdRE stakeholder.**  
11 complaints → 17 requirement candidates: battery health certification, service history access, charging infrastructure at resale. None of these appear in OEM new-car requirements pipelines.

---

## Open Research Questions Raised (Toward 2030)

- **RQ1** How to normalize cross-platform sentiment without discarding variation that is itself a requirement signal?
- **RQ2** Who in the RE process owns lifecycle-phase and post-purchase requirement categories?
- **RQ3** Can a unified CrowdRE ontology have a shared economic layer (price/value appears in both domains) with domain-specific vocabularies above it?

---

## Citation

```
Zhimin Wang. "Beyond App Reviews: Mining Crowd Feedback for Smart Connected
Product Requirements: A Platform-Aware Experience Report Toward CrowdRE 2030."
CrowdRE 2026 Workshop @ IEEE RE'26, 2026. (under review)
```

---

## License

Paper and LaTeX source: All rights reserved until publication.  
Analysis output CSVs: Available for research reference; not for redistribution.  
Raw platform data: Not included; contact myra0406@sjtu.edu.cn for access requests.
