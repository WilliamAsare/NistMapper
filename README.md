# NIST Mapper

**The complete NIST cybersecurity standards ecosystem - visualized, interactive, and accessible.**

**Live Platform: [nist-mapper.vercel.app](https://nist-mapper.vercel.app)**

---

## What Is NIST Mapper?

NIST (National Institute of Standards and Technology) publishes the world's most important cybersecurity frameworks and standards, including SP 800-53, the Cybersecurity Framework (CSF 2.0), SP 800-171, MITRE ATT&CK mappings, and dozens more. These publications reference each other, build upon each other, and together form a complex knowledge web.

**The problem:** Understanding how 67+ publications, 1,196 security controls, the full CSF 2.0 Core, SP 800-171 requirements, and 49 ATT&CK techniques connect to each other requires reading thousands of pages across dozens of PDFs - and the cross-framework mappings between them are scattered across separate spreadsheets.

**NIST Mapper solves this** by transforming the entire ecosystem into a single interactive platform where every relationship is visual, explorable, and - critically - **sourced directly from NIST's own machine-readable data** so the mappings are authoritative rather than estimated.

---

## Authoritative by Design

What sets NIST Mapper apart is that it does not hand-author its core reference data. Wherever NIST publishes machine-readable data, the platform ingests it directly:

- **NIST CPRT** (Cybersecurity & Privacy Reference Tool) for the CSF 2.0 Core and SP 800-171 Rev 3
- **NIST OLIR** (Online Informative References) for the cross-framework crosswalks
- **OSCAL** for SP 800-53 Rev 5 controls, enhancements, and baselines
- **MITRE ATT&CK** (STIX) plus the Center for Threat-Informed Defense control mappings

Every cross-framework mapping carries its **provenance** - the source reference, its publication status, and whether it is a direct mapping or one derived through an intermediate framework. The pipeline is re-runnable, version-pinned, and guarded by an automated data-integrity test suite, so the data stays accurate and reproducible as NIST updates its standards.

---

## Features

### Interactive Knowledge Graph
A force-directed D3.js network visualization of the entire NIST publication ecosystem. Each node represents a publication or framework. Curved arc edges show how they connect through references, implementations, or hierarchical relationships. Hover to highlight connections. Click to explore. Zoom, pan, and filter by publication series.

### 3-Panel Publication Explorer
A deep-dive interface with three synchronized panels:
- **Left:** Framework tree organizing every document by series (SP 800, SP 1800, FIPS, NISTIR, CSWP)
- **Center:** Full detail view with metadata, descriptions, and direct links to official NIST publications
- **Right:** Cross-references and relationship sidebar showing all connected documents, each tagged with its OLIR source and status
- **Back navigation:** Browser-history-aware back button alongside breadcrumb trails

### Full CSF 2.0 Core
The complete Cybersecurity Framework 2.0 - all 6 Functions, 22 Categories, and 106 Subcategories - plus **363 official Implementation Examples** shown inline on each subcategory to make the guidance immediately actionable.

### CSF 2.0 Coverage Map
A visual matrix showing how all 22 CSF 2.0 categories map to the 20 SP 800-53 control families. Cell intensity represents the number of control mappings. The matrix is derived from NIST's **official CSF 2.0 to SP 800-53 Rev 5 informative reference** (746 subcategory-level mappings), so coverage gaps and overlaps reflect the authoritative crosswalk rather than estimates.

### SP 800-171 Rev 3
The complete Protecting Controlled Unclassified Information catalog - 17 families and 97 requirements with their discussions and **Organization-Defined Parameters (ODPs)** - mapped to CSF 2.0 (313 mappings). Essential for contractors and the CMMC program.

### Cross-Framework Mappings
Authoritative crosswalks connecting CSF 2.0 to SP 800-53, SP 800-171, CIS Controls v8.1, and PCI-DSS v4.0.1 - plus ISO/IEC 27001 and HIPAA coverage produced through Derived Relationship Mapping (composing crosswalks through SP 800-53). Over 1,700 sourced mapping relationships in total.

### MITRE ATT&CK Threat Matrix
All 14 ATT&CK Enterprise tactics displayed as columns with techniques listed underneath. Each technique shows its defense coverage, indicating how many SP 800-53 controls mitigate that specific threat. Color-coded from red to green for instant coverage assessment.

### SP 800-53 Control Classes
Control families organized by their SP 800-18 security classification:
- **Management:** Program management, planning, risk assessment, and governance controls
- **Operational:** Personnel security, physical protection, contingency planning, and awareness training
- **Technical:** Access control, audit, identification, system protection, and communications security

Each family card shows baseline indicators (LOW / MODERATE / HIGH) and expands into a detail panel with full control listings, CSF 2.0 mappings, ATT&CK threat counts, and Organization-Defined Parameters.

### Control Baseline Comparison
Side-by-side comparison of LOW, MODERATE, and HIGH impact security baselines from SP 800-53. See exactly what controls are added at each level, broken down by control family, so you know precisely what each baseline commitment requires.

### Revision Changes
A side-by-side view of what changed between framework revisions (CSF v1.1 to v2.0, SP 800-171 Rev 2 to Rev 3), built directly from NIST's official transition crosswalks. Each current element is classified as carried over, restructured, or new.

### Compliance Advisor
A decision-support tool for organizations. Select your type (federal agency, contractor, healthcare, financial services, small business, cloud provider, or critical infrastructure) and receive a personalized compliance pathway showing exactly which NIST frameworks and controls apply to your situation.

### Learning Paths
Guided educational walkthroughs organized by difficulty level. From beginner overviews of the CSF framework to advanced deep-dives into control implementation.

### Additional Features
- **Organization-Defined Parameters:** ODPs surfaced on SP 800-53 controls and SP 800-171 requirements
- **OLIR Provenance:** every cross-framework mapping cites its source reference, status, and whether it is derived
- **Publication Timeline:** 25 years of NIST publications across every series, showing evolution and supersession
- **Glossary:** Complete NIST cybersecurity terminology reference
- **Insights & Statistics:** Analytics dashboard with ecosystem-wide metrics
- **Global Search:** Instant full-text search across all publications, controls, and requirements
- **Command Palette:** Quick keyboard navigation (Ctrl+K / Cmd+K)
- **Dark + Light Mode:** Full theme support
- **Mobile Responsive:** Works on desktop, tablet, and phone

---

## Platform Stats

| Metric | Count |
|--------|-------|
| NIST Publications | 67 |
| Security Controls & Enhancements | 1,196 |
| Control Families | 20 |
| CSF 2.0 Subcategories | 106 |
| CSF 2.0 Implementation Examples | 363 |
| SP 800-171 Rev 3 Requirements | 97 |
| Cross-Framework Mappings (OLIR) | 1,700+ |
| MITRE ATT&CK Techniques | 49 |
| Knowledge Graph Nodes | 1,996 |
| Knowledge Graph Edges | 7,586 |
| Interactive Pages | 15 |
| API Endpoints | 12 |

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Next.js 16 (App Router, Turbopack) |
| Language | TypeScript 5.9 |
| UI | React 19 |
| Styling | Tailwind CSS v4 |
| Visualization | D3.js v7 (force-directed graphs, coverage maps) |
| Data Layer | In-memory knowledge graph (30 JSON data files) |
| Authoritative Sources | NIST CPRT + OLIR + OSCAL (machine-readable ingestion) |
| Testing | Vitest (unit, integration, and data-integrity gate) |
| Hosting | Vercel (Edge Network) |
| Architecture | Server-side API routes + client-side interactivity |

---

## The NIST Ecosystem Covered

| Domain | Key Publications |
|--------|-----------------|
| Cybersecurity | CSF 2.0, SP 800-53 Rev 5, SP 800-171 Rev 3, SP 800-37 (RMF) |
| Privacy | Privacy Framework v1.0, SP 800-188 |
| AI & Machine Learning | AI RMF 1.0, AI 100-2, NISTIR 8596 (Cyber AI Profile) |
| IoT Security | NISTIR 8228, 8259, 8259A, 8259B, 8425 (Cyber Trust Mark) |
| Risk Management | SP 800-30, SP 800-39, SP 800-37, NISTIR 8286 series (A-D) |
| Supply Chain | SP 800-161 Rev 1, NISTIR 8276 |
| Cloud | SP 800-144, SP 800-145, SP 800-210 |
| Cryptography | SP 800-57, SP 800-175B, FIPS 140-3, FIPS 197, FIPS 186-5 |
| Cross-Framework | CIS Controls v8.1, PCI-DSS v4.0.1, ISO/IEC 27001, HIPAA Security Rule |
| Sector Profiles | Manufacturing (8183r1), Satellite (8401), PNT/GPS (8323r1), Ransomware (8374) |
| And more... | 67 total publications across SP 800, SP 1800, FIPS, NISTIR, and CSWP series |

---

## Who Is This For?

- **Security Engineers:** Quickly find which controls mitigate specific threats
- **Compliance Officers:** Navigate baseline requirements and generate compliance pathways
- **CISOs & Risk Managers:** Visualize coverage gaps across frameworks
- **GRC Analysts:** Explore authoritative cross-framework mappings (CSF to SP 800-53 to ATT&CK, plus 800-171, CIS, PCI, ISO, HIPAA)
- **Government Contractors:** Work through SP 800-171 Rev 3 requirements and CMMC alignment
- **Students & Educators:** Learn NIST standards through interactive exploration
- **Federal Agencies:** Understand full RMF implementation requirements
- **Small Businesses:** Get personalized guidance through the Compliance Advisor

---

## Why I Built This

Navigating the NIST cybersecurity standards ecosystem is overwhelming. Publications reference each other across series, controls map to multiple frameworks, and threat techniques cut across all of them. Existing tools are either paywalled, static PDFs, or disconnected spreadsheets - and the mappings between frameworks are notoriously hard to trust.

NIST Mapper makes the entire ecosystem explorable in one place - free, visual, and sourced directly from NIST's authoritative machine-readable data. Whether you're a security professional mapping controls to threats, a contractor working through SP 800-171, a student learning about CSF 2.0, or a small business trying to figure out where to start with compliance, this platform gives you immediate clarity you can rely on.

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
