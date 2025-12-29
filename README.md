# systems-design-automation
A systems design project demonstrating secure, human-in-the-loop automation using BPMN, cloud infrastructure, and AI.

## Overview
This project demonstrates how modern software systems can be designed to automate complex, real-world workflows while remaining ethical, auditable, and human-controlled.

I designed and implemented an end-to-end **job application preparation system** that streamlines how job opportunities are evaluated and prepared for — without removing human judgment or accountability from the process.

The focus of this project is not “automation for automation’s sake”, but **good systems design**: clear process modelling, secure infrastructure, controlled AI usage, and scalability.

---

## Problem Statement
Applying for roles at scale often creates two problems:
1. Manual processes are slow and inconsistent
2. Fully automated systems risk inaccuracies, hallucinations, or misuse

This project explores how to balance **efficiency and responsibility** by designing a system that automates repetitive work while enforcing review gates and traceability.

---

## System Design Approach

The system was first modelled using **BPMN 2.0** to clearly define:
- Inputs and outputs
- Decision points
- Parallel processing
- Human approval stages
- Failure handling

Only once the process was well-defined was it implemented technically.

---

## Architecture & Implementation

### Core Components
- **Process Modelling:** BPMN 2.0 (pools, lanes, gateways, loop tasks)
- **Automation Engine:** n8n (self-hosted)
- **AI Integration:** OpenAI (prompt engineering, relevance scoring, content generation)
- **Cloud Infrastructure:** Google Cloud Platform
- **Secure Access:** Cloudflare Zero Trust Tunnel
- **Data Storage:** Google Docs & Google Sheets APIs

### Workflow Summary
1. Job listings are aggregated from multiple sources
2. Data is normalised and de-duplicated
3. Roles are evaluated using AI-driven relevance scoring
4. For relevant roles, the system generates:
   - Tailored CV
   - Cover letter
   - Professional outreach email
   - LinkedIn message
5. A **mandatory human review step** validates all outputs
6. Approved assets are stored with structured metadata for traceability

---

## Key Design Principles

- **Human-in-the-loop:** No application content is used without explicit approval
- **Auditability:** Every step is observable and repeatable
- **Security-first:** No public exposure of internal systems
- **Scalability:** Designed to evolve from personal use to service or institutional use
- **Ethical AI use:** AI assists decision-making, it does not replace it

---

## Skills Demonstrated

- Software systems design and thinking
- BPMN applied to real-world automation (not theoretical)
- Secure cloud architecture
- Automation orchestration
- Responsible AI integration
- Process governance and documentation
- Problem decomposition and solution structuring

---

## Why This Project Matters
This project reflects how I think about software:
- Start with the **problem**, not the tools
- Design the **system**, not just the code
- Build solutions that are **useful, safe, and explainable**

---

## Notes
Source code is intentionally limited in this repository. 
The emphasis is on **design, architecture, and decision-making**, rather than implementation detail.

Diagrams and supporting artefacts may be added over time.
