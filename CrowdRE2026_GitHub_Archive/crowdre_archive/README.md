# CrowdRE 2026 — Beyond App Reviews: Archive

**Paper:** Beyond App Reviews: Mining Crowd Feedback for Smart Connected Product Requirements  
**Venue:** CrowdRE 2026 Workshop @ IEEE RE'26  
**Submitted:** 2026-05-25 (Submission 3, Version 3)  
**Author:** Zhimin Wang, Shanghai Jiao Tong University  
**Contact:** myra0406@sjtu.edu.cn

---

## Repository Structure

```
paper/          Final submitted PDF and LaTeX source
figures/        Pipeline diagram (used in paper)
data/
  crowdre_raw_analysis/     Smartphone corpus analysis outputs
  vehicle_nlp_artifacts/    Smart vehicle NLP pipeline outputs
docs/           Submission log and notes
```

## Data Notes

- **Smartphone corpus**: 4,984 items from Reddit, Bilibili, GSMArena, SMZDM  
  (6 brands: vivo, Samsung, Xiaomi, Apple, OPPO, Huawei)
- **Smart vehicle corpus**: 1,185 posts + 18,049 comments from Bilibili and Reddit  
  (9 brands, 34 models)
- Raw comment text is **not included** in this repository.  
  Full crawler scripts: https://github.com/MyraWang0406/Auto-sentiment-copilot-V1
- All analysis outputs are exploratory NLP artifacts, not benchmark-quality annotations.

## Paper Abstract

CrowdRE has spent its first decade primarily mining app store reviews. This experience
report applies a platform-aware CrowdRE pipeline to smartphones and new-energy vehicles,
showing that platform identity substantially shifts the observed requirement vocabulary,
and that smart connected products require vocabulary extensions beyond app-review taxonomies.

## Key Findings

| Finding | Summary |
|---------|---------|
| F1 | Platform identity shapes requirement vocabulary (GSMArena 16.1% neg vs Reddit 8.9%) |
| F2 | Smart vehicle crowd surfaces reliability/dealer trust over battery/software |
| F3 | Used-vehicle context reveals OEM pipeline blind spot (battery health, service history) |

## Submission Log

| Version | Date | Time | Note |
|---------|------|------|------|
| v1 | 2026-05-25 | 08:11 | Initial submission |
| v2 | 2026-05-25 | 08:24 | Reference corrections ([12][13]) |
| v3 | 2026-05-25 | 11:36 | Final: ref [10][12][14] page numbers corrected |
