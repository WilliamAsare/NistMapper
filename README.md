# NIST Mapper

**The complete NIST cybersecurity standards ecosystem: visualized, interactive, and accessible.**

**Live Platform: [nist-mapper.vercel.app](https://nist-mapper.vercel.app)**

---

## What Is NIST Mapper?

NIST (National Institute of Standards and Technology) publishes the world's most important cybersecurity frameworks and standards, including SP 800-53, the Cybersecurity Framework (CSF 2.0), MITRE ATT&CK mappings, and dozens more. These publications reference each other, build upon each other, and together form a complex knowledge web.

**The problem:** Understanding how 57+ publications, 1,196 security controls, 20 control families, and 49 ATT&CK techniques connect to each other requires reading thousands of pages across dozens of PDFs.

**NIST Mapper solves this** by transforming the entire ecosystem into a single interactive platform where every relationship is visual, explorable, and immediately understandable.

---

## Features

### Interactive Knowledge Graph
A force-directed D3.js network visualization of the entire NIST publication ecosystem. Each node represents a publication or framework. Each edge shows how they connect through references, implementations, or hierarchical relationships. Hover to highlight connections. Click to explore.

### 3-Panel Publication Explorer
A deep-dive interface with three synchronized panels:
- **Left:** Framework tree organizing every document by series
- **Center:** Full detail view with metadata, descriptions, and direct links to official NIST publications
- **Right:** Cross-references and relationship sidebar showing all connected documents

### CSF 2.0 x SP 800-53 Control Heatmap
A visual matrix showing how Cybersecurity Framework 2.0 categories map to SP 800-53 control families. Cell intensity represents the number of control mappings, making coverage gaps instantly visible at a glance.

### MITRE ATT&CK Threat Matrix
All 14 ATT&CK Enterprise tactics displayed as columns with techniques listed underneath. Each technique shows its defense coverage, indicating how many SP 800-53 controls mitigate that specific threat. Color-coded from red to green for instant coverage assessment.

### Baseline Comparison
Side-by-side comparison of LOW, MODERATE, and HIGH impact security baselines from SP 800-53. See exactly what controls are added at each level, broken down by control family, so you know precisely what each baseline commitment requires.

### Compliance Wizard
A decision-support tool for organizations. Select your type (federal agency, contractor, healthcare, financial services, small business, cloud provider, or critical infrastructure) and receive a personalized compliance pathway showing exactly which NIST frameworks and controls apply to your situation.

### Learning Paths
Guided educational walkthroughs organized by difficulty level. From beginner overviews of the CSF framework to advanced deep-dives into control implementation.

### Additional Features
- **Publication Timeline:** 25 years of NIST publications across every series, showing evolution and supersession
- **Glossary:** Complete NIST cybersecurity terminology reference
- **Insights & Statistics:** Analytics dashboard with ecosystem-wide metrics
- **Global Search:** Instant full-text search across all publications and controls
- **Command Palette:** Quick keyboard navigation (Ctrl+K)
- **Dark + Light Mode:** Full theme support
- **Mobile Responsive:** Works on desktop, tablet, and phone

---

## Platform Stats

| Metric | Count |
|--------|-------|
| NIST Publications | 57 |
| Security Controls | 1,196 |
| Control Families | 20 |
| MITRE ATT&CK Techniques | 49 |
| Knowledge Graph Nodes | 1,401 |
| Knowledge Graph Edges | 5,270 |
| Interactive Pages | 12 |
| API Endpoints | 11 |

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Next.js 16 (App Router) |
| Language | TypeScript |
| Styling | Tailwind CSS v4 |
| Visualization | D3.js v7 (force-directed graphs, heatmaps) |
| Data Layer | In-memory knowledge graph (27 JSON data files) |
| Hosting | Vercel (Edge Network) |

---

## The NIST Ecosystem Covered

| Domain | Key Publications |
|--------|-----------------|
| Cybersecurity | CSF 2.0, SP 800-53 Rev 5, SP 800-171, SP 800-37 (RMF) |
| Privacy | Privacy Framework v1.0, SP 800-188 |
| AI & Machine Learning | AI RMF 1.0, AI 100-2 |
| Cloud | SP 800-144, SP 800-145, SP 800-210 |
| Risk Management | SP 800-30, SP 800-39, SP 800-37 |
| Cryptography | SP 800-57, SP 800-175B, FIPS 140-3, FIPS 197, FIPS 186-5 |
| And more... | 57 total publications across SP 800, SP 1800, FIPS, NISTIR, CSWP series |

---

## Who Is This For?

- **Security Engineers:** Quickly find which controls mitigate specific threats
- **Compliance Officers:** Navigate baseline requirements and generate compliance pathways
- **CISOs & Risk Managers:** Visualize coverage gaps across frameworks
- **GRC Analysts:** Explore cross-framework mappings (CSF to SP 800-53 to ATT&CK)
- **Students & Educators:** Learn NIST standards through interactive exploration
- **Federal Agencies:** Understand full RMF implementation requirements
- **Cloud Providers:** Map FedRAMP requirements to specific controls
- **Small Businesses:** Get personalized guidance through the Compliance Wizard

---

## Why I Built This

Navigating the NIST cybersecurity standards ecosystem is overwhelming. Publications reference each other across series, controls map to multiple frameworks, and threat techniques cut across all of them. Existing tools are either paywalled, static PDFs, or disconnected spreadsheets.

NIST Mapper makes the entire ecosystem explorable in one place: free, open, and visual. Whether you're a security professional mapping controls to threats, a student learning about CSF 2.0, or a small business trying to figure out where to start with compliance, this platform gives you immediate clarity.

---

## Try It Now

**[nist-mapper.vercel.app](https://nist-mapper.vercel.app)**

---

## Built By

**William Asare Yirenkyi**

- GitHub: [@WilliamAsare](https://github.com/WilliamAsare)

---

## License

This project writeup is publicly available. The source code is maintained in a private repository. NIST publications and standards referenced are public domain works of the U.S. Government.
