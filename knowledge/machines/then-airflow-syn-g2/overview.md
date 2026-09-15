---
type: Document
title: THEN-Airflow SYN G2 / SYN1200 G2 — maintenance overview
description: Machine-level entry point for the THEN-Airflow SYN G2 / SYN1200 G2 dyeing machine, order 37029530-31 — what each specialized maintenance record covers, how to use them for diagnosing electrical and mechanical faults, and the knowledge boundaries that remain outside the corpus.
status: stable
order: 1
generated: { by: "human:hanif", at: 2026-09-15T13:37:01Z }
ksor:
  audience: [public]
  owner: "human:hanif"
  approval: { by: "human:hanif", at: 2026-09-15T13:37:01Z }
---

## Purpose

This record is the machine-level entry point and navigation map for the
THEN-Airflow SYN G2 / SYN1200 G2 maintenance knowledge record. It exists to
help maintenance personnel and agents diagnosing electrical and mechanical
faults in the unit find the correct specialized record quickly. It carries no
technical detail of its own beyond the identity and boundaries below; every
documented fact lives in the specialized records it links to.

## Machine Identity

Only confirmed identity, as recorded in the approved records:

- The machine is the **THEN-Airflow SYN G2 / SYN1200 G2** high-temperature
  air-flow dyeing machine, **order 37029530-31** (`electrical.md`,
  `safety.md`).
- The operator manual is the THEN-Airflow SYN G2 使用说明书 v2.0 by THEN
  Machinery (特恩机械有限公司, THEN Machinery (HK) Ltd.) (`operation.md`).
- The electrical drawing set **UXLA00379** and the installation drawing set
  **IB29530/B/C/D** are FONG'S EUROPE drawings for the SYN1200 G2, order
  37029530-31 (`electrical.md`, `installation.md`).
- **IBAK159** is a FONG'S EUROPE SYN-family valve/pneumatic sheet relied on by
  the injection-system and operating records (`injection-system.md`, `operation.md`).

No further model or order relationship is asserted here.

## Knowledge Coverage

- [electrical.md](electrical.md) — electrical control and diagnostic
  signals: control, fault-signal, interlock, emergency-off and analog-signal
  references read from the UXLA00379 drawing set.
- [safety.md](safety.md) — manufacturer safety boundaries and documented
  fault-response context: electrical, pressure, temperature, mechanical,
  chemical and emergency-stop hazards, and the manufacturer's fault responses.
- [installation.md](installation.md) — installation, utility, connection and
  physical installation context from the IB29530 drawing set and the THEN
  manual and safety guideline.
- [operation.md](operation.md) — manufacturer-supported operating states,
  operating conditions and setpoints, normal and abnormal indications, and
  documented fault-to-operating-condition relationships.
- [injection-system.md](injection-system.md) — injection-system
  identification, drawing-set injection signals, and the source limitations
  of the IBAK159 sheet.

## Diagnostic Use

- Start here for machine and record context, then follow the specialized
  record that matches the fault — electrical signals, safety/diagnostic
  hazards, installation/utilities, operating context, or injection system.
- Treat **Not documented** as an explicit knowledge boundary, not as an
  invitation to infer. The records mark their gaps deliberately so that
  undocumented values are never guessed.
- OCR-derived labels from the image-only drawing sheets (UXLA00379, the
  IB29530 set, IBAK159) must be verified against the original sheet before
  use in maintenance.

## Important Knowledge Boundaries

The following are preserved unresolved, exactly as the sources leave them:

- **Injection quantity / orifice selection** is **Not documented** in the
  available source set (`injection-system.md`).
- The governing **IBAK159 machine-type column for the SYN1200 G2** is
  **unresolved** — the sheet does not name SYN1200 (`injection-system.md`).
- **Ambiguous OCR tags** (for example V117 vs. V111/V112, and V411 vs. V421,
  on IBAK159) must be verified against the original sheet; none is asserted
  as a definite tag (`injection-system.md`, `operation.md`).
- **PLC logic, wiring and terminal numbers, alarm codes, setpoints, repair
  procedures and maintenance intervals** not printed by the sources remain
  outside the corpus (`operation.md`, `electrical.md`, `safety.md`,
  `injection-system.md`).

## Safety Boundary

`safety.md` is the authoritative machine safety record and must be consulted
before any maintenance intervention on the unit. Nothing in this overview, or
in the records it links to, overrides it, bypasses an interlock, or authorizes
work on a hot, pressurized or energized machine.

## Related Records

- [electrical.md](electrical.md)
- [safety.md](safety.md)
- [installation.md](installation.md)
- [operation.md](operation.md)
- [injection-system.md](injection-system.md)

## Sources / Provenance

This overview is distilled from the five approved records above. Those records
derive from the textile-machinery source set committed under
`sources/textile-machinery/` — the THEN operator manual and safety guideline,
and the FONG'S EUROPE drawing sets UXLA00379, IB29530/B/C/D and IBAK159. Each
specialized record carries its own full source list with confidence labels;
they are not duplicated here.