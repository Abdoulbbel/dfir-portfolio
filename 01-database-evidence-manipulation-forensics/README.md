# Forensic Investigation of Database Evidence Manipulation

**Type:** Independent academic research project
**Focus area:** Digital forensics · Binary/executable-level analysis · Evidence integrity
**Tools:** IDA Pro, disassembly/static analysis techniques, forensic documentation practices

---

## Overview

Relational databases are a primary target for evidence tampering in fraud, insider-threat, and compliance investigations — an attacker (or malicious insider) with sufficient access can alter records and, critically, alter the low-level program logic that should detect or log that alteration. This project investigated how unauthorized manipulation of database evidence can be identified at the binary and executable level, rather than relying solely on higher-level application logs that a sophisticated attacker could also tamper with.

## Objective

Design and execute a forensic investigation methodology capable of detecting unauthorized manipulation of database evidence by examining the compiled program structures and security-relevant functions directly, and produce a repeatable process that other investigators could apply to similar relational database environments.

## Methodology

1. **Scoping & evidence acquisition** — Identified the relevant executable/binary components of the database environment under investigation and preserved them for offline analysis, following standard forensic handling practices to maintain evidence integrity.
2. **Static binary analysis** — Used IDA Pro to disassemble the target binaries, mapping out program structures and identifying functions responsible for security-relevant operations (access control, logging, integrity checks).
3. **Tamper identification** — Compared the disassembled structures and function logic against expected/baseline behavior to identify tampered program structures — points where the compiled logic had been altered to mask or enable unauthorized database manipulation.
4. **Chain-of-custody documentation** — Logged each analysis step, tool version, and finding in a structured forensic case report, so the investigation would hold up to scrutiny and could be independently reproduced.
5. **Methodology generalization** — Distilled the process into a repeatable methodology applicable to other relational database environments facing similar integrity questions, rather than a one-off analysis.

## Key Findings

- Demonstrated that unauthorized manipulation of database evidence can leave detectable traces at the binary/executable level, even when application-layer logs appear clean.
- Identified specific categories of tampered program structures and security-relevant functions that are common targets for this type of manipulation.
- Produced a documented, reproducible forensic methodology — not just a single case finding — intended for reuse in similar relational database integrity investigations.

## Chain of Custody & Evidence Handling

All analysis was conducted on preserved copies of the target binaries, never the live environment, with each step (acquisition, tool, timestamp, analyst action) logged to maintain a defensible chain of custody consistent with forensic best practice.

## Skills Demonstrated

`Digital Forensics` `Binary/Executable Analysis` `IDA Pro` `Reverse Engineering Fundamentals` `Chain of Custody Documentation` `Forensic Methodology Design` `Technical Report Writing`

## Research Presentation

This work was presented at the International Conference on Sustainable AI for Cybersecurity (JIMS Greater Noida, India) and, in an extended AI-driven form, at the 31st FAI International Conference 2026 (Poornima University, India).

---
*Academic research project conducted as part of an M.Tech in Information Security and Cyber Forensics. Details of the specific target environment have been generalized for public disclosure.*
