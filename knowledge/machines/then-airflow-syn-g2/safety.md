---
type: Document
title: THEN-Airflow SYN G2 / SYN1200 G2 — safety and diagnostic hazards
description: Manufacturer-documented electrical, pressure, temperature, mechanical, chemical and emergency-stop hazards of the THEN-Airflow SYN G2 / SYN1200 G2 dyeing machine, as context for diagnosing electrical and mechanical faults in the unit.
status: stable
order: 3
generated: { by: "human:hanif", at: 2026-09-15T14:28:07Z }
sources:
  - id: safety
    resource: sources/textile-machinery/特恩高溫氣流染色機SYN G2安全指引.pdf
    title: THEN-AIRFLOW SYN G2 安全指引 (Safety Guideline), v1.0 - 特恩机械有限公司 (THEN Machinery (HK) Ltd.)
  - id: then
    resource: sources/textile-machinery/THEN高温气流染色机SYN G2.pdf
    title: THEN-Airflow SYN G2 使用说明书 (Operating Manual), v2.0 - THEN Machinery
  - id: uxla
    resource: sources/textile-machinery/37029530~531  UXLA00379.pdf
    title: UXLA00379 electrical drawing set, SYN1200 G2, order 37029530-31 - FONG'S EUROPE GMBH, 2012
  - id: instb
    resource: sources/textile-machinery/IB29530B .pdf
    title: Installation schematic plan, SYN1200 G2, order 37029530-31 - FONG'S EUROPE GMBH
  - id: instc
    resource: sources/textile-machinery/IB29530C .pdf
    title: Installation scheme - utility specifications, SYN1200 G2, order 37029530-31 - FONG'S EUROPE GMBH
ksor:
  audience: [public]
  approval: { by: "human:hanif", at: 2026-09-15T14:28:07Z }
  owner: "human:hanif"
---

This record is the safety and diagnostic-hazard reference for ONE machine: the
THEN-Airflow SYN G2 / SYN1200 G2 high-temperature air-flow dyeing machine,
order 37029530-31, controller DYNET [^uxla][^then][^safety]. It exists to put
fault diagnosis into its safety context: the hazards the operator and the
diagnostician face when this machine is hot, pressurised, energized or loaded
with chemicals. Nothing in this record is a work instruction for installation,
operation, maintenance or repair, and it does not describe safe isolation.

## Confidence labels

- **[confirmed]** — printed precisely in the source and read clearly from its text layer.
- **[OCR]** — printed in the source but read through OCR (image-only or garbled scans); the wording or value may differ slightly from the sheet and must be verified against it before use.
- **[interpretation]** — my reading of context, not a printed statement.
- **Not documented** — important information the sources do not provide.

## Machine safety context

The SYN G2 is a high-temperature air-flow dyeing machine: a hot, pressurised
pressure vessel with a blower air-circulation system, rotating winches
(fabric-transport rollers), dye-liquor circulation pumps, a heat exchanger and
chemical dosing [^then][^safety].

The manufacturer's safety equipment, named in the safety guideline, is: the
safety valve, the working-door flange ring (which prevents steam escaping), the
blower guard, the lifting-motor guard, the emergency-stop buttons (operator
panel and control cabinet) and warning plates — including "do not touch moving
fabric" and "do not open while pressurised or above 80 °C" [^safety]. The
guideline states these safety devices exist for the operator's safety and must
not be modified, removed or rendered ineffective [^safety].

Requirements the manufacturer places on the operating company [^safety]:

- All persons installing, commissioning, operating, maintaining and repairing
  the machine must be appropriately qualified and fully compliant with the
  guideline.
- Before the machine is started, all safety equipment must be in place and
  functioning; safety rules must be posted visibly near the machine.
- The machine is intended ONLY for wet rope-form textile (plus its
  tumble-dryer function where fitted); any other application is misuse, for
  which the manufacturer accepts no liability.
- Unauthorised modification of the machine or its control system is
  forbidden; changed or replaced parts must be THEN-original or THEN-recommended.
- It is forbidden to change the software of the programmable control system.

## Electrical hazards

The machine is fed at 400 V / 50 Hz, its control circuits use 220 V AC / 24 V
DC, and its main isolator is rated 250 A — values read from the UXLA00379
drawing-set cover sheet and carried from the electrical record, so they are
[OCR] and must be confirmed against the sheet before use [^uxla]. These are
hazardous voltages.

Manufacturer-documented points [^safety]:

- Supply-voltage danger exists inside the main electrical cabinet; machine
  operators must not open it.
- Before maintenance or repair work, switch off the motor and the main
  switch and protect against re-energization ("将电动机和主电闸关闭并做好保
  护") [interpretation] — the exact lockout arrangement is the site's own.
- Persons working on the electronic system and electrical equipment must be
  skilled electricians or persons under the guidance and supervision of a
  skilled electrician, and must comply with electrical-engineering
  regulations.
- Opening the side covers of the lifting roller requires the machine to be
  shut down and the main-cabinet main switch isolated.

> [!WARNING]
> The machine contains hazardous electrical energy. Fault diagnosis may involve
> energized equipment. Before any physical intervention, apply the site's
> approved isolation / lockout procedure and verify that the equipment is
> de-energized. Only appropriately qualified personnel may perform electrical
> work on this machine. The isolation and lockout procedure itself is **not
> documented in any source here** — it is a site-specific procedure.

## Pressure and temperature hazards

The machine is a pressurised vessel heated by steam [^safety][^then]. The
manufacturer's safety guideline governs access whenever the vessel is hot or
under pressure; the same thresholds appear in the operating manual [^safety][^then]:

- **Door-opening conditions (kier working door, filter working door, manhole):**
  the machine must be depressurized (pressure gauge reading 0 bar), the
  temperature must be below **80 °C (176 °F)**, and — for the filter working
  door and the manhole — the kier must hold no residual liquid (check the
  controller's level indication) [^safety][^then].
- **Re-evaporation residual pressure.** Working doors are closed by
  toggle/stud bolts, one of which is a safety device that holds the cover and
  allows a gap of about 3 mm before full opening, so residual pressure escapes
  safely by re-evaporation. Bolts must be slackened slowly, one at a time [^safety][^then].
  Manholes with ordinary bolts are slackened diagonally, a few turns at a time,
  before removal by hand [^safety].
- **Sampling and liquor draining.** The dye liquor must be cooled below
  80 °C (176 °F) and the machine depressurized before sampling or draining;
  the injection system is switched off first for sampling [^safety].
- **Salt addition.** Salt/dissolving is temperature-guarded on valve VD (V300):
  salt may only be added below 80 °C (176 °F) [^then].

**Safety interlocks on external valves** — the guideline's safety-circuit
chapter states that valves operated from outside the pressure vessel must be
interlocked above 80 °C (176 °F) and above **0.4 bar**, and documents the
interlock-check components and thresholds [^safety]:

| Interlock [confirmed] | Engages | Components the guideline names |
| --- | --- | --- |
| External working-valve interlock | above 80 °C and above 0.4 bar | general |
| Pressure interlock | pressure above 0.3 bar engages the interlock branch (check: pressure valve VEL opened to ~0.5 bar) | pressure switch **F1110**; pressure transmitter **B1112**; pressure locking valve **Y177** |
| Temperature interlock | ~90 °C (194 °F) in the check (heat the vessel to around 90 °C) | temperature-regulator switch **N1102**; temperature probe **B1100**; temperature locking valve **Y176** |

This is a summary of the manufacturer's check checklist, not a work
instruction; only qualified personnel perform these checks, and safety devices
must never be bypassed [^safety].

**Blower (air circulation) start and running constraints** [^safety]:

- Before the blower starts: no dye liquor may be in the blower (controller
  water-level indication below ~95 % and a visual check of the kier level);
  static pressure must be below **1 bar** (gauge); the VX flap must be closed.
- The blower must not be run at zero setting (VX flap closed) for more than
  **five minutes**; the blower motor's rated output and the VX-flap / static
  pressure set values must stay within their permitted ranges.
- Kier water level "Nda" reads at a maximum of ~95 %: above that, water or dye
  liquor can be drawn into the blower.

[confirmed] figures in this section are read from the safety guideline's text
layer; IB29530B / IB29530C installation sheets carry related pressure figures
which are image-only and [OCR] (see below).

**Installation-schematic pressure figures [OCR]** — the installation plan and
installation scheme are single-page, image-only scans [^instb][^instc] with no
readable text layer; the figures below come from the OCR pass made at
inspection and were NOT re-verifiable from the scan in this review. Treat every
figure here as unverified until it is read directly from the sheet:

- Steam supply pressure: minimum 6 bar, maximum 8 bar, and the pressure must be
  reduced to the machine / heat-exchanger service pressure [^instc][OCR].
- Soft water supply: 2–3 bar, maximum 3 bar [^instc][OCR].
- The safety-valve relieving capacity and set pressure are printed on the
  installation plan [^instb][OCR]; the set-pressure value could not be re-read
  reliably this session and is not asserted here ([interpretation] of the OCR
  readings was ambiguous) — verify directly on the sheet.

**Safety valve.** The machine is fitted with a safety valve. Its settings must
never be changed; its inlet, discharge and internal passages must be kept clear
and clean; it must be checked regularly, and its handle may be lifted only to
flush it, e.g. when not pressurised [^safety].

## Mechanical hazards

- Rotating drum / rollers present an injury hazard; moving fabric must not be
  touched, and the machine must be allowed to cool before touching [^safety].
- Motors, drives, transmissions, agitators, couplings and lifting devices must
  be guarded against contact; the machine must not be started until all guards
  are fully in place, and guards must never be removed unless the main switch
  is off [^safety]. Named guards include the blower guard and the lifting-motor
  guard [^safety].
- The working door carries a deflector so any liquid leaking past the seal
  flows downward, away from the operator [^then].
- Lifting/hoisting equipment (chains, ropes, slings, hooks, rings) and the
  lifting gear are on the manufacturer's periodic inspection list (see below)
  [^safety].
- Loading and unloading: the controller must be set to the load/unload
  program; gloves are required; mind the fabric loop and beware of hot steam
  pockets [^safety].
- Fabric being sampled or handled is hot — wear protective gloves [^then][^safety].

**Periodic safety inspection schedule** — [confirmed] from the safety guideline
[^safety]; safety devices must be checked, and the safety circuit (all
mechanical, electrical and pneumatic parts: sensors, relays, contactors,
wiring, control valves, valves, piping) must be checked weekly by THEN-provided
or qualified maintenance staff:

| Cadence [confirmed] | What is checked |
| --- | --- |
| Operator, daily | work clothing/PPE, machine condition (damage/wear), instruments (functional & visual), sight glasses (fogging, cracks) |
| Operator, weekly | threaded and hinge connections, seals on covers/locks (blower, pumps, sight glasses), solenoid valves and connections, safety devices (visual) |
| Professional, monthly | safety valve (functional; seals, max working pressure, inlet/outlet, lifting lever) |
| Professional, every 6 months | interrupt devices (covers, valves), control equipment, lifting equipment, warning/safety signs, lifting gear; statutory inspections |
| Professional, yearly | platforms, access platforms, railings; storage of dyes, chemicals and auxiliaries |

Additional rules: after repair or replacement of any safety-affecting part a
full safety check is required; after a machine standstill of more than three
days a full safety check is required; after electrical/electronic repair or
replacement a re-check (e.g. of the temperature interlock) is required; the
machine may return to production only after the responsible safety officer
releases it [^safety].

## Emergency stop and safety-related signals

- Emergency-stop buttons are provided at the operator panel and at the control
  cabinet. **Any** emergency-stop button or the main switch can shut down the
  machine [^safety]. The drawing set labels an "EMERG.-OFF input" on the PLC
  overview sheets [^uxla][OCR].
- The safety guideline's plant figure identifies: 1 = main switch, 2 = control
  cabinet emergency-stop button, 3 = operator-panel emergency-stop button, 4 =
  safety valve (4.1 = its lifting lever) [^safety].
- Operator-panel indicators and controls [^then][confirmed]: a temperature-lock
  lamp (温度锁定), a guide-roller / winch fault indicator (导布轮故障), a motor
  fault indicator (马达故障), an inhibit-signal lamp (禁止信号), and the
  emergency-stop control (紧急停运). These are operator-facing; the sources do
  not link them to specific drawing labels ([interpretation] — see the
  electrical record).
- The UXLA drawing set additionally labels a set of safety-related control
  signals — "EMERG.-OFF input", "signal cut-off", "press. interlock",
  "temperature interlock" — transcribed in the electrical record; all [OCR],
  verify against the sheet ([^uxla]).

**Manufacturer-documented fault-response actions** — emergency responses printed
in the safety guideline's "first-aid procedures" chapter (p. 18) and air-loop /
door chapters; given for diagnosis context, not as a repair procedure [^safety]:

- On any fault, report it immediately to the dyehouse management; depending on
  the danger, press the red emergency button (operator panel or control
  cabinet) and turn the main switch to zero. For a minor leak, cool the machine
  below 80 °C.
- Feed-water line leak (e.g. at the heating device): close the feed-water
  main valve.
- Sight-glass leak: do not tighten the flange-edge screws while the machine is
  running.
- Frost risk: empty the machine, including pumps and actuators.
- Specific failures, all manufacturer-documented:
  - Steam supply valve **VLZ** stuck open — manually close the main valve at an
    appropriate distance from the kier.
  - Fill-water valve **VCZ** not closing and water overflowing — close the
    control valve by hand, or press the emergency button, or cut the main power.
  - Level sensor failure with overflow — press the emergency-stop button or cut
    the main power.
  - Reflux valve **VD** stuck open or opening unexpectedly — press the
    emergency-stop button or cut the main power.
  - Any danger during unloading — press the emergency-stop button or cut the
    main power.
- Sudden machine balance error ("sudden balance error") — close the
  main-cabinet main switch or press the operator panel's red emergency-stop
  button, then find and eliminate the cause [^safety].

## Chemical and process hazards

- Dyeing uses corrosive and toxic chemicals; a leak from the vessel, seals,
  pumps or piping can bring chemicals and hot dye liquor into contact with the
  body — a chemical-contact hazard the guideline calls out [^safety].
- Chemicals, auxiliaries and dyes must be handled and stored to the relevant
  rules and their own safety data sheets (chemical properties, permitted
  heating gradient, dosing speed, buffers); the operating company is
  responsible [^safety].
- Equipment must be rinsed after every batch; substances that can react
  dangerously together must not be used; correct disposal is required [^safety].
- **Stainless-steel corrosion warning** — the guideline states that stainless
  steels 1.4571 and 1.4401 do not resist halide (chloride, iodide, bromide)
  solutions; pitting (with localised corrosion able to penetrate the sheet) is
  especially dangerous. This applies to bleachers (hydrogen peroxide or sodium
  peroxide) and to bleach liquor (sodium hypochlorite, sodium chloride) [^safety].
- Cleaning with hydrochloric-acid-containing solutions is forbidden unless it
  is immediately followed by correct passivation [^safety].
- No food in the machine [^safety].
- High-temperature discharge (optional): a check valve is required downstream
  to prevent dye liquor and steam returning from the drain; discharge must be
  collected in a closed system to protect personnel; a collection tank must be
  temperature-monitored to stay below boiling; if a mixing cooler is used its
  safety thermostat must be monitored so that, on cold-water loss or control
  failure, steam and hot water cannot flow back into the drain [^safety].
- Salt dissolving duty: keep below the solubility limits (recommended
  reference values printed in the manual: refined salt / sodium chloride at
  ~250 g/l, sodium sulphate per the printed temperature table) — otherwise
  crystallisation can destroy the metering pump and stirrer mechanical seals;
  base the figures on solubility at 20 °C (68 °F) and stay at least 50–100 g/l
  below saturation [^then].
- Emergency eye-rinse facilities and professional first-aid personnel are part
  of the plant requirements listed in the guideline [^safety].

## Diagnostic safety boundaries

This record distinguishes three kinds of statement:

1. **Hazard information documented by the manufacturer** — [confirmed] or [OCR]
   material in the sections above, transcribed from the cited sources.
2. **Diagnostic context inferred from the documentation** — [interpretation]
   readings, where the text does not state the fact outright (for example the
   correspondence of panel indicator lamps to drawing labels, or the sense of
   "protect against re-energization" for the main switch). These carry no
   authority as instructions.
3. **Site-specific procedures that are NOT documented here** — the site's
   isolation/lockout procedure, its confined-space entry rules, its PPE policy
   and its vessel-entry authorisation. None of these appear in the sources and
   none is implied by this record.

Boundaries relevant to diagnosis:

- The sources document what the hazards and safety-related signals ARE; they
  do not provide a general fault-resolution procedure. If a fault occurs, the
  response must come from the machine's own service documentation or the
  manufacturer, against the emergency actions quoted above.
- Safety interlocks, emergency stops, guards and protective systems must not be
  defeated, bypassed, modified or removed [^safety]. The guideline explicitly
  forbids modifying the machine or its control system without authorisation
  and forbids configurations ("其它配置") that weaken or switch off the safety
  functions; the emergency button must remain reachable at all times [^safety].
- Diagnosing a fault is not a licence to operate hot, pressurised or energized
  equipment. Any physical intervention on the vessel, piping or electrical
  systems follows the manufacturer's access conditions (depressurised, below
  80 °C, de-energized) and the site's approval procedures [^safety][^uxla].
- Where a diagnostic change to operational software would be involved, the
  guideline forbids changing the programmable control system's software; such
  work belongs to the manufacturer or an authorised service act [^safety].

## Not documented

- **Maximum operating pressure and maximum design/dyeing temperature of the
  vessel:** not stated in the text-layer sources. The safety-valve set/relieving
  pressure is printed on the installation plan IB29530B but is image-only and
  was not reliably re-read this session — read it from the sheet and from the
  machine's pressure-vessel nameplate [^instb].
- **Steam, water, compressed-air and instrument-air pressure values** referenced
  in the guideline's "correct use" chapter are pointed at the wiring diagram,
  not printed there [^safety]; the utility-side figures on IB29530C are [OCR]
  and unverified [^instc].
- **Site lockout / isolation procedure, confined-space entry procedure, vessel
  entry authorisation, and PPE policy**: not in any source; site responsibility.
- **Electrical ratings beyond 400 V / 50 Hz, 220 V AC / 24 V DC and the 250 A
  main isolator**: not documented; see the electrical record [^uxla].
- **PLC bit addresses, terminal numbers, wire numbers and alarm-code meanings**:
  not provided by the safety sources; the electrical record's constraints apply.
- **Component repair procedures** for the safety valve, guards, doors or
  interlocks: not provided and deliberately not constructed here.
- **Maintenance intervals beyond the safety inspection schedule above**: the
  operating manual contains no maintenance/troubleshooting chapter [^then].

## Sources

[^safety]: `sources/textile-machinery/特恩高溫氣流染色機SYN G2安全指引.pdf` — THEN-AIRFLOW SYN G2 安全指引 (Safety Guideline), v1.0; 特恩机械有限公司 (THEN Machinery (HK) Ltd.); text layer readable; printed page numbers 3–24 cover the foreword, general rules, definitions, machine hazards, hazard sources (p. 9), work areas, authorised operators, PPE (p. 11), premises measures, safety devices and their function (p. 14), safety-device inspection checklist (p. 15–16), safety-circuit periodic check incl. interlock components/reset values (p. 17–18), first-aid procedures (p. 18), main-switch / emergency-stop / safety-valve plant figure (p. 19), pressure-vessel and air-circulation rules (p. 20–21), door/filter/manhole opening rules (p. 21–22), sight glass, liquor drain, safety valve, high-temperature discharge, sampling and loading/unloading rules (p. 23–24).

[^then]: `sources/textile-machinery/THEN高温气流染色机SYN G2.pdf` — THEN-Airflow SYN G2 使用说明书 (Operating Manual), v2.0; THEN Machinery; text layer readable; operator-panel signals (§2.1), loading-door toggle-bolt safety and the door deflector (§4), salt addition temperature guard on VD/V300 (§8), sampling and unloading door-opening conditions at ≤ 80 °C and 0 bar (§9.2, §10.2).

[^uxla]: `sources/textile-machinery/37029530~531  UXLA00379.pdf` — UXLA00379 electrical drawing set, SYN1200 G2, order 37029530-31; FONG'S EUROPE GMBH; image-only scan ([OCR]); machine electrical identity and the EMERG.-OFF input are carried from the electrical record and must be confirmed against the sheet.

[^instb]: `sources/textile-machinery/IB29530B .pdf` — Installation schematic plan (connection points, safety-valve relieving data), SYN1200 G2, order 37029530-31; FONG'S EUROPE GMBH; single-page image-only scan ([OCR]).

[^instc]: `sources/textile-machinery/IB29530C .pdf` — Installation scheme, utility specifications (steam, soft water), SYN1200 G2, order 37029530-31; FONG'S EUROPE GMBH; single-page image-only scan ([OCR]).