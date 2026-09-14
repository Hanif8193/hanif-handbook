---
type: Document
title: THEN-Airflow SYN G2 / SYN1200 G2 — electrical control and diagnostic signals
description: Electrical control, fault-signal, interlock and analog-signal references for the SYN G2 / SYN1200 G2 dyeing machine, read from the UXLA00379 drawing set.
status: stable
order: 2
generated: { by: "human:hanif", at: 2026-09-14T21:21:04Z }
sources:
  - id: uxla
    resource: sources/textile-machinery/37029530~531  UXLA00379.pdf
    title: UXLA00379 electrical drawing set, SYN1200 G2, order 37029530-31 - FONG'S EUROPE GMBH, 2012
  - id: then
    resource: sources/textile-machinery/THEN高温气流染色机SYN G2.pdf
    title: THEN-Airflow SYN G2 使用说明书 v2.0 - THEN Machinery
ksor:
  audience: [public]
  approval: { by: "human:hanif", at: 2026-09-14T21:21:04Z }
  owner: "human:hanif"
---

This record is a diagnostic-reference map for the electrical control and
fault-signal information of ONE machine: the THEN-Airflow SYN G2 / SYN1200 G2
dyeing machine, order 37029530-31 [^uxla]. It is transcribed from the UXLA00379
electrical drawing set (image-only scans, so every label below is OCR-read and
must be verified against the sheet before use) [^uxla], with the machine's
operator-panel indicators cross-referenced from the THEN operating manual
[^then]. It serves the record's stated scope — diagnosing electrical and
mechanical faults in the unit — and nothing in it is a work instruction for
installation, operation or maintenance.

## Confidence labels

- **[confirmed]** — printed precisely in the source and read clearly.
- **[OCR]** — printed in the source but read through OCR of a scanned drawing; the wording may differ slightly from the sheet.
- **[interpretation]** — my reading of context, not a printed label.
- **Not documented** — explicitly absent from these sources.

## Machine electrical identity — [OCR]

Read from the scanned UXLA00379 cover sheet and title blocks [^uxla]; every
value is OCR-read and must be confirmed against the sheet before use:

| Item | Value |
| --- | --- |
| Machine model | SYN1200 G2 |
| Order | 37029530-31 |
| Controller | DYNET |
| Supply voltage / frequency | 400 V / 50 Hz |
| Feed line | 95 mm² + PE + GND |
| Control voltage | 220 V AC / 24 V DC |
| Main isolator rating | 250 A |
| Drawing set | DWG.NO UXLA00379 (revisions R01, R02 observed) |
| Designed / date | Yang WeiGuo, 05-06-2012 (R01) and 10-07-2012 (R02) |
| Approved | PWCHIU |
| Machine builder | FONG'S EUROPE GMBH |
| Customer | International Textile Limited (Pakistan) |

Scope boundary: this record covers ONLY the diagnosis-relevant electrical
information of the unit — fault / trouble signals, interlocks, emergency-off,
motor / blower / pump fault signals, temperature- and pressure-related signals,
analog I/O, and the inverter references printed in the drawing set. Installation,
layout, general operation and maintenance are out of scope here and appear only
as boundaries or cross-references: installation has a planned separate record,
and the THEN operating manual is cited only for the operator-facing fault
indicators. Mechanical fault signals (winch, plaiter, blower) are covered only
as the electrical signals that report them.

## What the drawing set contains — [OCR]

The set is the machine's electrical control package. Its drawing index lists,
among others, the following sheet families (list read by OCR from the index
sheets [^uxla]):

- PLC Overview 1 and 2
- Analog In/Output Overview
- Pneumatic-Module Mounting Plate 1 and 2
- Per-store sheets for winch stores 1-4: Power Unit, Control, Run-of-Fabrics Monitoring, "Part 1. Man." [OCR]
- Terminal Diagrams 1-6
- Legend
- Inverter Parameter
- Flow Meter Parameter Setting (KROHNE)
- Network Connection
- Electric Kilowatthour Meter

[OCR] Sheet codes (for example the UT… block codes and the =A/… / =LIB/…
sequence references) and the per-store numbering were read with some
uncertainty; verify on the index pages if needed. The label "Part 1. Man." is
not expanded in the index — its meaning is [interpretation] unconfirmed
(possibly take-up or fabric-guidance related).

## Fault and trouble signals — [OCR][^uxla]

Printed labels on the PLC Overview sheets, grouped by function. The first
column shows the printed prefix; the prefixes are printed but their meaning is
[interpretation] unresolved, so treat them as labels, never as definitive PLC
addresses.

### Blower
| Prefix (printed) | Signal label (printed) |
| --- | --- |
| 6.1 | blower revolution |
| 6.2 | blower reset |
| 6.3 | blower on |
| 6.4 | feed-back blower |
| 6.6 | blower current (U102) |
| — | trouble blower |

### Winches / plaitor (fabric transport) [interpretation]
| Prefix (printed) | Signal label (printed) |
| --- | --- |
| 13.3 / 13.4 | winch 1 forwards / winch 1 backwards |
| 13.5 | winch 1 trouble |
| 17.4 / 17.5 | winch 2 forwards / winch 2 backwards |
| 17.6 | winch 2 trouble |
| 21.4 / 21.5 | winch 3 forwards / winch 3 backwards |
| 21.6 | winch 3 trouble |
| 25.4 / 25.5 | winch 4 forwards / winch 4 backwards |
| 25.6 | winch 4 trouble |
| 13.7 | plaiter on |
| 13.8 | plaiter trouble |
| — | winch reset |
| 44.5 | winch + blower reset |

Store-specific run-of-fabric signals repeat per store (Sp. 1-4):
| Signal label (printed) |
| --- |
| SL run of fab. trouble (Sp. 1-4) |
| light barrier (Sp. 1-4) |
| seam detect. (Sp. 1-4) |
| part 1. man. (Sp. 1-4) |

### Pumps / motors
| Signal label (printed) |
| --- |
| trouble blower (see Blower) |
| injection pump trouble |
| injection pump ON / feed-back injection pump |
| addition pump trouble |
| DA mixing pump ON |
| rinsing motor ON |
| pump cooling (Y100) [printed with an output tag] |
| motor trouble (operator-panel group) |
| winch trouble (operator-panel group) |

## Interlocks and emergency-off — [OCR][^uxla]

Printed labels from the PLC Overview sheets; their functions are [interpretation]
inferences:

| Signal label (printed) | Function [interpretation] |
| --- | --- |
| EMERG.-OFF input | emergency-off input to control |
| signal cut-off | printed signal; function not expanded |
| press. interlock | pressure interlock |
| Temperature interlock | temperature interlock |
| injection interlock (per store) | injection interlock |
| flasher | printed signal; interpreted as a fault beacon, unconfirmed |

Operator-panel indicators — [confirmed] (manual text layer) — THEN operating
manual [^then]: the panel carries a temperature-lock lamp, a guide-roller fault
indicator (导布轮故障; [interpretation] the winch / fabric-drive fault signal,
not linked in the sources to the drawing's "winch trouble" labels), a motor
fault indicator (马达故障), and an emergency-stop control (紧急停运). These are
operator-facing indicators; the sources do not link them to specific drawing
labels.

## Analog input / output signals — [OCR][^uxla]

Printed on the Analog In/Output Overview sheet (4-20 mA channels).

| Signal label (printed) | Kind | Reference printed |
| --- | --- | --- |
| blower revolution | output | U102 |
| blower current | output | U102 |
| winch revolution Sp. 1-4 | output | U131-U134 |
| plaiter revolution | output | U105 |
| nominal value injection pump | output | U101 |
| temperature additive tank AT1 | input | — |
| temperature injection | input | P100, B1105 |
| temperature Tda | input | B1100 |
| static pressure FK | input | — |
| level AT | input | — |
| level d.a. | input | — |
| control valve VHK | input | B136 |
| metering valve VVD | input | B356 |
| rinsing valve VPR | input | B163 |
| control valve VDJ | input | B109 |
| flow meter | input | — |
| flow injection | input | — |
| water counter | input | — |

Module and channel tags are also printed (for example 1ANA_HS, 2ANA_HS,
1ANA_STM, 2ANA_STM, I/0_TBL and PT1-PT6 channel labels); their exact mapping
is [OCR] and not asserted here.

## Temperature- and pressure-related electrical signals — [OCR][^uxla]

Printed labels from the PLC Overview and analog sheets, collected here for fault
diagnosis; the values themselves are not documented in the sources.

| Signal label (printed) | Reference printed |
| --- | --- |
| Temperature interlock | — |
| press. interlock | — |
| temp. main current cabinet | B0000 |
| temp. warm water | B1107 |
| temp. operator's module | — |
| temperature additive tank AT1 | — |
| temperature injection | P100, B1105 |
| temperature Tda | B1100 |
| static pressure FK | — |
| level AT, level d.a. | — |

## Inverter / VFD references — [OCR][^uxla]

- The drawing index lists an "Inverter Parameter" sheet and a "Blower Frequency
  Control" sheet. Their contents are NOT transcribed in this record.
- [interpretation] These two index entries show that inverter-driven drives are
  part of the machine's drive scheme (at least for blower frequency control).
  The injection pump's own drive arrangement belongs to the separate
  injection-system source and its planned record, not this one.

Danfoss VLT-2800 / FC-300 component manuals exist in the sources but are
covered by separate component records; they are not cited here.

## What is NOT documented in this record

Out of scope by design: installation, general operation and maintenance are not
authoritative here and are not covered. What the cited sources also do not
provide is listed below:

- **No fault-resolution procedure exists for any signal above** in either
  source. The recording documents what the signal is, not what to do about it.
  If a fault occurs, the response procedure is not documented in this record
  and must come from the machine's own service documentation or the
  manufacturer before any action.
- PLC bit addresses: the PLC Overview sheets carry axis labels (for example
  A0.0, E0.x, E1.x) whose meaning is [OCR] unresolved. No address is asserted.
- Terminal numbers and wire numbers: not read from the scanned sheets.
- Inverter parameter values, setpoints and thresholds: not transcribed.
- Voltages beyond the cover-sheet values: not documented.
- The printed numeric prefixes on the PLC sheets (for example 13.5, 44.8) are
  labels whose meaning is [interpretation] unresolved — not addresses.

> [!WARNING]
> The machine is fed at 400 V / 50 Hz, its control circuits use 220 V AC / 24 V
> DC, and its main isolator is rated 250 A (cover-sheet values [^uxla]). The
> machine therefore contains hazardous electrical energy, and fault diagnosis
> may involve energized equipment. Before any physical intervention, apply the
> site-approved isolation / lockout procedure and verify that the equipment is
> de-energized. Only appropriately qualified personnel may perform electrical
> work on this machine. This record is a diagnostic reference, not a work
> instruction, and does not describe safe isolation. All values and signal
> labels are OCR-read and must be confirmed against the drawing sheets before
> they are used to identify a component.

## Sources

[^uxla]: `sources/textile-machinery/37029530~531  UXLA00379.pdf` — UXLA00379 electrical drawing set, SYN1200 G2, order 37029530-31; FONG'S EUROPE GMBH; sheets dated 05-06-2012 and 10-07-2012.

[^then]: `sources/textile-machinery/THEN高温气流染色机SYN G2.pdf` — THEN-Airflow SYN G2 使用说明书 (operator manual), v2.0; THEN Machinery.