## 📋 Table of Contents

1. [Module Overview & Objectives](#-module-overview--objectives)
2. [Pre-Assessment Test](#-pre-assessment-test)
3. [Safety Data Sheets (SDSs) & GHS Chemical Labeling](#-safety-data-sheets-sdss--ghs-chemical-labeling)
   - [GHS Label Requirements & Warning Materials](#ghs-label-requirements--warning-materials)
   - [Relevant SDS Sections in Critical Facilities](#relevant-sds-sections-in-critical-facilities)
4. [Chemical Authorization & Contractor Oversight](#-chemical-authorization--contractor-oversight)
5. [Storage, Controls & Secondary Containment](#-storage-controls--secondary-containment)
   - [General Best Practices](#general-best-practices)
   - [The 10% / 100% Sizing Rule](#the-10--100-sizing-rule)
6. [Operational Chemical Risk Areas](#-operational-chemical-risk-areas)
   - [Cooling Systems & Water Treatment](#cooling-systems--water-treatment)
   - [Emergency Generator Fueling Protocols](#emergency-generator-fueling-protocols)
7. [Battery Safety & Management Systems](#-battery-safety--management-systems)
   - [Battery Chemistries Compared](#battery-chemistries-compared)
   - [Emergency Response & Eyewash Standards](#emergency-response--eyewash-standards)
8. [Safe Transfer, Spill Response & Disposal](#-safe-transfer-spill-response--disposal)
   - [Transfer Procedures & Prohibitions](#transfer-procedures--prohibitions)
   - [Emergency Spill Protocol](#emergency-spill-protocol)
   - [Disposal Standards](#disposal-standards)
9. [Pre-Assessment Answer Key & Detailed Explanations](#-pre-assessment-answer-key--detailed-explanations)
10. [Quick-Reference Summary](#-quick-reference-summary)

---

## 🎯 Module Overview & Objectives

Modern data centers rely on chemicals beyond routine janitorial products. Large-scale infrastructure requires bulk hydrocarbon fuels for backup generators, complex industrial chemical regimens for chilled water treatment, and high-density battery energy storage systems (BESS). Improper handling, storage, or disposal presents severe chemical burn, toxic vapor, arc flash, thermal runaway, fire, and regulatory compliance risks.

### Learning Objectives
- **Interpret** GHS chemical labels and identify relevant sections of a Safety Data Sheet (SDS).
- **Navigate** site approval workflows and contractor chemical disclosure mandates.
- **Calculate** secondary containment capacity using the standard 10%/100% rule.
- **Implement** protocols across specialized operational areas (cooling/water treatment loops, bulk diesel transfer, and battery charging rooms).
- **Execute** emergency spill, eyewash station access, and hazardous waste disposal procedures.

---

## 📝 Pre-Assessment Test

Evaluate your baseline knowledge before studying the technical documentation.

### 1. According to the standard "10% / 100% rule," what minimum capacity must a secondary containment system provide if storing four 55-gallon drums of water treatment chemicals?
- [ ] A) 5.5 gallons
- [ ] B) 22.0 gallons
- [ ] C) 55.0 gallons
- [ ] D) 220.0 gallons

### 2. Under industrial safety standards, an emergency eyewash station must be reachable within how much time from a battery charging/handling area?
- [ ] A) 10 seconds (roughly 55 feet / 17 meters)
- [ ] B) 30 seconds (roughly 150 feet / 45 meters)
- [ ] C) 60 seconds (roughly 300 feet / 90 meters)
- [ ] D) Within the same building quadrant

### 3. Which transfer method is strictly PROHIBITED when dispensing or moving flammable liquids inside a facility?
- [ ] A) Utilizing a closed piping distribution system
- [ ] B) Using compressed air or gas pressure to force liquid out of a tank or container
- [ ] C) Dispensing via gravity through an approved self-closing valve
- [ ] D) Drawing liquid through the top of the container using an approved pump

### 4. What type of fire extinguisher is specifically required in areas where Lithium-Ion batteries are stored and charged?
- [ ] A) Class A (Ordinary combustibles)
- [ ] B) Class B (Flammable liquids)
- [ ] C) Class C (Standard electrical only)
- [ ] D) Class D (Combustible metals / specialized fires)

### 5. Why must VRLA (Valve-Regulated Lead-Acid) and flooded wet cell battery rooms maintain active mechanical ventilation?
- [ ] A) To cool down server intake air
- [ ] B) To prevent the hazardous accumulation of flammable hydrogen gas released during charging
- [ ] C) To prevent humidity drops below 10%
- [ ] D) To disperse ozone created by data hall fans

*(Check your answers in the [Pre-Assessment Answer Key](#-pre-assessment-answer-key--detailed-explanations) section at the bottom).*

---

## 📄 Safety Data Sheets (SDSs) & GHS Chemical Labeling

### GHS Label Requirements & Warning Materials
All chemical containers entering or stored within a data center must feature clear, legible identification compliant with the **Globally Harmonized System (GHS)**:
- **Product Identifier:** Chemical name, code, or batch number.
- **Signal Words:** `DANGER` (severe hazards) or `WARNING` (less severe hazards).
- **Hazard Statements & Pictograms:** Standardized diamond-shaped graphic symbols depicting health, physical, and environmental hazards.
- **Precautionary Statements:** Mandatory PPE, safe storage conditions, and emergency response steps.
- **Secondary / Workplace Warnings:** When chemicals are transferred into secondary containers, the container must feature duplicate labeling, approved placards, process sheets, or batch tickets accessible throughout every shift.

### Relevant SDS Sections in Critical Facilities
While an SDS contains 16 standardized sections, data center operations prioritize the following:

| SDS Section | Designation | Operational Focus in Data Centers |
| :--- | :--- | :--- |
| **Section 1** | Substance Identification | Confirms trade name, CAS number, manufacturer emergency numbers, and authorized use. |
| **Section 2** | Hazard Identification | Details GHS classification, signal words, pictograms, and exposure hazards. |
| **Section 4** | First-Aid Measures | Specific flushing times, antidotes, and critical inhalation/dermal treatment protocols. |
| **Section 5** | Firefighting Measures | Suitable vs. unsuitable extinguishing media, thermal combustion hazards, and PPE for firefighters. |
| **Section 7** | Handling and Storage | Ventilation requirements, static bonding mandates, and chemical incompatibility constraints. |
| **Section 8** | Exposure Controls / PPE | Permissible Exposure Limits (PEL/TLV) and specific glove/goggle/respirator types. |
| **Section 11** | Toxicological Information | Acute toxicity, carcinogenic ratings, and target organ effects (short & long-term). |
| **Section 13** | Disposal Considerations | Waste classifications, neutralizer safety, and EPA/local regulatory constraints. |

> **Accessibility Mandate:** Employers must guarantee zero-barrier access to SDSs for all employees across all shifts. If maintained digitally, offline backups or uninterruptible power must ensure availability during network or power failures.

---

## 🔒 Chemical Authorization & Contractor Oversight

**Golden Rule:** *No chemical substance may cross the data center security perimeter without prior written approval from Site Leadership or Environmental Health and Safety (EHS).*

```
Contractor/Vendor Submits List
 (Product IDs, Volumes, SDSs)
            |
            v
EHS & Facilities Engineering Review
 (Risk Assessment, Incompatibilities, Code Limits)
            |
            +---> [DENIED] ---> Access/Substance Rejected at Gate
            |
            v
     [APPROVED]
            |
            v
Site Entry Permitted & Logged into Master Chemical Inventory
```

### Contractor & Vendor Submittal Requirements
Contractors must deliver a formal chemical disclosure packet well ahead of mobilization:
1. Complete list of chemical trade names and expected maximum on-site quantities.
2. Complete, current SDSs for every compound.
3. Compatibility matrix verifying that proposed compounds will not react with existing site systems (e.g., HVAC piping, halocarbon/clean-agent fire extinguishing lines).

---

## 📦 Storage, Controls & Secondary Containment

### General Best Practices
- **Inventory Reduction:** Maintain only the minimum necessary quantity required for routine maintenance ("just-in-time" staging).
- **Segregation of Incompatibles:** Physically separate oxidizers from flammable liquids, and strong acids from strong bases to eliminate exothermic or toxic reactions.
- **Spill Pallet Integrity:** Inspect containment basins weekly for debris, cracks, or accumulated water.

### The 10% / 100% Sizing Rule
Secondary containment systems (spill pallets, berms, bunded slabs) must be engineered to hold whichever volume is larger:

$$\text{Required Containment Capacity} = \max\left(0.10 \times V_{\text{total}}, \; 1.00 \times V_{\text{largest}}\right)$$

#### Sizing Scenarios

```
Scenario A: Fifteen (15) 55-Gallon Drums
- Total Volume: 15 * 55 = 825 gallons
- 10% of Total: 0.10 * 825 = 82.5 gallons
- 100% of Largest Unit: 1 * 55 = 55.0 gallons
==> Required Secondary Capacity: 82.5 gallons (10% rule governs)

Scenario B: Three (3) 55-Gallon Drums
- Total Volume: 3 * 55 = 165 gallons
- 10% of Total: 0.10 * 165 = 16.5 gallons
- 100% of Largest Unit: 1 * 55 = 55.0 gallons
==> Required Secondary Capacity: 55.0 gallons (100% rule governs)
```

---

## ⚙️ Operational Chemical Risk Areas

### Cooling Systems & Water Treatment
- **Chemical Classes:** Glycol-based heat-transfer solutions, biocides, corrosion inhibitors, scale dispersants, and acid neutralizers.
- **Engineering Controls:** Double-walled storage tanks, automated chemical feed pumps, closed loop injection ports, dedicated room ventilation, and containment dikes.
- **Handling Precautions:** Automated dosing pumps cycle on demand based on continuous conductivity/pH sensors. Never perform maintenance without zero-energy electrical isolation and chemical line depressurization.
- **Static Grounding:** Ground and bond metal containers when transferring volatile or flammable formulations to prevent static-induced deflagration.

### Emergency Generator Fueling Protocols
Enterprise data centers house tens of thousands of gallons of Ultra-Low Sulfur Diesel (ULSD).

```
PRE-FUELING                     FUEL DELIVERY                    POST-FUELING
• Inspect tank valves & seals   • Approved rated transfer gear   • Re-seal all tank caps & ports
• Eliminate ignition sources    • Stage SPCC spill kit nearby    • Inspect bunds for drips
• Verify diesel specification   • Slow fill; avoid surge shocks  • Log transfer volume in
• Check weather conditions      • Confirm driver stays at nozzle   EHS compliance manifest
```

- **Spill Prevention, Control, and Countermeasure (SPCC):** Any diesel transfer operation must align with the site SPCC plan. In the event of an active spill, halt pumping immediately, trip emergency shutoffs, drop absorbent booms, and notify critical operations management.

---

## 🔋 Battery Safety & Management Systems

Data centers utilize high-density battery energy storage to supply continuous DC voltage to Uninterruptible Power Supply (UPS) inverters during utility interruptions.

### Battery Chemistries Compared

| Battery Type | Primary Applications | Key Inherent Hazards | Mandatory Safety Controls |
| :--- | :--- | :--- | :--- |
| **VRLA (Valve-Regulated Lead-Acid)** | UPS strings, Gen-set starters | Overcharging off-gassing (Hydrogen $H_2$), thermal runaway, sulfuric acid | Active hydrogen detection sensors, exhaust ventilation, room temperature moderation ($20\text{--}25^\circ\text{C}$). |
| **Flooded Wet Cell** | Legacy high-capacity UPS, PITs/Forklifts | Liquid sulfuric acid splash, explosive $H_2$ generation, terminal corrosion | Mandatory acid apron, face shield, and chemical boots during maintenance; nearby neutralizing spill kit. |
| **Ni-Cd (Nickel-Cadmium)** | Emergency egress lighting, switchgear control | Heavy metal cadmium toxicity, potassium hydroxide ($KOH$) alkaline burns | Non-metallic insulated tools to avoid dead shorts; specialized toxic metal recycling manifests. |
| **Li-Ion (Lithium-Ion)** | High-density modular UPS, tools | Thermal runaway propagation, toxic solvent off-gassing, self-sustaining fires | Continuous Battery Management System (BMS) monitoring, rack-level deflagration exhaust, Class D extinguishing agents. |

### Emergency Response & Eyewash Standards

```
+--------------------------------------------------------------------------+
|                     EMERGENCY EYEWASH STATION (EWS)                      |
|                                                                          |
| • Travel Time: Maximum 10 seconds from battery handling areas            |
| • Distance: Approximately 55 feet (17 meters) unobstructed               |
| • Lithium-Ion Specification: 15-minute continuous-flow plumbed/portable  |
| • Activation: Single-action pull/push valve; stays open hands-free       |
+--------------------------------------------------------------------------+
```

#### Specialized Acid Spill Kit Contents
Every lead-acid battery bank requires a dedicated, tamper-tagged response kit containing:
- **PPE:** Heavy neoprene/nitrile acid-resistant gloves, full-face shield, and chemical-resistant coveralls.
- **Neutralizers:** Sodium bicarbonate or commercial acid neutralizers with built-in colorimetric pH indicators (turns color when safe).
- **Absorbents:** Acid-inert synthetic pads, pillows, and non-sparking, chemical-resistant cleanup tools.

---

## 🛢️ Safe Transfer, Spill Response & Disposal

### Transfer Procedures & Prohibitions

```
APPROVED TRANSFER METHODS                    PROHIBITED METHODS
• Closed-loop hard piping                    ❌ NEVER pressurize containers with
• Approved FM/UL-listed safety cans             compressed gas/air to discharge liquids
• Hand/rotary top-draw suction pumps         ❌ NEVER dispense ungrounded near
• Gravity feed via self-closing brass tap       flammable vapor clouds
```

### Emergency Spill Protocol

```
1. DISCOVER & CALL ➔ 2. EVACUATE & ISOLATE ➔ 3. CONTAIN ➔ 4. NOTIFY & LOG
Alert nearby staff;    Cordon boundary;         Deploy rated     Report up chain
notify supervisor      reroute pedestrian       absorbents if    to EHS / Facilities
and EHS immediately.   and PIT traffic.         trained & safe.  per SPCC plan.
```

- **Tamper Tags:** Spill kits must feature breakaway plastic tamper seals. If a seal is broken, the critical operations team must immediately inspect, replenish, and re-tag the kit.

### Disposal Standards
- **Rags and Wipes:** Fuel- or solvent-soaked rags must be stored in self-closing, heavy-gauge, fire-resistant safety cans to prevent spontaneous combustion.
- **Battery Recycling:** Lead-acid, Ni-Cd, and Lithium-ion batteries must never enter regular municipal waste streams. They require chain-of-custody documentation and transfer to licensed hazardous waste and e-waste recycling handlers.

---

## 💡 Pre-Assessment Answer Key & Detailed Explanations

1. **C (55.0 gallons)**  
   *Calculation:* Total volume $= 4 \times 55 = 220\text{ gallons}$. $10\%$ of total volume is $22\text{ gallons}$. However, $100\%$ of the largest single container is $55\text{ gallons}$. Because the rule mandates the *greater* of the two, the system must hold at least $55\text{ gallons}$.
2. **A (10 seconds / ~55 feet)**  
   ANSI/ISEA Z358.1 and occupational safety standards require that emergency eyewash units be located within a 10-second travel time (approximately 55 feet or 17 meters) on an unobstructed path from corrosive chemical/acid risks.
3. **B (Using pressure to move flammable liquids)**  
   Pressurizing a standard liquid drum or tank with compressed air or gas can cause catastrophic overpressure rupture, massive liquid spray, and electrostatic ignition of aerosolized flammable mists.
4. **D (Class D)**  
   Lithium-metal fires and severe high-energy lithium-ion battery failure events involving combustible materials and thermal events require specialized Class D dry powder extinguishing agents or tailored site suppression procedures.
5. **B (Prevent hydrogen accumulation)**  
   During charging—particularly overcharging—aqueous lead-acid batteries electrolyze water into oxygen and flammable hydrogen gas ($H_2$). Without active ventilation, hydrogen can exceed its lower explosive limit (LEL of $4\%$) in air, creating severe explosion risks from any electrical spark.

---

## 📌 Quick-Reference Summary

- **Labeling Standard:** All vessels must possess GHS markings; SDS access must be instant and unhindered.
- **The Golden Rule:** No chemical enters without prior EHS/leadership authorization and SDS verification.
- **Containment Rule:** Sizing must hold $\ge 10\%$ of total volume or $\ge 100\%$ of the largest vessel.
- **Distance Rule:** Eyewash stations must be reachable within 10 seconds ($\approx 55\text{ feet}$).
- **Safety Directive:** Never pressurize chemical drums to empty them; maintain bonding/grounding cables for flammable fluids.
