---
type: Document
title: THEN-Airflow SYN G2 / SYN1200 G2 — installation context
description: Manufacturer-recorded installation context for the THEN-Airflow SYN G2 / SYN1200 G2 dyeing machine — layout, foundation, utility and connection requirements, and the installation-related conditions relevant to maintenance diagnosis, read from the FONG'S EUROPE IB29530 installation drawing set and the THEN manual and safety guideline.
status: stable
order: 4
generated: { by: "human:hanif", at: 2026-09-15T09:20:26Z }
sources:
  - id: layout
    resource: sources/textile-machinery/IB29530 .pdf
    title: General layout plan, SYN1200 G2, order 37029530-31 - FONG'S EUROPE GMBH
  - id: foundation
    resource: sources/textile-machinery/IB29530A .pdf
    title: Foundation layout plan, SYN1200 G2 - FONG'S EUROPE GMBH
  - id: schematic
    resource: sources/textile-machinery/IB29530B .pdf
    title: Schematic plan (installation and utilities), SYN1200 G2, order 37029530-31 - FONG'S EUROPE GMBH
  - id: scheme
    resource: sources/textile-machinery/IB29530C .pdf
    title: Installation scheme — utility specifications, SYN1200 G2, order 37029530-31 - FONG'S EUROPE GMBH
  - id: fittings
    resource: sources/textile-machinery/IB29530D .pdf
    title: Valves and fittings installation scheme, SYN1200 G2, order 37029530-31 - FONG'S EUROPE GMBH
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
  owner: "human:hanif"
  approval: { by: "human:hanif", at: 2026-09-15T09:20:26Z }
---

This record documents the installation context of ONE machine — the THEN-Airflow
SYN G2 / SYN1200 G2 dyeing machine, order 37029530-31 [^layout][^uxla] — as
printed in the FONG'S EUROPE installation drawing set IB29530, IB29530A-D, with
the machine's construction, installation-site, pressure, utility and safety
requirements cross-referenced from the THEN operating manual [^then] and the
THEN safety guideline [^safety]. It serves the record's stated scope —
supporting diagnosis of electrical and mechanical faults in the unit by
establishing what the machine's installed environment and connections require —
and nothing in it is a work instruction for installation, commissioning,
operation or maintenance.

## Confidence labels

- **[confirmed]** — printed precisely in the source and read clearly (text layer).
- **[OCR]** — printed in the source but read through OCR/WinOCR of a scanned or vector-only drawing; wording, numerals or dimensions may differ slightly from the sheet and MUST be verified against the original drawing before use.
- **[interpretation]** — my reading of context, not a printed label.
- **Not documented** — explicitly absent from these sources.

> [!NOTE]
> The five IB29530 installation drawings carry no text layer (vector/scanned
> sheets). EVERY value taken from them in this record is **[OCR]** and must be
> read off the original sheet before it is used to size, connect, or set
> anything. The THEN manual and safety guideline have text layers, so their
> contents are **[confirmed]** from that text.

## 1. Scope

What this record covers:

- The installation layout sheet and what it places on the machine surroundings.
- The foundation sheet: anchor and dowel pattern, loads, and dimensions.
- The utility and connection requirements at the machine's supply boundary,
  including pressures, pipe connections, and discharge schemes.
- The electrical installation identity (from the UXLA00379 cover sheet).
- The connected valves and fittings the installation sheets name.
- Installation-related safety conditions from the safety guideline.
- What the sources do NOT document, kept as explicit gaps.

Sister records hold the detail: the electrical control and fault signals are the
electrical record's territory [^uxla], and the machine's operating hazards,
interlocks and emergency responses are the safety record's [^safety]. This
record neither repeats nor overrides them.

## 2. Machine / document identity

Read from the IB29530 layout title block and the UXLA00379 cover sheet [^layout][^uxla]:

| Item | Value |
| --- | --- |
| Machine model | SYN1200 G2 |
| Order | 37029530-31 |
| Drawing set (installation) | IB29530 / IB29530A / IB29530B / IB29530C / IB29530D |
| Drawing set (electrical) | UXLA00379 |
| Builder (install drawings) | FONG'S EUROPE GMBH [interpretation] — the IB title blocks did not print a legible builder name in OCR; the attribution follows the shared order 37029530-31 with the UXLA set [^uxla] |
| Builder (electrical drawings) | FONG'S EUROPE GMBH [OCR] |
| Customer | International Textile Limited [OCR] [^uxla] |

The machine's construction, as listed in the operator manual's construction
chapter — vessel, circulation system, circulation pump (hidden behind), heat
exchanger, liquor filter, air filter (within the vessel), addition (dosing)
tank, working platform, blower, take-off roller, winch drive, nozzle, DYNET
control, operator panel and main control cabinet (below the blower) — is
[confirmed] from the manual [^then] and is the vocabulary the installation
sheets assume.

## 3. Installation layout — [OCR][^layout]

The general layout plan (sheet IB29530, A3, not to scale — "NTS" in the title
block) shows the machine with its supply and connection points labelled. Every
item below is OCR-read and must be verified on the sheet:

- Connection points printed on the layout: **compressed air 8 bar**, **soft
  water, max. 3 bar**, a **steam line (DN50)** to the booster, **cooling-water
  return pipeline (DN50)**, **condensate (DN32)** and a further **condensate
  (DN25)** line, **drain (DN20)**, and **water inlet/outlet**.
- The **electrical cabinet** position and the fabric **supply / inlet / outlet**
  arrangement are drawn. The layout labels around the fabric end were partially
  legible in OCR ("supply of fibres") and the exact wording should be confirmed
  on the sheet [interpretation].
- Metric dimension figures printed on the plan (e.g. 1149, 1098, 684, 520, 263,
  160 and an overall figure read as 5900) are [OCR] and must be read off the
  original; the sheet is not to scale, so nothing here should be dimensioned
  from OCR output alone.

## 4. Foundation information — [OCR][^foundation]

The foundation layout plan (IB29530A) prints the anchoring for the machine and,
per the sheet's own note, the fixing of the processing kier and the pump is the
customer's responsibility:

- "**THE PROCESSING KIER AND THE PUMP HAVE TO BE FIXED PROFESSIONALLY AT
  CUSTOMER'S PREMISES.**" [OCR]
- Anchor bolts and dowels — as read by OCR, verify each on the sheet: **16×
  M20×200**, **8× M20** and **4× M20** anchor bolts; **3× M16×160**, **M12×120**
  and **M20×1200** dowels, several marked "erection and fasten at final
  assembly".
- A printed **working-platform load of 20000 N**.
- Printed dimension figures include an overall foundation outline read as
  ~4680, ~3500, and internal figures ~2410.5, ~1594, ~1570, ~1430, ~1250, ~985,
  ~860, ~580, ~520, ~400 and ~130 (mm, [OCR]).

The safety guideline adds the site obligation that the floor loading must meet
the machine's requirement and that an unstable or misaligned installation
endangers life and limb [^safety] [confirmed].

## 5. Utilities and connections

The installation scheme (IB29530C) states the supplies the machine is
connected to — saturated steam, soft water, water, compressed air — and the
scheme/schematic sheets (IB29530C/B) print the pressure and flow requirements.
All figures in this section are **[OCR]** from the vector/scanned sheets and
must be verified against the originals:

- **Saturated steam**: min **6 bar** / max **8 bar** (the sheet's header also
  prints a "MIN 7" steam figure; confirm the printed minimum on IB29530C) with
  impurity limits printed as max **5 g/m³** water content and max **0.5 mg/l**
  oil content.
- **Soft water**: min **2 bar** / max **3 bar** (also printed in psi as ~29–43.5).
- **Water**: min **2 bar** / max **3 bar**.
- **Compressed air**: labelled **8 bar** on the layout and **8–10 bar** on the
  schematic; the schematic prints an **air requirement of max. 7 Nm³/h** for the
  machine (5 Nm³/h for the dye autoclave side).
- **Steam consumption**: heat exchanger **max. 3180 kg/h**; addition (service)
  tank **max. 175 kg/h**.
- **Water flow** printed in the main-pump circuit: **7690 kg/h**.
- A pipes requirement line on the scheme read as "pipes … made of stainless
  steel" [OCR; wording to be confirmed].

The scheme prints two installation notes that define the responsibility and
sizing boundary [OCR]:

- "**All connections led to the machine have to be reduced in their pressure to
  the service pressure of the machine resp. of the heat exchanger systems. The
  execution has to be clarified with the inspection authorities!**"
- Broken lines and parts of plant are **not part of our [the manufacturer's]
  delivery**; a fibre retainer with printed mesh width ~1.25 mm (0.0499") is
  likewise marked **not part of our delivery**.

The safety guideline makes compliance with the connection-diagram pressures
normative for the machine to function correctly [^safety] [confirmed].

## 6. Pressure / steam / water installation context

- The supply pressures above are the pressures required at the machine's
  connection points. The scheme's note — that every connection must be reduced
  to the machine's/heat-exchanger service pressure and cleared with the
  inspection authorities — is the governing rule for the site side [^scheme]
  [OCR].
- Discharge/relief arrangements printed on the scheme: safety let-off locally
  (closed system), an open system (channel) discharge, a separate closed-system
  discharge for hot (HT) drain, condensate and cooling-water backflow paths, and
  a pump drain taken over the roof [^scheme] [OCR]. These connect to the
  high-temperature-drain and safety-valve rules in the safety record [^safety].
- Steam and condensate pipes are to be insulated; the safety guideline requires
  hot pipes to be insulated against accidental contact and condensate-carrying
  lines to be drained (e.g. automatic condensate separator) [^safety]
  [confirmed].
- Safety-valve relieving capacities printed on the schematic [^schematic]
  [OCR]: a **DN50** valve — **steam 1695 kg/h (2175 m³/h)** — and a **G ½"**
  valve — **steam 370 kg/h (483 m³/h)**. Two further printed labels read
  "**set pressure 8 bar**" (in the main-pump / free-outlet area) and "**set
  pressure 3 bar**" (cooling water, soft); their exact assignment is
  [interpretation] and must be confirmed on the sheet.
- For rinsing the transmitter line the scheme prints a required water pressure
  of the max. admissible vessel pressure, but **not below 2 bar** [^scheme]
  [OCR].
- The safety guideline [confirmed] adds: safety-valve settings must never be
  changed, and pressure vessels must be installed, operated and monitored per
  the official regulations [^safety].

## 7. Electrical installation context

From the UXLA00379 cover sheet [^uxla] [OCR] — the same identity the electrical
record and the safety record carry:

| Item | Value |
| --- | --- |
| Supply voltage / frequency | 400 V / 50 Hz |
| Feed line | 95 mm² + PE + GND |
| Control voltage | 220 V AC / 24 V DC |
| Current main isolator | 250 A |
| Controller | DYNET |

The drawing index lists electrical-installation-related sheets — "Feed Lines",
"Connect Cabinet", "Main Cabinet Power Unit / Emergency-off", "Installation
Denomination", and terminal/naming sheets — which are the reference for wiring
according to the drawing set [^uxla] [OCR]. The main control cabinet sits below
the blower [^then] [confirmed], and the emergency-stop positions (operator panel
and control cabinet) and the main switch are the machine's shut-off points
[^safety] [confirmed].

> [!WARNING]
> This machine is connected at 400 V / 50 Hz with a 250 A main isolator [^uxla]
> and carries hazardous electrical energy. This record is NOT the electrical
> record [^uxla] and contains no instructions for working on or near energized
> equipment — use the electrical record for signals and the safety record for
> hazards, and apply the site-approved isolation / lockout procedure before any
> physical intervention.

## 8. Valves, fittings, and connected equipment

- The dedicated valves-and-fittings installation sheet (IB29530D) exists in the
  set [^fittings]; in this review its drawing content could not be read from the
  scan (only the ISO 16016 copyright block was legible), so the detailed
  valves-and-fittings arrangement is **Not documented** here and must be read
  from the original sheet.
- The schematic sheet (IB29530B) prints valve tags on the utility lines against
  the machine's components — heat exchanger, blower, main pump, booster, dye
  autoclave (DA), service/addition tank (AT), filter, pneumatic module [^schematic]
  [OCR]. Tags read by OCR include **V147, V51, V131, V124, V20, V125, V163,
  V175, V142, V137, V132, V136, V138, V301, V30, V356, V359, V321, V311, V113,
  V105, V120, V112, V101, V360, V102, V351, V109, V174**; a few further tags
  (rendered by OCR only as "VSO"/"V50", "vss"/"V85", and a "V21"-like mark in
  the filter area) were ambiguous and are NOT transcribed here. The reading is
  incomplete and every tag must be confirmed on the sheet before it is used to
  identify a valve.
- A few of these tag families also appear in the manual's operating text
  [^then] [confirmed] (e.g. the VD salt valve as V300 and the VX front flap as
  V121, plus VV/V351) — [interpretation] the schematic's V356/V301 tags sit in
  the same main-pump / free-outlet region and V121 ↔ VX, V351 ↔ VV; the drawing
  does not print those cross-links, so this mapping is not asserted.
- Component notes on the schematic: "DA = DYE AUTOCLAVE, AT = SERVICE TANK"
  [OCR]; a "taking-out of dye bath / free outlet" arrangement at the main pump;
  a condensation / cooling-water network; and a ventilation line [^schematic]
  [OCR].

## 9. Installation-related safety boundaries

The safety guideline's installation-site chapter places these obligations on
the owner [^safety] [confirmed]:

- Install the machine according to the installation drawings; the floor loading
  must meet the machine's requirement.
- Chemical-resistant, slip-resistant flooring in the working area; marked and
  signposted work places.
- Rooms suitable for operation and maintenance, emergency-exit marking,
  fire-fighting equipment.
- Wastewater piping adequately sized with suitable non-return valves; drains
  must not be able to block.
- All inlet and drain pipes must have the appropriate back-up or non-return
  valves installed upstream of each machine, per the connection/installation
  drawings.
- Chemical pipes protected from damage; hot pipes insulated; exhaust/ventilation
  piping installed; leak-collection measures so spilled chemicals are channeled
  safely.
- Safe access around the machine (platform/ladder for maintenance); entry into
  the vessel is governed by the guideline's container rules [^safety] and is
  NOT described here.

Prohibitions relevant at installation time [^safety] [confirmed]: other
installations must not weaken or disable the machine's safety devices; the
emergency stops must stay reachable at all times; the programmable control
software must not be altered; safety-valve settings must never be changed. Work
on the machine's electrical systems is reserved for appropriately qualified
personnel.

## 10. Maintenance / diagnostic relevance

What an engineer diagnosing the unit can take from the installation context:

- **Supply pressure checks**: steam, water and air pressures are defined at the
  connection boundary (§5, §6). A supply above or below those figures is a
  first-line diagnostic lead — the pressure-interlock and sensor behaviour in
  the safety record [^safety] and the pressure signals in the electrical record
  [^uxla] assume this installed environment.
- **Safety-valve identity** for servicing: DN50 steam 1695 kg/h and G ½" steam
  370 kg/h relieving capacities, printed set pressures 3 / 8 bar (§6) [^schematic]
  [OCR] — confirm each on the sheet; the safety guideline fixes that the
  settings are not to be changed [^safety].
- **Foundation / anchoring** figures (§4) are the reference for level, re-tighten
  and relocation checks; the kier and pump must be fixed professionally at the
  site [^foundation] [OCR].
- **Delivery boundaries**: the machine's own delivery ends at its connection
  points — broken supply lines, parts of plant and the fibre retainer are not
  part of the delivery [^scheme] [OCR].
- **Condensate and drain upkeep**: condensate lines must be drained and not
  blocked (the scheme prints a pump drain over the roof) [^scheme] [OCR][^safety].
- **Electrical shutdown points** for safe intervention: main switch, control
  cabinet and operator-panel emergency stops [^safety] [confirmed], and the
  electrical record for the signals around them [^uxla].

## 11. Not documented / requires drawing verification

The following are explicit gaps or OCR caveats:

- **IB29530D (valves & fittings installation)** — drawing content not legible in
  this review; read from the original sheet (§8).
- **Exact anchor-bolt/dowel pattern and positions, and the overall dimension
  set** — [OCR], verify every figure on IB29530 / IB29530A (§3, §4).
- **Steam minimum**: OCR read both "6 bar" and "7 bar"; confirm the printed
  minimum on IB29530C (§5).
- **Set pressures 3 bar / 8 bar** — printed, but their assignment to specific
  valves is [interpretation]; verify (§6).
- **"Pipes … made of stainless steel"** — OCR fragment of the scheme's note;
  wording to be confirmed (§5).
- **Terminal numbers, wire numbers, and any electrical connection details** —
  not read from UXLA00379 in this record; the drawing set's installation
  denomination / feed-line sheets hold them (§7, §11).
- **Foundation bolt grades and any torque / grouting / levelling procedure** —
  not printed in the sheets reviewed.
- **Site-provided work access** (scaffold, platforms beyond the 20000 N working
  platform) and official pressure-vessel inspection requirements — referenced
  only in general terms by the safety guideline; detail is the site's [^safety].

## Sources

[^layout]: `sources/textile-machinery/IB29530 .pdf` — General layout plan "GENERAL LAYOUT PLAN FOR SYN1200 G2/37029530-31", sheet A3, NTS — FONG'S EUROPE GMBH. No text layer; OCR-read.

[^foundation]: `sources/textile-machinery/IB29530A .pdf` — Foundation layout plan "FOUNDATION LAYOUT PLAN FOR SYN1200 G2" — FONG'S EUROPE GMBH. No text layer; OCR-read.

[^schematic]: `sources/textile-machinery/IB29530B .pdf` — Schematic plan "SCHEMATIC PLAN FOR SYN1200 G2/37029530-31" (installation and utilities) — FONG'S EUROPE GMBH. No text layer; OCR-read.

[^scheme]: `sources/textile-machinery/IB29530C .pdf` — Installation scheme "INSTALLATION SCHEME FOR SYN1200 G2/37029530-31" (utility specifications) — FONG'S EUROPE GMBH. No text layer; OCR-read.

[^fittings]: `sources/textile-machinery/IB29530D .pdf` — Valves and fittings installation scheme, SYN1200 G2, order 37029530-31 — FONG'S EUROPE GMBH. No text layer; drawing content not readable in this review.

[^then]: `sources/textile-machinery/THEN高温气流染色机SYN G2.pdf` — THEN-Airflow SYN G2 使用说明书 (operator manual), v2.0; THEN Machinery. Text layer; contents [confirmed].

[^safety]: `sources/textile-machinery/特恩高溫氣流染色機SYN G2安全指引.pdf` — THEN-AIRFLOW SYN G2 安全指引 (safety guideline), v1.0; 特恩机械有限公司 (THEN Machinery (HK) Ltd.). Text layer; contents [confirmed].

[^uxla]: `sources/textile-machinery/37029530~531  UXLA00379.pdf` — UXLA00379 electrical drawing set, SYN1200 G2, order 37029530-31; FONG'S EUROPE GMBH; cover sheet dated 05-06-2012, drawing index dated 05-06-2012. Scanned sheets; OCR-read.