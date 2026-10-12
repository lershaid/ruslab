# Review of «Концепция Green Lab» (version with Kuznetsova's tracked edits, 2026‑10‑08)

Scope of this review: (1) mistakes or omissions that become difficult or expensive to correct once the concept is frozen into a Terms of Reference (ToR / ТЗ на проектирование) and the design starts; (2) conflicts or gaps against ISO/IEC 17025:2017 and the other ISO standards a testing laboratory is assessed against.

Source reviewed: `Концепция_Green_с_правками_Кузнецова.docx`, all tracked changes read (205 insertions, 27 deletions by «Кузнецова»).

---

## 0. Verdict in short

- The tracked edits are technically sound. Everything they add (argon supply, nitrogen generator, clean acid room 1а, organic prep 5а, solid prep 5б, sample storage 9а, unified earthing, 100 % outdoor air, stack/sampler separation, decision list in III.8) is correct and moves the document in the right direction. Several figures were spot‑checked against vendor data and are right (see section 4).
- There are no hard "violations" of ISO/IEC 17025 in the concept, because 17025 does not prescribe layouts, cleanroom classes or GLP. But four things in the current zoning would be raised at an accreditation assessment (section 2.1–2.2, 2.5).
- The expensive risks are not in what is written but in what is still undecided or missing: jurisdiction/codes, the accreditation scope (method list), the building program (plant rooms, gross area), the HVAC definition (hood schedule, pressure cascade, exhaust treatment, cleanroom class), and an over‑specification (Ex‑rated electrics for a whole room). These must be fixed in the ToR, not left to the designer.

---

## 1. Mistakes and omissions that are expensive to correct after the ToR

Ranked by cost of late correction.

### 1.1 Jurisdiction and governing codes are not fixed; the document mixes EU, US and IEC references

The text cites EN 12341, EN 14175, ISO 14644 (EU) alongside ANSI/ASSP Z9.5, NFPA 55, ANSI/ISEA Z358.1, 40 CFR 58, the EPA PM2.5 method (US), and IEC 60364/60825. A ToR must name, for the actual country and site:

- building and fire code (occupancy class, compartments, sprinklers vs. gas suppression in instrument rooms);
- electrical code and hazardous‑area classification scheme (ATEX / IEC 60079 vs. NEC 500);
- fume‑hood test standard (EN 14175 vs. ASHRAE 110) and lab ventilation standard (EN 14175‑/DIN 1946‑7 vs. ANSI Z9.5);
- flammable‑liquid and compressed‑gas storage limits;
- radiation licensing regime for the WDXRF (closed source, but licensed in most jurisdictions);
- the national regulatory methods for each matrix (this decides the weighing‑room climate, see 1.4, and much of the equipment list).

Why expensive: a design made against the wrong code set is redone, hoods bought to the wrong test standard, electrical equipment with the wrong certification, a weighing room with the wrong humidity system.

### 1.2 Scope of accreditation (method list) is undefined, so the room and equipment program is incomplete

The concept lists "directions" but no methods. Mapping the claimed services to the equipment list shows functions that each need a room or substantial utilities and are not in the program:

| Claimed service | What is missing | Space / utility impact |
|---|---|---|
| Drinking, natural and waste water "control"; "reference center" | A wet‑chemistry lab for general parameters (pH, conductivity, turbidity, BOD5, COD, TSS, nutrients, TOC, oil & grease, phenols, cyanide, surfactants) with hoods, BOD incubator, drying oven, TOC analyser. The concept deliberately moves away from wet chemistry, but regulatory water monitoring cannot be done without these. | ~30–40 m² bench lab, 2–3 hoods |
| VOC in ambient and workplace air | Thermal‑desorption unit and/or canister autosampler plus canister cleaning system for the GC‑MS/MS; purge‑and‑trap or headspace for VOC in water. Without them the GCMS‑TQ8050 cannot do ambient VOC. | Space, zero‑air/He, vacuum and exhaust in room 2 |
| "Reference center" for air quality | Gaseous reference analysers (NOx chemiluminescence, SO2 UV‑fluorescence, O3, CO, BTX) and a gas‑analyser calibration lab (dilution calibrator, zero‑air generator, permeation ovens, transfer standards). Only portable stack analysers are listed. | Separate calibration room with its own gas infrastructure |
| PM source apportionment / fingerprinting | EC/OC analyser (thermal‑optical). Metals + ions without EC/OC is an incomplete speciation set. | Instrument space, gases |
| Heavy metals | Dedicated mercury analyser (CV‑AAS/AFS or direct). ICP‑MS is not the practical tool for Hg in routine monitoring. | Small |
| "СОЗ" (POPs) | If dioxins/furans/PCBs are meant, a dedicated dioxin suite (separate, ¹³C‑labelled standards, usually GC‑HRMS) is required. Either exclude explicitly or plan a suite. | Separate suite |
| Industrial emissions for ПЭК / tax | Isokinetic stack‑sampling trains (dust EN 13284‑1 / EPA M5, metals EN 14385), probe cleaning and stack‑filter weighing. | Workshop and weighing capacity |
| Biomass / pellet export certification | ISO 17225 needs calorimetry, ash, moisture, chlorine; CHNS alone does not certify fuel. | Fuel‑lab bench, calorimeter |
| "Carbon footprint (ESG)" | This is an ISO 14064/14067 calculation, not a CHNS measurement. The claim is conceptually wrong and should be removed from the lab's services. | None, but misleading in a ToR |
| Ecotoxicology, drinking‑water microbiology | Already flagged by the editor as decisions; both need separate suites with own ventilation. | Separate suites |
| "Обязательная аттестация рабочих мест" | In Russia this is СОУТ (426‑ФЗ) with its own accreditation and sampling equipment; elsewhere different. Depends on 1.1. | Field equipment store |

Why expensive: the 20–30 % area reserve the editor proposes will be consumed by two or three of these items alone. The decision which of them are in scope belongs in the ToR.

### 1.3 There is no building program: gross area and plant rooms are missing

Net area of the rooms listed in 2.4 sums to roughly 325–400 m² (lab + office). Not in the program at all:

- HVAC plant (air handling units for 100 % outdoor air with run‑around heat recovery, exhaust fans, scrubbers), which for a chemical lab is the largest technical space;
- electrical room (step‑down transformer for the XRF, central UPS, diesel generator with fuel store and acoustic enclosure);
- IT/server room (see 2.5);
- compressor / nitrogen‑generator room (the editor places it "in the ramp or a niche"; it is a noisy heat source and should be a room);
- hazardous‑waste store with external access (currently inside the sample store, see 2.1);
- loading dock / sample receiving dock; vehicle bay and field‑equipment store (28 sampling stations imply a vehicle fleet and consumables logistics);
- gowning airlocks for rooms 1, 1а, 7; corridors; staff amenities (the editor added these); cleaning/janitor room.

Rule of thumb for chemical laboratories: gross area is 2–2.5 × net. Expect 800–1000 m² gross, not 400. Undersized plant rooms are the most expensive retrofit in a lab building.

### 1.4 HVAC is not defined to the level a designer can price

- **Fume‑hood schedule.** The editor correctly says hood count and width per room must be fixed before design. This is the single largest cost driver (each hood ≈ 500–1000 m³/h of conditioned outdoor air). The ToR must also fix VAV vs. CAV, face velocity, diversity factor, night setback.
- **Exhaust treatment.** No scrubbers are specified for the acid/HF exhaust (room 5, 1а) or the ICP‑MS plasma exhaust. In most jurisdictions the lab needs its own emission permit, and the roof PM monitor would otherwise measure the lab's own exhaust. Scrubbers need roof or plant space and drains.
- **Pressure‑cascade conflict in room 1а.** The clean acid room is specified at positive pressure (подпор) while HF and HNO3 are handled in it. Lab‑safety standards (ANSI/ASSP Z9.5, NFPA 45) require rooms with hazardous chemicals to be negative to non‑lab spaces. The standard trace‑metal clean‑lab solution is: room positive to its own gowning anteroom, anteroom negative to the corridor, all acid work inside PP hoods, HF only in closed digestion vessels. This must be drawn as a pressure‑cascade diagram in the ToR; left to interpretation, the contractor builds one or the other and reworking HVAC is expensive.
- **Cleanroom class is ambiguous.** "ISO 6–7" with "ISO 5 workplaces" is not a specification. ISO 14644‑1 requires the class and the occupancy state (as‑built / at‑rest / operational). ISO 6 roughly doubles the air‑change rate of ISO 7 and adds ISO 14644‑2 requalification cost for the life of the lab. Recommendation: room 1а — ISO 7 at‑rest (ISO 8 operational), ISO 5 inside PP laminar hoods; room 1 (ICP‑MS instrument room) — HEPA‑filtered, positive pressure, but no formal classification unless there is a method requirement.
- **Weighing‑room climate.** The editor correctly makes this depend on the reference method (EN 12341 vs. EPA). Humidification vs. dehumidification is a different HVAC system; the choice must be in the ToR, not "to be decided".

### 1.5 Explosion‑proof (взрывозащищенное) electrical equipment for the whole room 5а is an over‑specification

Standard organic‑prep equipment (rotary evaporators, accelerated solvent extraction, SPE manifolds, nitrogen evaporators, fridges) is not available Ex‑rated, and Ex‑rated lighting, sockets and controls for a 25 m² room are costly. The correct approach is a hazardous‑area classification by risk assessment (IEC 60079‑10‑1 or NFPA 45): with hoods and local exhaust the room is unclassified; only the interior of solvent cabinets and waste containers is Zone 2. Keep Ex‑rated exhaust fans for the reagent store (room 6) and for solvent‑cabinet venting. Written as it is, the ToR will either be ignored by the designer or priced at a premium.

### 1.6 The "ppt" ultra‑trace ambition drives the most expensive package; decide whether it is needed

ISO 6 clean room, PP laminar hoods, Savillex acid purification, Type I water at point of use, metal‑free finishes and gowning are the "geochemistry / semiconductor" level. Regulatory limits for the stated markets are µg/L in waters and ng/m³ for metals in PM, which an ISO 7/8 metal‑free prep room with PP hoods achieves. Two consistent options:

- keep the ppt package, but limit the claim to drinking/natural waters and filters (ppt in waste water is not achievable in any lab because of the matrix, and should be removed from 1.1 and 1.2);
- or drop to ISO 7/8 and save on HVAC, finishes and validation.

Either is defensible; leaving both in the text is not.

### 1.7 The building is being designed around instrument models that may not survive procurement

The site‑prep figures in the text are correct for the named Shimadzu and Rigaku models (verified, section 4). But if a tender yields a different vendor:

- ICP‑MS argon rises from 11 L/min at 99.95 % to 15–20 L/min at 99.996 % (most other vendors);
- the WDXRF may be 3‑phase: Rigaku's own tube‑below variant (ZSX Primus IVi) is 600 kg, 3‑phase 200/208 V, 40 A (~14 kVA), versus the tube‑above IV at 620 kg, single‑phase 200 V, 8 kW;
- LC‑MS in high‑flow gas mode needs ~27 L/min N2 plus ~29 L/min dry air, versus the ~25 L/min total in the text (standard mode).

The ToR should state design envelopes with margins (gas flows, power, heat, mass, crate dimensions), and "or equivalent" if public procurement rules apply.

### 1.8 Fire safety and the hazardous‑materials inventory are not addressed

Quantities of flammable solvents, acids (HF, HNO3, and whether perchloric acid is used), and compressed/liquefied gases per room determine the occupancy classification, fire compartments, sprinkler vs. suppression choice, fire rating of the reagent store and cylinder‑storage rules. Without the inventory the fire authority rejects the design or the designer over‑builds. One specific decision cannot be retrofitted: perchloric‑acid digestion requires wash‑down hoods and dedicated ductwork. State explicitly "no perchloric acid" or include the hoods.

### 1.9 Smaller items that are still cheaper to fix now than later

- Emergency showers and eyewashes need a tempered‑water supply (ANSI Z358.1: 16–38 °C) and floor drains; plumbing that is hard to add afterwards.
- "Высота этажа 4,2–4,5 м" should be stated as floor‑to‑floor and complemented by a minimum clear height under services (≥ 3.0 m) to avoid disputes.
- A Type II water ring main through the building (III.6) is prone to stagnation and is hard to change; point‑of‑use Type II + Type I units are the usual choice. Not a mistake, but a decision to make consciously.
- The microwave digester TANK 40 "inside a fume hood" needs a hood sized for ~60–80 kg and its depth; vendors normally bench‑mount it beside the hood with its own exhaust port.
- The LIMS server in "a lockable vestibule with a split AC" is inadequate for the primary record system (see 2.5); plan a small IT room.

---

## 2. ISO/IEC 17025 and related ISO standards

Preface. ISO/IEC 17025:2017 does not prescribe layouts, cleanroom classes or GLP. The facility‑relevant clauses are 6.3 (facilities and environmental conditions), 6.4 (equipment, including storage and handling), 6.5 (metrological traceability), 7.3 (sampling), 7.4 (handling of test items), 7.11 (control of data and information management), 8.4 (control of records). The editor's replacement of "GLP" by "ISO/IEC 17025 п. 6.3" and the removal of the pharmaceutical "one‑way flow" rule are both correct. Against those clauses:

### 2.1 Incompatible activities co‑located (6.3.4 c; 7.4.3–7.4.4)

- **Room 8** combines sample reception/registration with the field‑equipment workshop (purging, repair, calibration of gas analysers) and cylinders of toxic calibration gases. Water samples for trace metals, VOC tubes and PM filters cannot be received and logged in a workshop atmosphere. Separate a clean sample‑reception room (adjacent to cold storage, pass‑through to the labs) from the field‑equipment workshop/store.
- **Room 9а** combines the sample store and archive (test items under 7.4) with hazardous‑waste collection (solvent and acid waste). Solvent vapours contaminate organics samples and filters, and assessors flag this co‑location. Separate rooms; the waste store needs external access.

### 2.2 Storage of reference standards and CRMs is not defined (6.4.3, 6.5)

Certified reference materials, calibration‑gas standards, E2 reference weights for the microbalance and reference filters need defined, monitored storage (fridge/freezer with logging, a reference‑weight cabinet in the weighing room). No location or conditions are given.

### 2.3 Documented facility and environmental requirements (6.3.1–6.3.2)

The ToR should carry a Room Data Sheet per room: temperature, humidity, pressure differential, particle class and state, vibration criterion, EMI, lighting, utilities, hood count, loads, alarm limits. The current text has these scattered and partly undetermined (weighing room; cleanroom class). Monitoring with logging and alarms (6.3.3) is included, which is good; add integration with LIMS for data integrity.

### 2.4 Access control and confidentiality (6.3.4 a; 4.2)

Only the XRF room has access control. The whole laboratory block must be access‑controlled against visitors (Block D). The glass partitions between the negotiation room and Block A are acceptable, provided visitors stay outside the controlled zone and cannot see other clients' samples or results on screens.

### 2.5 Control of data and records (7.11; 8.4)

For the primary record system (LIMS) and terabytes of raw spectra, 7.11.3 requires protection against loss and unauthorised access and backup. A server rack in a vestibule with a split unit does not meet that. Specify a small IT room with UPS, cooling, fire suppression and off‑site backup, and a records archive (paper and electronic) separate from the sample archive.

### 2.6 Sampling infrastructure (7.3)

With 28 stations, stack sampling and workplace air, sampling is within scope and needs a traceable calibration bench for flow calibrators and samplers, sampler maintenance space, cold chain and vehicles. Room 8 partly covers this; make it explicit.

### 2.7 "Референс‑центр" is not an ISO/IEC 17025 status

If it means a national or regional reference laboratory for air quality (EU Air Quality Directive, Art. 3 logic), the lab must be accredited for the reference methods (EN 12341, 14211, 14212, 14625, 14626, 14662, 14902, 15549, 16913, 16909) and take part in the corresponding QA/QC programmes. None of the gaseous reference analysers are in the equipment list (see 1.2). If it means producing reference materials or running proficiency‑testing schemes, ISO 17034 and ISO/IEC 17043 apply, with their own infrastructure. Define the term.

### 2.8 Other ISO references

- ISO 14644‑1: class and occupancy state must be specified (see 1.4); ISO 14644‑2/‑3 then impose periodic requalification.
- ISO 3696 water grades and ISO 8573‑1 class 1.4.1 compressed air are cited correctly.
- ISO 14001 / ISO 45001 are not required for accreditation and are rightly not cited.

---

## 3. Internal inconsistencies and factual errors to fix before the ToR

- **Table 2.3:** room 7 (весовая) still sits under Block B in the table while the text declares it Block A. Move the row.
- **III.5 gas lines:** the bullet now states stainless steel is mandatory and, two sentences later, that copper is admissible per vendor site‑prep. Pick one (stainless for He/N2 to GC‑MS; copper acceptable for Ar to the Shimadzu ICP‑MS, stainless preferred).
- **1.2 table:** "расчет углеродного следа" by CHNS — remove (see 1.2). "подтверждение экспортного качества пеллет" needs calorimetry, ash, moisture, chlorine.
- **1.1 / 1.2:** "ppt" in waste water — remove. "Cary 60/630" are Agilent instruments. "DustTrack" → DustTrak (TSI). "Стандарт: ISO 7" → "ISO 14644‑1 class 7, at‑rest".
- **EN 12341 conditions:** the standard specifies 20 ± 1 °C and 50 ± 5 % RH, i.e. 45–55 %, not "45–50 %". Check against the standard text before it goes into a room data sheet.
- **LC‑MS gas:** "до ~25 л/мин" is the standard‑mode figure (Peak Genius 1051). State the operating mode; high‑flow mode needs roughly double.
- **XRF:** the figures (620 kg, 1310 × 1470 × 890 mm, single‑phase 200 V, 8 kW) are for the tube‑above ZSX Primus IV. State the variant.
- **BAM 1020 "on the roof":** the instrument needs a climate‑controlled enclosure (manual range 0–50 °C, agencies hold 20–30 °C). The editor's "павильон" must be specified as climate‑controlled.
- **Room 1:** "антивибрационный стол (не из металла)" for a ~100 kg ICP‑MS is unusual; metal frames with epoxy or PP cladding are standard. Relax to "no exposed bare metal".
- **Earthing "не более 2–4 Ом":** vendor requirements are typically ≤ 10 Ω (or class D, 100 Ω). The figure is unjustified; use the vendor value or drop it.
- **Lidar:** the Lufft CHM 15k is a ceilometer (Class 1M, eye‑safe); the "laser safety zone" requirement is largely moot. Keep the roof penetration, base and cabling.

---

## 4. Items checked and found correct (no need to re‑open)

- ICP‑MS 2040: argon ~11 L/min in normal mode, 99.95 % purity acceptable, 7 m³ cylinder ≈ 10 h (Shimadzu).
- ZSX Primus IV (tube‑above): ~620 kg, 1310 × 1470 × 890 mm, single‑phase 200 V, 8 kW (Rigaku).
- Nitrogen/dry‑air generator at ~25 L/min total for LCMS‑8050 standard gas mode (Peak Genius 1051 sizing).
- BAM 1020 requires a climate‑controlled shelter; siting away from exhaust stacks per 40 CFR 58 App. E.
- ANSI/ASSP Z9.5 stack guidance (≥ 3 m above roof, ≥ 15 m/s), ANSI/ISEA Z358.1 (10 s travel), NFPA 55 oxygen/fuel‑gas segregation.
- IEC 60364: a separate independent earth electrode is not permitted; the editor's correction is right.
- 100 % outdoor air, no rotary heat recovery; separate acid and solvent exhaust systems; PP/PVDF ductwork.
- Removal of GLP references and of the pharmaceutical one‑way‑flow rule.
- Weighing room moved to the clean block with airlock, 48 h conditioning racks, ionizer, microbalance 1 µg for the EPA method.

---

## 5. Decisions that must be in the ToR (extends section III.8 of the document)

1. Country, site, new build vs. fit‑out, number of storeys; the full set of governing codes (1.1).
2. Scope of accreditation: method list per matrix, with explicit yes/no for wet chemistry, VOC/TD, gaseous reference analysers and calibration lab, EC/OC, Hg, dioxins/POPs, stack sampling, fuel lab, ecotoxicology, microbiology, СОУТ (1.2).
3. Sample throughput per matrix and staff headcount (amenities, egress, parking).
4. Reference method for PM10/PM2.5 (weighing‑room climate) — already in III.8.
5. Hazardous‑materials inventory per room; perchloric acid yes/no (1.8).
6. Fume‑hood schedule per room; pressure‑cascade diagram; cleanroom class and occupancy state (1.4).
7. Instrument list with design envelopes and vendor site‑prep; "or equivalent" policy (1.7).
8. Building program with gross area and all plant rooms (1.3).
9. Siting of the monitoring station and lidar — already in III.8.
10. LIMS/IT architecture, data retention and backup (2.5).

Recommended format for the ToR: convert sections 2.3–2.4 into one Room Data Sheet per room and one engineering‑load matrix, separate "shall" requirements from recommendations, and put every open item from this list into a "decisions required" table with an owner and a date.
