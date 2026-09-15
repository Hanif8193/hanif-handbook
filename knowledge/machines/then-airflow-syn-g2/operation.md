---
type: Document
title: THEN-Airflow SYN G2 / SYN1200 G2 — operating context
description: Manufacturer/source-documented operating context for the THEN-Airflow SYN G2 / SYN1200 G2 dyeing machine — machine states, operating conditions and setpoints, normal/abnormal indications and documented fault-to-operating-condition relationships useful for diagnosing electrical and mechanical faults — read from the THEN operator manual and safety guideline and the UXLA00379, IB29530/B/C and IBAK159 drawing sheets.
status: stable
order: 5
generated: { by: "human:hanif", at: 2026-09-15T09:58:19Z }
sources:
  - id: then
    resource: sources/textile-machinery/THEN高温气流染色机SYN G2.pdf
    title: THEN-Airflow SYN G2 使用说明书 (Operator Manual), v2.0 - THEN Machinery
  - id: safety
    resource: sources/textile-machinery/特恩高溫氣流染色機SYN G2安全指引.pdf
    title: THEN-AIRFLOW SYN G2 安全指引 (Safety Guideline), v1.0 - 特恩机械有限公司 (THEN Machinery (HK) Ltd.)
  - id: uxla
    resource: sources/textile-machinery/37029530~531  UXLA00379.pdf
    title: UXLA00379 electrical drawing set, SYN1200 G2, order 37029530-31 - FONG'S EUROPE GMBH, 2012
  - id: layout
    resource: sources/textile-machinery/IB29530 .pdf
    title: General layout plan, SYN1200 G2, order 37029530-31 - FONG'S EUROPE GMBH
  - id: schematic
    resource: sources/textile-machinery/IB29530B .pdf
    title: Schematic plan (installation and utilities), SYN1200 G2, order 37029530-31 - FONG'S EUROPE GMBH
  - id: scheme
    resource: sources/textile-machinery/IB29530C .pdf
    title: Installation scheme — utility specifications, SYN1200 G2, order 37029530-31 - FONG'S EUROPE GMBH
  - id: bak
    resource: sources/textile-machinery/IBAK159.pdf
    title: IBAK159 pneumatic-valve sheet, SYN family - FONG'S EUROPE GMBH
ksor:
  audience: [public]
  approval: { by: "human:hanif", at: 2026-09-15T09:58:19Z }
  owner: "human:hanif"
---

This record documents the operating context of ONE machine — the THEN-Airflow
SYN G2 / SYN1200 G2 high-temperature air-flow dyeing machine, order 37029530-31,
controller DYNET [^then][^uxla] — as the manufacturer printed it: the machine's
operating states, the documented operating conditions (temperature, pressure,
level, flow, circulation, injection, unloading), the normal/abnormal
indications a diagnostician can read, and the fault symptoms the sources tie to
specific operating conditions. It exists to put fault diagnosis into its
operating context; nothing in it is a work instruction for installation,
operation, commissioning or maintenance. It is a draft record and has not been
approved.

## Confidence labels

- **[confirmed]** — printed precisely in the source and read clearly from its text layer.
- **[OCR]** — printed in the source but read through OCR of a scanned or vector-only drawing; wording, numerals or values may differ slightly from the sheet and MUST be verified against the original before use.
- **[interpretation]** — my reading of context, not a printed statement.
- **Not documented** — important information the sources do not provide.

> [!NOTE]
> The THEN operator manual and the THEN safety guideline have text layers, so
> their contents are **[confirmed]** from that text [^then][^safety]. The
> UXLA00379 electrical drawing set, the IB29530/B/C installation sheets and the
> IBAK159 sheet are image-only (no text layer); EVERY value or label taken from
> them is **[OCR]** and must be read off the original sheet before it is used.
> The electrical record [^uxla] owns the fine-grained fault-signal list and the
> safety record [^safety] owns the hazards and interlocks; this record carries
> the operating context around them and neither repeats nor overrides them.

## 1. Scope

What this record covers:

- The operating states the DYNET control shows (program, loading, sampling,
  unloading, manual, alarm) and how they relate [^then].
- The documented operating conditions: temperature and pressure thresholds the
  process runs to, water-level figures, air/steam/water flows and the
  circulation and injection functions [^then][^safety][^uxla][^schematic].
- The documented normal/abnormal indications: operator-panel indicators, screen
  state symbols, analog operating signals and the fault/trouble signals in the
  drawing set [^then][^uxla].
- Manufacturer-documented fault symptoms and their relationship to operating
  conditions (boiler/fill/level/salt/blower cases) [^then][^safety].
- Operating observations a maintenance person or agent may use to distinguish
  faults [interpretation] connections between the manual's sequences and the
  drawing-set signals where the sources do not print the link.
- The IBAK159 pneumatic-valve sheet as far as it could be read [^bak].
- What the sources do NOT document, kept as explicit gaps.

This is deliberately NOT a general operator manual: the full loading/unloading
and sampling procedures are only summarized where they are diagnostic-relevant.

## 2. Operating sub-systems the process uses

The machine's construction chapter names the parts the operating process uses —
vessel, circulation system, circulation pump (hidden behind), heat exchanger,
liquor filter, air filter (within the vessel), addition (dosing) tank, working
platform, blower, take-off roller, winch (fabric-transport) drive, nozzle, DYNET
control, operator panel and main control cabinet (below the blower) [^then]
[confirmed]. The installation record carries the same vocabulary from the
installation sheets [^layout][^schematic][^scheme]. For diagnosis, the
operating-relevant drives named in the sources are: the **blower** (air-flow
circulation), the **winches** per storage store (fabric transport), the
**plaiter**, the **main pump**, the **booster**, the **injection pump**, the
**addition pump**, the **DA mixing pump**, the **rinsing motor** and the
**take-off roller / X-Y plaiting drives** (frequency-converter driven per the
unloading chapter) [^then][^uxla].

## 3. Documented operating states — [confirmed][^then]

The DYNET screen symbols and status operators printed in the manual's chapter 3:

- **Status/state display symbols (3.3)**: program end; program stop; auto
  program; manual operation; status unknown or no connection; loading;
  unloading; cleaning the filter; sampling; check pH value; check salt content;
  cancel; dissolve salt; alarm.
- **Menu symbols (3.2)**: nominal/runtime picture screens (4 freely configured);
  graphical batch report and batch curve; indication of the applied dye program
  and of a jump during the program; alarm list; dye-program list; re-dye program
  list; dye-program macro editor; manual program; reference (nominal value)
  change; next/previous level; quit program; password entry; service tools
  (time setting, EEPROM setting, GUI configuration).
- **Screen buttons (3.4)**: program list / program selection; load dye program;
  load re-dye program; program start; program stop; end program; switch to
  manual; close manual function / re-open the machine in stop state; start
  re-dye program after manual operation; end program, close manual operation.

These are the labels a machine shows. [interpretation] The "alarm" operator and
the "alarm list" menu entry are the machine's alarm indication; the drawing
set's alarm/trouble signals are listed in the electrical record [^uxla].

## 4. Documented operating-state relationships — [confirmed][^then]

Sequence relationships the manual prints, each useful to check the machine's
behavior against:

- **Program start** (ch. 5): the controller must be in the "program end" state
  (3.3-1); select the program (selected program appears with blue background);
  press "load dye program" (3.4-2); confirm the displayed program; the program
  name then shows in the machine-status window and the status changes to
  "program stop" (3.3-2); press "program start" (3.4-4). From then on the
  manual states the status "can switch fully automatically according to the set
  program".
- **Loading confirmation** (ch. 6/7): when the flash-pulse device blinks and
  the screen shows "loading", pressing "immediately" confirms and "next" closes
  the dialog; the animated operator "load" (3.3-6) also enters the confirmation
  screen; if no confirmation screen appears, selecting that animated operator
  brings it up. After confirming, the program continues.
- **Salt addition** (ch. 8): during the "add salt" function, liquor flows
  continuously from the circulation line above the VD valve (V300) into the
  addition tank, while suction at the addition tank and at VV (V351) draws it
  back into the circulation line; both valves are timed to keep the program
  level; adding salt with the VD valve (V300) fully open is recommended by the
  manual; after adding and confirming, the remaining liquor is drawn back from
  the tank into the circulation system.
- **Sampling and seam handling** (ch. 9): the flash-pulse device blinks and the
  screen shows "sampling"; pressing the "half-manual" sync indicator (2.8), the
  operator waits until the red "fabric running" lamp flashes, meaning the
  machine has stopped because a fabric seam (布缝) has passed — the seam
  detection stops the fabric run. Confirming then lets the program continue
  ("sample OK") or select a re-dye program.
- **Unloading and seam detection** (ch. 10): the flash-pulse device blinks and
  the screen shows "unloading"; once a seam is detected the "half-manual" sync
  indicator flashes; pressing the half-manual indicator of a storage store
  searches for further seams. Store 1 unloads via the take-off roller with or
  without the X-Y plaiting device; the X-Y plaiting controls are X (straight
  plaiting only), X+Y (both), Roller (take-off drum speed, with frequency
  converter), X-speed and Y-speed, manually adjustable during take-off.
- **Program browse / jump** (ch. 11): while a program runs, the current macro
  instruction is shown (yellow); marking a new macro (blue background) and
  pressing "jump to new macro" performs a program skip.
  [interpretation] Because a skip changes the running state, it can look like a
  fault when it happens unexpectedly.

## 5. Documented operating conditions and setpoints

### 5.1 Temperature conditions — [confirmed][^then][^safety]

- **Door-opening / sampling / unloading / liquor-drawing threshold: below
  80 °C (176 °F)** and the vessel **depressurized (pressure gauge at 0 bar)**.
  Repeated in the manual (sampling §9.2, unloading §10.2) and the safety
  guideline (filter/manhole doors, liquor drain).
- **Salt addition limit: below 80 °C (176 °F).** The VD valve (V300) has a
  temperature protection; salt addition only takes effect below 80 °C.
- **Temperature-interlock check point ~90 °C (194 °F)** — the safety
  guideline's own safety-circuit check heats the vessel to about 90 °C to test
  the temperature interlock (components N1102, B1100, Y176); see the safety
  record. Not an operating setpoint.
- Steam supply 6–8 bar and heat-exchange duty are the installed boundary
  ([OCR] — read from the installation sheets, see §5.3); the vessel's own
  maximum dyeing temperature is **Not documented** in the sources.

### 5.2 Level and pressure operating conditions — [confirmed][^safety]

- **Blower (air circulation) start conditions**: no dye liquor in the blower —
  the controller water-level indication must read below ~95 % and a visual
  check of the kier level confirms it; **static pressure below 1 bar (gauge)**;
  the **VX flap closed**.
- **Kier water level "Nda" reads at a maximum of ~95 %.** Above that, water or
  dye liquor can be drawn into the blower.
- The guideline also prints two level reference figures "water level ≈ 95 %"
  and "water level ≈ 42 %" beside a caption naming pressure vessels and open
  vessels; [interpretation] the 95 % figure is the pressure-vessel (kier) figure
  that the air-circulation chapter repeats, and the 42 % figure concerns the
  open (atmospheric) vessel side — the mapping is not printed and must be
  confirmed.
- **Blower running constraint**: the blower must not be set to zero (VX flap
  set to closed) for more than **five minutes**; the blower motor's rated
  output and the VX-flap / static-pressure set values must stay within their
  permitted ranges.
- **Salt solubility operating boundary** — manual [^then]: base additions on the
  solubility at 20 °C (68 °F), stay **at least 50–100 g/l below saturation**,
  else re-crystallization on cooling can destroy the metering pump and stirrer
  mechanical seals. Recommended reference values printed: refined salt (sodium
  chloride) ~ **250 g/l**; sodium sulphate per the printed temperature table
  (≈ 161 g/l at 20 °C, rising to ≈ 332 g/l at 32.4 °C, falling again toward
  100 °C — [confirmed] figures from the manual's table).

### 5.3 Utility / flow operating context — [OCR]

Printed on the IB29530/B/C installation sheets (vector/scanned, verify on the
sheet), carried here for context because they bound what the machine can do:

| Condition | Value printed | Source sheet |
| --- | --- | --- |
| Steam supply, heat exchanger | 6–8 bar (scheme: min 6 / max 8 bar; layout and schematic: 6–8 bar) | [^scheme][^schematic][^layout] |
| Steam, booster | 3 bar | [^layout] |
| Soft water supply | max. 3 bar (scheme: 2–3 bar) | [^layout][^scheme] |
| Water supply | 2–3 bar | [^scheme] |
| Compressed air supply | 8 bar (layout); 8–10 bar (schematic), inlet DN40 | [^layout][^schematic] |
| Air requirement | max. 7 Nm³/h total; 5 Nm³/h on the pneumatic-module / instruments side | [^schematic] |
| Steam consumption | heat exchanger max. 3180 kg/h; addition tank max. 175 kg/h | [^schematic] |
| Cooling-water flow | 7690 kg/h (printed at the cooling-water return pipeline) | [^schematic] |
| Free outlet at the main pump | ~2–3 L/min (printed "free outlet 2-3L/min", tag V100 area) | [^schematic] |
| Transmitter-line rinsing water | not above the admissible vessel pressure, and not below 2 bar | [^scheme] |

These are connection/supply figures (the installation record's territory) and
are repeated here only because a diagnostician reads supply faults against them
[^layout][^schematic][^scheme].

### 5.4 Circulation / injection functions — [confirmed][^then][^uxla]

- **Injection system**: the drawing set's Analog sheet routes a "nominal value
  injection pump" output (U101) and reports "injection pump trouble",
  "feed-back injection pump" and a per-store "injection interlock" alarm —
  all [OCR]; the injection pump's own drive/parameter documentation belongs to
  the separate injection-source pump record, not this one [^uxla].
- **Addition (AT) and dye autoclave (DA)**: the drawing set reads "level AT"
  and "level d.a.", "temperature additive tank AT1" and "AT fill level/drain"
  as analog/control signals [^uxla], consistent with the manual's addition-tank
  checks before loading (tank filled with suitable water, or empty and clean)
  [^then].
- **Heat exchange / temperature control**: "control valve VHK" (B136), "control
  valve VDJ" (B109), "temperature Tda" (B1100), "temperature injection"
  (P100/B1105), "temperature warm water" (B1107/1231) and temperature-of-cabinet
  signals appear as analog inputs in the drawing set [^uxla] [OCR].
- **Rinsing**: "rinsing valve filter" (Y105), "rinsing valve VSP3" (Y108),
  "rinsing valve transducers" (Y174/Y175), "rinsing valve VPR" (B163),
  "rinsing valve light barrier" (Y050) and a "rinsing motor ON" output are
  printed in the set [^uxla] [OCR]; the manual's "cleaning the filter" state
  (3.3-8) is the operator-facing counterpart [^then].

## 6. Normal / abnormal indications

### 6.1 Operator panel — [confirmed][^then]

The manual's operator-panel (§2.1) lists: touch screen; a **temperature-lock
signal lamp**; **sync indicators** for guide-roller (winch) fault, motor fault
and inhibit signal; an "unlock" control; an **emergency stop** (the manual
points to chapter 10 for its use); the **flash-pulse device** (blinks to prompt
loading/sampling/unloading confirmations); a **red "fabric running" lamp**;
**winch speed potentiometer**; **winch direction switch (forward/backward)**;
an **illumination key**; a **half-manual sync indicator**; and a **nozzle-lock
sync indicator**. (The item numbers printed in the manual are inconsistent
between the panel figure and the chapters' cross-references — [interpretation]
they are the manual's own loose numbering; the labels themselves are confirmed.
The electrical record links these panel lamps to drawing-set signals only where
the sources do; see its [interpretation] notes.)

### 6.2 Screen states — [confirmed][^then]

See §3. A diagnostician reads: "status unknown or no connection" as a control
connection problem [interpretation], "alarm" as the machine's alarm state, and
the "program end / stop / auto / manual" states as the current operating mode.

### 6.3 Analog operating signals — [OCR][^uxla]

The Analog In/Output Overview sheet names 4–20 mA channels that show the
machine's operating quantities (verification against the sheet required):

- Blower revolution (U102) and blower current (U102).
- Winch revolution per store (U131–U134) and plaiter revolution (U105).
- Nominal value injection pump (U101).
- Temperatures: Tda (B1100), injection (P100/B1105), additive tank AT1,
  warm water (B1107/1231), main current cabinet (B0000), operator module.
- Static pressure FK, level d.a. (kier), level AT (addition tank).
- Flow meter, flow injection, water counter, and control-valve feedbacks
  (VHK B136, VDJ B109, metering valve VVD B356, rinsing valve VPR B163).

**No normal values, setpoints or alarm thresholds for these channels are
documented in the sources** — see §8.

### 6.4 Trouble signals — [OCR][^uxla]

The PLC Overview sheets print the trouble/status inputs this machine family
uses: blower trouble/reset/on and feed-back; winch 1–4 trouble and forward/
backward; plaiter trouble; injection-pump trouble and feed-back; addition-pump
trouble; DA mixing pump ON; rinsing motor ON; EMERG.-OFF input; press.
interlock; temperature interlock; per-store run-of-fabric trouble, light
barrier and seam-detect signals. The full list is the electrical record's
table; it is referenced, not repeated, here.

## 7. Documented fault symptoms and their operating conditions

The following relationships ARE documented; the emergency RESPONSES to several
of them are in the safety record and are only pointed at here [^then][^safety]:

- **Salt crystallisation destroys the metering pump / stirrer mechanical
  seals** — symptom of adding refined salt or Glauber's salt near or above its
  solubility limit; the manual's rule is to stay at least 50–100 g/l below
  saturation at 20 °C. Salt addition is also temperature-guarded on VD (V300)
  below 80 °C (see §5.1) [^then].
- **Water or dye liquor drawn into the blower** — symptom of kier water level
  "Nda" above ~95 % (the max. the guideline allows before carry-over); the
  blower start checks (level < ~95 %, static pressure < 1 bar, VX flap closed)
  are the conditions that prevent it [^safety].
- **Blower kept at zero (VX flap closed) more than five minutes** — a running
  condition the guideline forbids; if it occurs, the machine is being operated
  contrary to the guideline [^safety].
- **Sudden balance error** — the guideline instructs to close the main switch
  or press the red emergency-stop, then find and eliminate the cause [^safety].
- **Steam supply valve VLZ stuck open** — a documented fault; the guideline's
  response is to close the main steam valve manually at a distance from the
  kier [^safety].
- **Fill-water valve VCZ not closing / water overflowing** and **level-sensor
  failure with overflow** — fill-control failures; responses per the guideline
  are to close the control valve by hand / press emergency / cut main power
  [^safety].
- **Reflux valve VD stuck open or opening unexpectedly** (the same VD / V300 of
  the salt function) — a circulation interrupt; response per the guideline is
  emergency-stop / cut main power [^safety].
- **Any danger during unloading** — emergency stop / cut main power [^safety].

None of these is a repair procedure; the machine's service documentation must
carry the actual repair steps.

## 8. Operating observations that help distinguish faults

- **Seam stop vs. winch fault.** A fabric seam passing light-barrier
  detection stops the fabric run and makes the red "fabric running" lamp flash
  (sampling, §9.1) and the "half-manual" sync indicator flash (unloading,
  §10.1); per-store "run of fab. trouble", "light barrier" and "seam detect."
  signals exist in the drawing set [^uxla]. [interpretation] If the machine
  stops but no seam lamp/signal behaviour appears, the seam-detection / light
  barrier path is suspect before the winch drive — the sources do not print
  this diagnostic order.
- **Level readings.** The controller shows the kier level (level d.a.) and the
  addition-tank level (level AT); the blower-start rule reads the kier level
  below ~95 % [^uxla][^safety]. Comparing these displayed levels to the
  guideline's ~95 % / ~42 % figures and to the physical vessel is a first check
  for fill and carry-over faults.
- **Blower condition via analog channels.** Blower revolution and blower
  current (both U102) and the static-pressure FK input let an operator compare
  running blower behaviour against the guideline's < 1 bar static-pressure rule
  — [interpretation] a current that reads while revolution is lost points at a
  mechanical/jamming fault rather than an electrical one; the values themselves
  are not documented.
- **Salt function behavior.** During "add salt", liquor flows from the
  circulation line above VD (V300) into the addition tank and is drawn back at
  the tank / VV (V351); both valves are timed. [interpretation] A batch that
  loses level or fails to dissolve salt during this step points at VD (V300)
  and VV (V351) — the same valve (VD/V300) the guideline's stuck-open fault
  names.
- **Heat control via the control-valve feedbacks.** The drawing set reads
  control valve VHK (B136) and VDJ (B109) plus several temperature channels §6.3
  [OCR]; the manual's temperature-lock lamp and the guideline's 80 °C / 90 °C
  thresholds bound the expected temperatures. No setpoints are documented.
- **Unloading drive behavior.** X / X+Y / Roller / X-speed / Y-speed plaiting
  controls are frequency-converter driven with manual adjustment during
  take-off [^then]; [interpretation] a take-off fault that follows a
  non-responsive plaiting control points at the drive/frequency-converter path
  the X-Y device uses.
- **Pneumatic-module behavior.** The drawing set's Pneumatic-Module Mounting
  Plate sheets (PM1 / PM2) print the pneumatic valves the machine drives (air
  feed ~6 bar on PM1, 3–6 bar on PM2) — aeration, flaps (VX flap 1–4), drain
  valves, filter drain, pressure/temperature interlocks, heating/cooling
  valves, water feeds, cut-off/by-pass/connection/mix valves and the
  E/P transducers B356, B136, B163, B109 [^uxla] [OCR]. The plate sheets are
  the place to identify a pneumatic valve an air fault implicates; tag-to-label
  pairing must be read from the sheets.

## 9. IBAK159 — pneumatic-valve sheet — [OCR][^bak]

IBAK159 is a single-page, image-only sheet (no text layer) titled by its title
block as a FONG'S EUROPE drawing (the title block itself did not OCR legibly).
Its content as read by OCR is a valve/tag list for the SYN machine family:

- Valve tags read by OCR (verify each on the sheet): V811, V856, V821, V900,
  V117, VAI, VA2, V113, V105, V101, V102, VS, V854, V808, V311, VBZ, V356,
  B1380, V355, VV3, V411, VBD, V359, V051, V147, VEL, V142, VE2, V300, VDZ,
  V400, VDD, V108, VSP3.
- Machine-type column entries read as: values on AFE50/SYN50/SYN60G,
  FE25/0/0G/3, AFE675/SYN750/SYN900G and AFE450/SYN500/SYN600 rows, with a
  "TYPE" header and a "*)OPTION" marker [OCR].
- [interpretation] The tag families overlap the machine's pneumatic system named
  elsewhere — VEL (air-feed valve), VE2 (aeration valve), V300 (= VD, the salt /
  reflux valve), VBZ (drain), VSP3 (rinsing valve), V142/V147/V174/V175 — so
  this sheet is likely the pneumatic module's valve listing; the mapping must be
  read from the sheet itself. Its value here is identification of pneumatic
  valves during a fault, not operating setpoints.

## 10. Not documented

- **PLC logic, timings, program steps, alarm codes and their meanings**: none of
  the sources documents the DYNET program internals or any alarm-code table.
- **Any "normal" numeric value for the analog channels** (blower current,
  revolution, temperatures, static pressure, levels, flows): the drawing set
  names the channels but prints no limits.
- **Maximum dyeing temperature and maximum working pressure of the vessel**:
  not printed in the text sources; safety-valve setting figures are [OCR] on
  IB29530B and unverified (see safety and installation records).
- **The IBAK159 sheet's own title, structure and full valve list**: OCR only
  partially legible; verify on the sheet.
- **The exact correspondence of manual panel item numbers to the drawing-set
  signals**: the sources print both but do not link them ([interpretation]
  boundaries noted in §6.1 and the electrical record).
- **Repair, adjustment or commissioning procedures** for any component or
  function above.
- **The permitted ranges for the VX-flap and static-pressure set values** beyond
  the guideline's words "within the permitted ranges" [^safety]: not printed.

## Sources

[^then]: `sources/textile-machinery/THEN高温气流染色机SYN G2.pdf` — THEN-Airflow SYN G2 使用说明书 (operator manual), v2.0; THEN Machinery. Text layer readable; contents [confirmed]: construction (ch. 2), operator-panel items (§2.1), DYNET display symbols (§3.2–3.4), program starting (ch. 5), loading confirmation (ch. 6–7), salt addition and VD/V300 temperature guard (ch. 8), sampling and seam detection (§9.1–9.5), unloading and seam detection (ch. 10), X-Y plaiting device (§10.6), program browse/jump and nominal-value change (ch. 11).

[^safety]: `sources/textile-machinery/特恩高溫氣流染色機SYN G2安全指引.pdf` — THEN-AIRFLOW SYN G2 安全指引 (safety guideline), v1.0; 特恩机械有限公司 (THEN Machinery (HK) Ltd.). Text layer readable; contents [confirmed]: air-circulation start and monitoring (p. 20–21), kier water level Nda ~95 %, blower zero-time ≤ 5 min, sudden-balance fault, door / filter / manhole opening conditions, liquor drain < 80 °C, safety-valve handling, emergency fault responses (VLZ, VCZ, level sensor, VD, unloading) (p. 18, 21–24).

[^uxla]: `sources/textile-machinery/37029530~531  UXLA00379.pdf` — UXLA00379 electrical drawing set, SYN1200 G2, order 37029530-31; FONG'S EUROPE GMBH; covers dated 05-06-2012 and 10-07-2012. Image-only scan; contents [OCR]: drawing index, PLC Overview sheets (trouble/interlock signals), Analog In/Output Overview (4–20 mA channels), Pneumatic-Module Mounting Plate 1/2, flutter and take-off sheets, X-Y plaiting control, flow/level/temperature signals.

[^layout]: `sources/textile-machinery/IB29530 .pdf` — General layout plan "GENERAL LAYOUT PLAN FOR SYN1200 G2/37029530-31", sheet A3, NTS — FONG'S EUROPE GMBH. No text layer; OCR-read: steam 6–8 bar (heat exchanger) and 3 bar (booster), soft water max 3 bar, compressed air 8 bar, cooling-water/condensate/drain connections.

[^schematic]: `sources/textile-machinery/IB29530B .pdf` — Schematic plan "SCHEMATIC PLAN FOR SYN1200 G2/37029530-31" (installation and utilities) — FONG'S EUROPE GMBH. No text layer; OCR-read: steam 6–8 bar, compressed air 8–10 bar with max 7 Nm³/h / 5 Nm³/h requirements, 6–8 bar and 8 bar pressure labels, steam consumption 3180/175 kg/h, cooling water 7690 kg/h, free outlet 2–3 L/min, valve tags.

[^scheme]: `sources/textile-machinery/IB29530C .pdf` — Installation scheme "INSTALLATION SCHEME FOR SYN1200 G2/37029530-31" (utility specifications) — FONG'S EUROPE GMBH. No text layer; OCR-read: saturated steam min 6/max 8 bar, soft water and water 2–3 bar, transmitter-line rinsing pressure (≥ 2 bar and not above admissible vessel pressure).

[^bak]: `sources/textile-machinery/IBAK159.pdf` — IBAK159 valve/pneumatic sheet, SYN machine family — FONG'S EUROPE GMBH. Single-page image-only scan; title block and content only partially OCR-readable ([OCR]); verify every tag on the sheet.