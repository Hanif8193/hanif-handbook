# Textile-Machinery Sources → KSoR Mapping Plan

Planning document only. No knowledge records were created. Authoritative content
must be transcribed from the PDFs themselves at authoring time; every non-text
(or garbled-text) source was OCR-read during inspection, and load-bearing
values must be hand-verified against the original page before approval.

Sources: `sources/textile-machinery/` (20 PDFs, byte-identical to
`C:\Users\pc\Desktop\textile` originals).

## Mapping table (20 PDFs)

Key: **K** = knowledge type codes (diagnosis `diag`, electrical `elec`, mechanical `mech`,
maintenance `maint`, operation `oper`, installation `inst`, safety `safe`,
instrumentation `instr`, process `proc`, other `othr`).
**Authority** = manufacturer / doc identity / date confirmed from page contents.
**Suitable** = suitable as the basis of an authoritative KSoR record (yes / partial / no).

| # | Source filename | Confirmed title / purpose | Machine/component | Proposed KSoR area | Proposed record(s) | K | Authority / provenance | Suitable | Limitations, ambiguity, OCR, safety |
|---|---|---|---|---|---|---|---|---|---|
| 1 | `37029530~531  UXLA00379.pdf` | Electrical control-drawing set (drawing index, PLC overview 1–2, analog I/O overview, pneumatic-module mounting plates, winch-store 1–4 control, terminal diagrams 1–6, inverter & flow-meter parameters, legend, kWh meter) — 75 pp | Fong's Europe THEN-Airflow **SYN1200 G2** dyeing machine, order **37029530-31**, controller DYNET | `machines/then-airflow-syn-g2/` | `electrical.md` | `elec diag instr proc` | FONG'S EUROPE GMBH, DWG.NO UXLA00379 R01/R02, designed Yang WeiGuo 05-06/10-07-2012, approved PWCHIU | yes | Image-only scan; OCR-only. 400 V / 250 A circuits — transcribe fault-signal & interlock lists against the sheets before stating them. Live-electrics safety. |
| 2 | `IB29530 .pdf` | General Layout Plan (views X/Y/Z/A, utility connection points, control-cabinet position) | SYN1200 G2 / 37029530-31 | `machines/then-airflow-syn-g2/` | `installation.md` | `inst proc` | FONG'S EUROPE GMBH, FEU No.KA111105/WA112617~18 | yes | Image-only; OCR-only. Dimensions approximate until measured. |
| 3 | `IB29530A .pdf` | Foundation Layout Plan (anchor bolts M12×120/M16×160/M20×200, loads 12 kN/350 kN/20 kN, "processing kier and pump to be fixed professionally") | SYN1200 G2 / 37029530-31 | `machines/then-airflow-syn-g2/` | `installation.md` | `inst mech` | FONG'S EUROPE GMBH, FEU No.KA111105/WA112617~18 | yes | Image-only; OCR-only; units/loads to be re-read from sheet. |
| 4 | `IB29530B .pdf` | Schematic Plan — connection points; air ≤7 Nm³/h, steam 1695 kg/h, cooling water 7690 kg/h; safety-valve relieving capacities DN50, set pressures 3/8 bar; elements DA/AT/HE | SYN1200 G2 / 37029530-31 | `machines/then-airflow-syn-g2/` | `installation.md` | `proc inst safe` | FONG'S EUROPE GMBH, FEU No.KA111105/WA112617~18 | yes | Image-only; OCR-only. Pressure/flow figures must be preserved exactly and cited. Steam/pressure hazard. |
| 5 | `IB29530C .pdf` | Installation Scheme — utility specs (steam min 6 / max 8 bar, soft water 2–3 bar max 3, stainless piping, pressure must be reduced to machine/HE service pressure, local inspection-authority note, transmitter-line rinse ≥2 bar ≤ vessel pressure) | SYN1200 G2 / 37029530-31 | `machines/then-airflow-syn-g2/` | `installation.md` | `inst safe` | FONG'S EUROPE GMBH, FEU No.KA111105/WA112617~18 | yes | Image-only; OCR-only; pressure limits are safety-load-bearing. |
| 6 | `IB29530D .pdf` | Installation Scheme — Valves & Fittings (customer-provided: cut-off/check/reducing valves, dirt traps, steam traps; grey cast iron / brass / stainless; PN10/16, 145/232 PSI; used with IB29530C) | SYN1200 G2 / 37029530-31 | `machines/then-airflow-syn-g2/` | `installation.md` | `inst mech` | FONG'S EUROPE GMBH, FEU No.KA111105/WA112617~18 | yes | Image-only; OCR-only; valve-rating table must be re-verified. |
| 7 | `IBAK159.pdf` | Injection-system / orifice-plate (Blende) selection & circuit sheet — machine-type table, "Lechler" nozzles, standard injection 80 Ltr, orifice plates F02–F09, injection pumps (VPH1/V060, VPH2/V061, VPHW2/V063, HW1/V062) "by means of frequency converter" | SYN G2 / AFE family (table includes AFE900/SYN1000/SYN1200 G2) | `machines/then-airflow-syn-g2/` | `injection-system.md` | `proc mech elec` | FONG'S EUROPE GMBH, Artikel-Nr. IBAK159; no order number printed | yes | Image-only; OCR-only. Order 37029530-31 link NOT printed (family-level only). Nozzle/orifice values must be read from the drawn table. |
| 8 | `THEN高温气流染色机SYN G2.pdf` | 使用说明书 v2.0 — operating manual: construction, DYNET touchscreen & symbols, loading/cancel, salt dosing, sampling, unloading (X-Y plaiting), program editor / manual program | THEN-Airflow SYN G2 dyeing machine | `machines/then-airflow-syn-g2/` | `operation.md` | `oper proc safe` | 特恩机械 / THEN Machinery, v2.0, DYNET | yes | Text layer OK. **No maintenance/troubleshooting chapter** — do not infer diagnostic content. Fault content = indicator symbols only. Dyeing chemicals → process safety. |
| 9 | `特恩高溫氣流染色機SYN G2安全指引.pdf` | 安全指引 v1.0 — safety guidelines (hazards, hot/pressurised vessel, chemicals, safe practice) | THEN-AIRFLOW SYN G2 | `machines/then-airflow-syn-g2/` | `safety.md` | `safe oper` | THEN-AIRFLOW SYN G2, v1.0 (Traditional Chinese) | yes | Text layer OK; Traditional Chinese → translate, keep warnings verbatim meaning. Safety-review gate. |
| 10 | `PUM00039c.pdf` | 电动机使用维护说明书 — WONDER motor usage & maintenance: direct / Y-Δ start, insulation test, wiring, lubrication intervals, brake motors, multi-speed, VFD motors, 高温排烟, full common-fault table, exploded-view parts list | Three-phase AC motors (WONDER, Fuzhou Wonder Electric) | `components/motors/` | `wonder-motor-guide.md` | `maint diag elec mech safe` | 福州万德电气 / WONDER, IEC60034/GB755/AS NZS1359:2004 | yes | Image-only scan; OCR-only. Fault table is the key value — transcribe carefully. Live-electrics + bearing/lubrication detail. |
| 11 | `PUM00040c.pdf` | 三相异步电动机使用维护技术指导书 — safety, start checks, operation monitoring, small/large maintenance schedule, §8 common-fault analysis & removal table, storage | Three-phase asynchronous motors (Wuxi Huada Motor) | `components/motors/` | `huada-motor-guide.md` | `maint diag elec mech safe` | 无锡华达电机 / WUXI HUADA MOTOR, 2004-1-1 | yes | Text layer usable (some garbled spans). Fault table high value. Live-electrics safety. |
| 12 | `PUM00036c.pdf` | 操作和维护手册 B1030 3/2004 — worm-gear reducer: installation, motor connection, start-up, maintenance (oil change 10000 h / 2 yr), oil-fill table, hollow-shaft lock-ring assembly | Worm-gear reducer units (NORD Drivesystems, Beijing) | `components/mechanical/` | `nord-worm-gear-reducer.md` | `maint mech elec inst` | 诺德(北京)传动 / NORD, doc B1030, 3/2004 | yes | Text layer garbled → verified via OCR; oil quantities/mounting positions must be re-read from page. |
| 13 | `PUM00031c.pdf` | VLT®2800 操作说明 MG.28.A2.41 — VFD operating instructions (installation, parameters, alarm/warning content present) | Danfoss VLT2800 frequency converter | `components/drives/` | `danfoss-vlt2800.md` | `elec diag oper safe` | Danfoss, MG.28.A2.41 (Chinese) | partial | CJK text layer garbled → alarm/warning list only moderate confidence; parameter/fault values must be verified against the PDF. Live VFD electrics. |
| 14 | `PUM00032c.pdf` | VLT® AutomationDrive FC 300 操作说明 MG.33.AA.41 — safety, install, programming, specs, ch.6 troubleshooting (warning/alarm list) | Danfoss VLT AutomationDrive FC 300 | `components/drives/` | `danfoss-vlt-fc300.md` | `elec diag maint oper safe` | Danfoss, MG.33.AA.41 (Chinese) | yes | Text layer OK. Troubleshooting chapter confirmed. Live VFD electrics. |
| 15 | `PUM00016c.pdf` | 电-气阀门定位器 使用说明书 — YT-1000 set-up, **故障诊断和措施** | YT-1000 electro-pneumatic valve positioner (YTC) | `components/positioners/` | `yt-1000-positioner.md` | `instr diag maint` | YTC / Young Tech YT-1000 (Chinese) | yes | Text layer OK. Pneumatic + 4–20 mA feedback calibration detail. |
| 16 | `PUM00017c.pdf` | YT-1000L positioner manual V1.01 — same family (variant of 16c) | YT-1000L positioner (YTC) | `components/positioners/` | `yt-1000l-positioner.md` | `instr diag maint` | YTC / Young Tech YT-1000L V1.01 | yes | Text layer OK. Cross-reference 16c to avoid duplicating common content. |
| 17 | `PUM00007c.pdf` | 压力变送器 技术资料 YB/PT-01-2006 — Cerabar PMC series: overviews, **selection tables**, technical data, wiring, zero/span adjustment, explosion-proof classes | Endress+Hauser Cerabar PMC pressure transmitter (PMC133…536(Z)) | `components/instrumentation/` | `endress-hauser-cerabar-pmc.md` | `instr elec safe` | Beijing Endress+Hauser Ripeness, YB/PT-01-2006 | partial | Garbled spans → OCR-verified. Primarily selection/data; no fault table. Ex hazardous-area classes must be stated with care. |
| 18 | `PUM00021c.pdf` | JUMO 90.2002 screw-in RTD (Pt100) datasheet — PL90 series | JUMO 90.2002 temperature probe | source-only (see §C) | `components/instrumentation/jumo-rtd-screw-in.md` (deferred) | `instr` | JUMO, PL90 series | partial | Thin datasheet; no diagnostic value. Keep source-only until a sensor-specific need arises. |
| 19 | `PUM00023c.pdf` | JUMO 90.2005 RTD (Pt100) with connecting cable, datasheet — PL90 series | JUMO 90.2005 temperature probe | source-only (see §C) | (same record as 18, if created) | `instr` | JUMO, PL90 series | partial | Thin datasheet; pair with 21c. Keep source-only. |
| 20 | `PUM00047c.pdf` | 弹簧式安全阀 安装使用说明书 — selection, transport/storage, installation, performance adjustment, **常见故障及排除方法**, maintenance | Spring-loaded safety valve (China Yongyi Valve Group) | `components/mechanical/` | `spring-safety-valve.md` | `mech safe diag maint` | 中国永一阀门集团, file YOY/CE.A74, v2004 (GB12243-89, ISO9002 referenced) | yes | Garbled spans → OCR-verified. Valve is an overpressure-protection device — adjustment/fault-remedy content needs safety review. |

## Proposed minimal KSoR directory structure

```
knowledge/
  index.md                                  # generated by ksor build — never authored
  machines/
    then-airflow-syn-g2/                    # machine-specific (order 37029530-31)
      overview.md       # identity, boundaries, component map, drawing index
      operation.md      # (8)  THEN operating manual
      safety.md         # (9)  THEN safety guidelines
      installation.md   # (2–6) IB29530 general/foundation/schematic/installation/valves
      electrical.md     # (1)  UXLA00379 electrical drawing set + fault signals
      injection-system.md # (7) IBAK159 nozzle/orifice selection
  components/
    motors/
      wonder-motor-guide.md     # (10) PUM00039c
      huada-motor-guide.md      # (11) PUM00040c
    drives/
      danfoss-vlt2800.md        # (13) PUM00031c
      danfoss-vlt-fc300.md      # (14) PUM00032c
    positioners/
      yt-1000-positioner.md     # (15) PUM00016c
      yt-1000l-positioner.md    # (16) PUM00017c
    instrumentation/
      endress-hauser-cerabar-pmc.md # (17) PUM00007c
      jumo-rtd-screw-in.md          # (18)+(19) deferred — one record, both JUMO part numbers
    mechanical/
      nord-worm-gear-reducer.md # (12) PUM00036c
      spring-safety-valve.md    # (20) PUM00047c
```

Rationale: machine-specific documents stay under one machine folder (single
order/drawing context, cross-referenced); generic component manuals sit under
`components/` as reusable records cited from the machine records; manufacturer
and doc identity are preserved per record via `sources:` frontmatter naming the
exact PDF path; nothing not in the sources is asserted.

## Classification

**A — Machine-specific records** (9 PDFs): #1 UXLA00379, #2–6 IB29530 series,
#8 THEN manual, #9 THEN safety guide. (#7 IBAK159 also machine-specific, folded
as `injection-system.md`.)

**B — Reusable component records** (9 PDFs): #10, #11 motors; #13, #14 drives;
#15, #16 positioners; #17 instrument transmitter; #12, #20 mechanical
components.

**C — Source-only unless a specific need arises** (2 PDFs): #18, #19 JUMO RTD
datasheets (thin, no diagnostic content; one record if ever needed).

**D — Especially careful safety review before approval**:
- `machines/then-airflow-syn-g2/safety.md` (#9) — hazard content governs.
- `machines/then-airflow-syn-g2/electrical.md` (#1) — live 400 V work,
  fault-signal interpretation.
- `machines/then-airflow-syn-g2/installation.md` (#2–6) — pressure/temperature
  limits, pressure-reduction requirement, local inspection authority.
- `components/mechanical/spring-safety-valve.md` (#20) — overpressure protection.
- `components/drives/*` (#13, #14) and `components/motors/*` (#10, #11) — carry
  live-electrics warnings; route through safety review as `sources:` include
  warnings.

## Recommended implementation order

1. `machines/then-airflow-syn-g2/overview.md` — identity, boundaries, source map.
2. `operation.md` + `safety.md` (THEN docs) → safety review gate on `safety.md`.
3. `installation.md` + `electrical.md` — highest diagnosis value; hand-verify OCR'd
   drawing values sheet-by-sheet.
4. Drive & positioner component records (#13, #14, #15, #16).
5. Motor & gearbox records (#10, #11, #12) — fault tables are the key content.
6. `endress-hauser-cerabar-pmc.md` (#17); JUMO datasheets stay source-only.
7. `spring-safety-valve.md` (#20); fold #7 into `injection-system.md`.
8. Every record: `npm run check` + `ksor build` clean, owner approval
   (`generated`/`approval` stamps) per governance before `npm run refresh` at the
   MCP rung.

## Verification

- Mapped source PDFs: **20 / 20** (rows 1–20 above).
- No source PDF modified (byte-identical copies verified at copy time).
- No knowledge/, instance.md, .ksor/, package files modified by this task.
- Git status below.