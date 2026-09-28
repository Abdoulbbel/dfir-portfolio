# Runtime Integrity Validation in Relational Databases (Memory Forensics)

**Type:** Independent academic research project
**Focus area:** Memory forensics · Runtime integrity validation · Incident timeline reconstruction
**Tools:** WinPMEM, FTK Imager, Volatility 3

---

## Overview

Disk-based and log-based forensics can miss attacks that live entirely in memory — in-memory privilege escalation, transient process tampering, and runtime manipulation that never touches disk. This project investigated whether volatile memory forensics could reliably validate the runtime integrity of a MySQL relational database environment, detecting compromise indicators that would be invisible to traditional static analysis.

## Objective

Design and execute a memory-forensics methodology to validate runtime integrity of a live MySQL database environment, and determine whether in-memory privilege escalation and other runtime tampering could be reliably identified by comparing baseline and manipulated system states.

## Methodology

1. **Baseline capture** — Established a clean baseline of the MySQL environment's expected runtime state before introducing any manipulation.
2. **Memory acquisition** — Acquired volatile memory images from the target environment using WinPMEM and FTK Imager, following forensically sound acquisition procedures to preserve evidence integrity.
3. **Artifact triage** — Used Volatility 3 to triage runtime artifacts and process memory, extracting MySQL process structures, privilege-related artifacts, and other runtime indicators from the memory images.
4. **Baseline vs. manipulated comparison** — Systematically compared the baseline memory state against a deliberately manipulated system state to isolate memory-level differences attributable to tampering rather than normal operation.
5. **Compromise indicator identification** — Identified indicators consistent with in-memory privilege escalation and other integrity anomalies that only manifest at runtime.
6. **Timeline reconstruction** — Documented an incident-style compromise timeline reconstructing the sequence of runtime events from the memory artifacts, in the same format used in real incident response engagements.

## Key Findings

- Confirmed that memory forensics can surface indicators of in-memory privilege escalation in a MySQL environment that would not be visible through disk or log analysis alone.
- Identified specific memory-level differences between baseline and manipulated states that serve as reliable compromise indicators.
- Demonstrated that a structured baseline-vs-manipulated comparison methodology, combined with incident-style timeline reconstruction, produces defensible, reproducible findings suitable for real-world DFIR workflows.

## Skills Demonstrated

`Memory Forensics` `Volatile Memory Acquisition` `Volatility 3` `WinPMEM` `FTK Imager` `Runtime Integrity Analysis` `Incident Timeline Reconstruction` `MySQL/Database Internals`

## Research Presentation

This work was presented at the International Conference on Forensic Science, Cyber Security & Digital Forensics 2026 (Aditya University, India).

---
*Academic research project conducted as part of an M.Tech in Information Security and Cyber Forensics, in a controlled lab environment. Details of the specific target environment have been generalized for public disclosure.*
