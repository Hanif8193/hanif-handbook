---
type: Document
title: THEN-Airflow SYN G2 / SYN1200 G2 — injection-system reference
description: Injection-system identification and boundary facts for the THEN-Airflow SYN G2 / SYN1200 G2 dyeing machine — the IBAK159 valve-inventory and machine-variant sheet read as far as it can be trusted, the drawing-set injection signals, and the sampling safety boundary — noting that injection quantity and orifice-selection figures are Not documented in the sources.
status: stable
order: 6
generated: { by: "human:hanif", at: 2026-09-15T13:22:47Z }
sources:
  - id: bak
    resource: sources/textile-machinery/IBAK159.pdf
    title: IBAK159 valve/pneumatic sheet, SYN machine family - FONG'S EUROPE GMBH
  - id: then
    resource: sources/textile-machinery/THEN高温气流染色机SYN G2.pdf
    title: THEN-Airflow SYN G2 使用说明书 (Operator Manual), v2.0 - THEN Machinery
  - id: safety
    resource: sources/textile-machinery/特恩高溫氣流染色機SYN G2安全指引.pdf
    title: THEN-AIRFLOW SYN G2 安全指引 (Safety Guideline), v1.0 - 特恩机械有限公司 (THEN Machinery (HK) Ltd.)
  - id: uxla
    resource: sources/textile-machinery/37029530~531  UXLA00379.pdf
    title: UXLA00379 electrical drawing set, SYN1200 G2, order 37029530-31 - FONG'S EUROPE GMBH, 2012
ksor:
  audience: [public]
  approval: { by: "human:hanif", at: 2026-09-15T13:22:47Z }
  owner: "human:hanif"
---

> [!CAUTION]
> IBAK159 is an image-only scan with no text layer. Every value or label taken
> from it is **[OCR]** and must be verified on the original sheet before it is
> used for maintenance. The intended headline topics of this record — injection
> quantity and orifice selection — are **Not documented** in the sources; §3
> states this plainly rather than supplying guessed numbers. This record is
> diagnostic context, not an operating or repair instruction.

## 1. Purpose / Scope

This record documents the injection-system facts for ONE machine — the
THEN-Airflow SYN G2 / SYN1200 G2 high-temperature air-flow dyeing machine,
order 37029530-31 — that the sources actually support, as context for
diagnosing electrical and mechanical faults in the injection circuit. Its
primary source is the single-page drawing IBAK159 [^bak]; the operator manual,
safety guideline and electrical drawing set [^then][^safety][^uxla] are used
only to bind names and boundaries.

It intentionally does not duplicate the approved records: the injection-drive
signals are treated in full in `electrical.md` and summarized in
`operation.md` (§4–§6), and the sampling/liquor-drain boundaries belong to
`safety.md`. This record adds what those do not: the IBAK159 valve inventory,
its SYN-family variant columns, and the explicit **Not documented** findings on
injection quantity and orifice selection.

## 2. Machine and Source Context

- **IBAK159** is a single-page, image-only (no text layer) FONG'S EUROPE
  drawing carrying an ISO 16016 notice in German and English. Its title block
  is only partially legible by OCR — the part number field reads "IBAK159"
  with a "Revisiore" (revision) field; the drawing title itself did not OCR
  [OCR] [^bak]. It is the same sheet the operating record reads as the
  pneumatic-valve sheet (operation.md §9) [^bak].
- Its layout is a **valve/tag inventory table crossed with SYN-family
  machine-type columns** (see §4 and §5) [OCR].
- The electrical drawing set for this same order names the injection circuit
  explicitly [OCR] [^uxla]:
  - drawing index: "Injection pump FQ, Addition Pump AT1", "Injection And
    Power\Rinse Valve VPR", "Injection Spray Rinse Control";
  - PLC overview signals: "injection pump trouble", "injection pump ON",
    "feed-back injection pump", "injection interlock";
  - analog channels: "nominal value injection pump U101", "temp.injection
    P100/B1105", "flow injection";
  - control sheets: "air bubble injection", "back-flow valve AT1",
    "cooling water reflow VK".
- The operator manual's only injection-word references are the panel lamp and
  the loading step that uses it [confirmed] [^then]:
  - §2.1 operator-panel item **2.9 — 同步指示灯 锁住喷射口** (synchronizing
    indicator lamp — injection-port lock);
  - §7.1 (loading) instructs: keep pressing the synchronizing indicator lamp
    2.9 until the fabric head has passed through the air flow.

## 3. Injection Quantity / Orifice Selection — Not documented

The headline topics cannot be filled from this source set and are written here
as an explicit gap rather than a guess:

- **Injection quantity** (litres per cycle, per process step, or per machine
  variant): **Not documented**. IBAK159 prints no flow-rate or quantity
  figures that OCR can read; the operator manual contains none.
- **Orifice / nozzle size and geometry**: **Not documented**. No orifice
  diameter, nozzle type, or injection-nozzle configuration is legible on
  IBAK159 or present in the other sources ([interpretation] the manual's two
  references — the fabric head led to the PTFE inlet during loading (§7.1) and
  the fabric threaded through the nozzle into the storage slot during unloading
  (§10.4) — are fabric-passage elements, not injection-size or orifice
  figures).
- **Per-process injection setpoints**: **Not documented**. The drawing set
  names the injection channels and drives (see §6) but prints no limits or
  setpoints.

## 4. Machine Variants or Applicable Models

- IBAK159's table header yields four machine-type strings [OCR] [^bak]:
  - AFE50/SYN50/SYN60G
  - FE25/0/0G/3
  - AFE675/SYN750/SYN900G
  - AFE450/SYN500/SYN600
  with a "TYPE" header and a "*)OPTION" marker also read on the sheet.
- The sheet does **not** print "SYN1200" anywhere that OCR could read, so
  **which column governs the SYN1200 G2 of order 37029530-31 is Not
  documented** ([interpretation] the SYN-containing labels imply the SYN
  family is the intended reader set; the specific variant row for this machine
  must be read from the sheet).

## 5. Source Tables / Dimensions / Relationships

- **Table structure**: rows are valve tags; the four machine-type columns
  carry a per-cell entry (count or denomination) that did **not** OCR
  intelligibly — standard-res reads produced fragments such as "e70/10x2",
  "2x3x6.52", "29/12x2", "823/6x1" that cannot be trusted. These are recorded
  only as "verify on the sheet", never reported as values [OCR] [^bak].
- **Tag rows read by OCR** (verify each on the sheet): V811, V856, V821, V900,
  V117 — OCR unstable; also read as V111/V112; verify on the original sheet —
  VA2, VAI, V113, V105, V101, V102, VS, V854, V808, V311, VBZ, V356, B1380,
  V355, VV3, V411/V421 — OCR ambiguous; verify on the original sheet — VBD,
  V359, V051, V147, VEL, V142, VE2, V300, VDZ, V400, VDD, V108, VSP3 [OCR]
  [^bak]. This matches the tag family already recorded in operation.md §9 with
  the same verification caveat.
- **Note fragments in the lower sheet area** read by OCR: "by means of
  frequency converter", "NTS", and "8OLtr." (possibly "8 Ltr."). None can be
  attributed to a specific component with confidence; treat them as leads to
  check on the sheet, not as values [OCR] [^bak].
- **Dimensions**: an "DN 6" fragment appears in the sheet's upper area but its
  row/column context is unreadable; nominal diameters for the individual
  valves are therefore **Not documented** [OCR] [^bak].

## 6. Diagnostic Relevance

What this record supports for fault work [OCR unless marked]:

- **Identification against the sheet**: with a suspected injection/rinse fault
  and a physical valve tag in hand, the IBAK159 inventory is the part-identity
  list for this machine's valve module. [interpretation] The tag families that
  DO overlap functions documented elsewhere are the ones already flagged in
  operation.md §9 — VEL (air-feed valve), VE2 (aeration valve), V300 (= VD,
  the salt / reflux valve), VBZ (drain), VSP3 (rinsing valve) — every other
  tag's function mapping is **Not documented**.
- **Injection drive** (cross-reference the electrical record, which treats
  these fully [^uxla]): injection pump drive U101 with the "nominal value
  injection pump" output channel; status signals "injection pump ON",
  "feed-back injection pump", "injection pump trouble"; an "injection
  interlock" signal is present on the PLC sheets [OCR].
- **Injection / power-rinse valve**: the drawing index names "Injection And
  Power\Rinse Valve VPR"; the electrical record confirms B163 as the "rinsing
  valve VPR" input/channel (electrical.md). [interpretation] A stuck or absent
  B163 feedback would read out through the control-valve feedback channels of
  the electrical record, not through any limit value documented here.
- **Injection flow and temperature channels**: "flow injection" plus
  "temp.injection P100/B1105" are measurable analog channels; the drawing set
  prints no normal range, so any diagnosis against them must rest on the
  machine's own behavior, not on a documented figure [OCR].
- **Operator signal**: §2.1/§7.1 of the manual — the synchronizing lamp 2.9
  (injection-port lock) is the operator's signal during loading [confirmed]
  [^then]; the manual prints no unloading use for it. A lamp that fails to
  hold the fabric pass in the air flow is an observation, not a documented
  fault code.

## 7. Safety / Boundary Notes

- **Sampling from the working door** — the safety guideline states the
  boundary that governs the injection circuit: before opening, cool the dye
  liquor below 80 °C (176 °F), depressurize the machine, and **shut off the
  injection device beforehand** [confirmed] [^safety].
- The injection lines carry hot, pressurized dye liquor; all general door /
  filter / manhole and liquor-drain conditions of `safety.md` apply to work on
  the injection circuit. This record is context, never an override, and the
  sources document no way to bypass an interlock — none is provided here
  either.
- No step-by-step repair, adjustment, commissioning, or bypass procedure is
  documented by any source for the injection system; accordingly none appears
  here (§8).

## 8. Not documented

- Injection quantity per machine variant, per orifice, per process step; all
  orifice/nozzle sizes and geometry; injection flow rates; per-process
  injection setpoints and any "normal" values for the "flow injection" and
  "temp.injection" channels.
- The reading of IBAK159's per-cell table (per-variant counts), its full
  title-block text, its nominal diameters, and whether its "8 Ltr." / "DN 6"
  fragments belong to any injection component.
- Which of the four machine-type columns applies to SYN1200 G2, order
  37029530-31.
- Function mapping for the majority of IBAK159 tags; PLC addresses, terminal
  numbers, wiring details, alarm codes, maintenance intervals, and any
  repair/adjustment/commissioning procedure.

## Sources

[^bak]: `sources/textile-machinery/IBAK159.pdf` — IBAK159 valve/pneumatic sheet, SYN machine family — FONG'S EUROPE GMBH. Single-page image-only scan; title block and table content only partially OCR-readable ([OCR]); verify every tag and value on the sheet.

[^then]: `sources/textile-machinery/THEN高温气流染色机SYN G2.pdf` — THEN-Airflow SYN G2 使用说明书 (operator manual), v2.0; THEN Machinery. Text layer readable; contents [confirmed]: operator-panel items (§2.1, incl. 2.9 synchronizing lamp — injection-port lock), loading and fabric guidance through the air flow (§7.1), fabric threading through the nozzle into the storage slot (§10.4).

[^safety]: `sources/textile-machinery/特恩高溫氣流染色機SYN G2安全指引.pdf` — THEN-AIRFLOW SYN G2 安全指引 (safety guideline), v1.0; 特恩机械有限公司 (THEN Machinery (HK) Ltd.). Text layer readable; contents [confirmed]: sampling boundary — cool below 80 °C (176 °F), depressurize, and shut off the injection device beforehand (p. 24), together with the general door / filter / manhole and liquor-drain conditions (p. 20–24).

[^uxla]: `sources/textile-machinery/37029530~531  UXLA00379.pdf` — UXLA00379 electrical drawing set, SYN1200 G2, order 37029530-31; FONG'S EUROPE GMBH. Image-only scan; contents [OCR]: drawing index entries "Injection pump FQ, Addition Pump AT1", "Injection And Power\Rinse Valve VPR", "Injection Spray Rinse Control"; PLC signals "injection pump trouble / ON / feed-back", "injection interlock"; analog channels "nominal value injection pump U101", "temp.injection P100/B1105", "flow injection"; control-sheet items "air bubble injection", "back-flow valve AT1".