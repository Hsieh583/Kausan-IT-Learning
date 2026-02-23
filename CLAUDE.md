# CLAUDE.md — Kausan IT Learning

## Project Purpose

A structured IT technical training documentation library for Kausan IT personnel.
The goal is to progressively raise IT operational maturity from Level 1 to Level 5 (L1–L5),
targeting ISO 27001 certification readiness by mid-2026.

Training is driven by an **Operational-First** strategy:
> 以不中斷、不爆炸為核心，逐層提升IT品質
> ("No outages, no explosions — build quality layer by layer")

Priority context (as of 2026-Q1):
- 1 IT staff covering ~5 roles (205% overload)
- 90% risk of critical system failure within 3 months
- ISO 27001 certification window: February–June 2026

---

## Tech Stack

This is a **documentation-only project** — no application code, no runtime dependencies.

| Tool | Purpose |
|------|---------|
| Markdown (`.md`) | All training materials and guides |
| Git | Version control for documents (see `L5_資訊治理與合規/Git_Documentation_Version_Control_Guide.md`) |
| GitHub/GitLab (implied) | Remote hosting and review workflow |

---

## Key Commands

There is no build, test, or lint pipeline. The following commands are useful for
working with this documentation repository.

### Markdown linting (optional)
```bash
# Install markdownlint-cli if not present
npm install -g markdownlint-cli

# Lint all Markdown files
markdownlint "**/*.md"
```

### Git workflow
```bash
# Stage and commit updated docs
git add <file>
git commit -m "docs: <brief description>"

# Check document change history
git log --oneline -- <file>
```

### Search across all documents
```bash
# Find keyword across all .md files (Unix)
grep -r "keyword" --include="*.md" .
```

---

## Framework: L1–L5 Operational Maturity Levels

Defined in [L1-L5_營運優先層級框架.md](L1-L5_營運優先層級框架.md).

```
L5: Documentation & Compliance      ← Final acceptance layer
     ↑
[Evidence automation pipeline]      ← Bridge: auto-generate registers
     ↑
L4: Tools & Automation              ← Accelerate delivery, reduce toil
L3: User Experience                 ← Reduce friction for end-users
L2: Defense & Monitoring            ← Signals when things go wrong
L1: Reliability & Disaster Recovery ← Foundation: no outages, no data loss
```

---

## Important Files & Folders

### Root-level documents

| File | Description |
|------|-------------|
| [Plan.md](Plan.md) | Master implementation checklist (tracks completion of all L1–L5 materials) |
| [L1-L5_營運優先層級框架.md](L1-L5_營運優先層級框架.md) | Full framework definition with maturity levels, KPIs, and ISO 27001 mappings |
| [Training_Schedule_2026Q1-Q2.md](Training_Schedule_2026Q1-Q2.md) | Q1–Q2 training schedule with priority tiers (P0/P1/P2), hours, and budget |
| [Technical_Glossary.md](Technical_Glossary.md) | Unified glossary of IT terms (bilingual: Chinese/English) |
| [IT Service Catalog_服務語言版.md](IT%20Service%20Catalog_服務語言版.md) | IT service catalog in Chinese |

### Training material folders

| Folder | Layer | Contents |
|--------|-------|---------|
| [L1_可靠性與容災/](L1_可靠性與容災/) | L1 | DR/BCP business continuity training |
| [L1_可靠性與災難復原/](L1_可靠性與災難復原/) | L1 | Backup verification guide |
| [L2_防禦與監控/](L2_防禦與監控/) | L2 | Firewall/network segmentation, incident response SOP, vulnerability management, Wazuh SIEM operations |
| [L3_使用者體驗/](L3_使用者體驗/) | L3 | IAM account management manual |
| [L5_文件與合規/](L5_文件與合規/) | L5 | ISO 27001 internal audit guide |
| [L5_資訊治理與合規/](L5_資訊治理與合規/) | L5 | Git documentation & version control guide |

### Missing / incomplete (per Plan.md)

- **L4 folder** — Tools & Automation materials not yet created
- Cross-cutting materials: technical debt management, career development path, troubleshooting scenarios

---

## Conventions

- All documents are bilingual (Traditional Chinese primary, English secondary) unless noted.
- Document headers include version, last-updated date, and owner fields.
- ISO 27001 control mappings are noted inline where applicable.
- Maturity levels use a 1–5 scale; current baseline is ~1.5, target for 2026 Q1–Q2 is 2.5–3.0.
