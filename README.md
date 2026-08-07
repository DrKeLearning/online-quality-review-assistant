# OQRA — Online Quality Review Assistant 🤖📚

[![Version](https://img.shields.io/badge/version-2.0.0-blue.svg)](https://github.com/your-username/oqra)
[![Rubric Framework](https://img.shields.io/badge/Framework-USF%20Green%20%26%20Gold%20v2.0-emerald.svg)](#knowledgebase--rubric-framework)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-brightgreen.svg)](https://github.com/your-username/oqra/graphs/commit-activity)

**OQRA (Online Quality Review Assistant)** is an AI-powered diagnostic system prompt framework designed to evaluate online and hybrid course artifacts against quality assurance standards. 

Engineered with a **zero-assumption diagnostic pipeline**, OQRA minimizes AI hallucinations and ensures evidence-based, audit-ready evaluations of syllabi, course maps, lesson modules, and assessment prompts.

---

## 📋 Table of Contents
- [Key Features](#-key-features)
- [Diagnostic Pipeline Architecture](#-diagnostic-pipeline-architecture)
- [Knowledgebase & Rubric Framework](#-knowledgebase--rubric-framework)
- [Repository Structure](#-repository-structure)
- [Getting Started](#-getting-started)
  - [Deployment Options](#deployment-options)
  - [Usage Workflow](#usage-workflow)
- [Standardized Output Schema](#-standardized-output-schema)
- [Versioning & Changelog](#-versioning--changelog)
- [Contributing](#-contributing)
- [License](#-license)

---

## ✨ Key Features

* **Strict Evidence Grounding:** Eliminates guesswork and hallucinations by enforcing pure zero-assumption diagnostic rules.
* **5-Step Diagnostic Protocol:** Executes a sequential evaluation algorithm (Standard Extraction $\rightarrow$ Evidence Gathering $\rightarrow$ Gap Analysis $\rightarrow$ Verdict Determination $\rightarrow$ Reporting).
* **Standard ID Indexing:** Native tracking and reporting using granular standard codes (e.g., `GR-S1.1` to `GR-S8.7` for Green standards, `GO-S4.6` to `GO-S7.5` for Gold standards).
* **Objective Verdict Thresholds:** Categorizes compliance using strict passing thresholds (`MET`, `NOT MET`, `INSUFFICIENT DATA`).
* **Actionable Instructional Design Advice:** Generates precise recommendations whenever a course artifact fails or lacks documented proof for a standard.

---

## ⚙️ Diagnostic Pipeline Architecture

OQRA operates using a structured 5-step diagnostic loop to evaluate course artifacts:

```mermaid
graph TD
    A[Upload Course Artifacts] --> B[Step 1: Extract Standard Rules & Thresholds]
    B --> C[Step 2: Search Artifacts for Direct Evidence]
    C --> D[Step 3: Analyze Gaps against Aligned/Violating Criteria]
    D --> E[Step 4: Determine Verdict: MET / NOT MET / INSUFFICIENT DATA]
    E --> F[Step 5: Generate Standardized Audit Report]
