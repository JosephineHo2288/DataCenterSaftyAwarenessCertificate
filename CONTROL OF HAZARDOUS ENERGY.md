**Module Check-Out Assessment**

**Scenario Question:**
A data center operations technician is preparing to replace a failed primary fan motor inside a computer room air handling unit (CRAHU). The unit is powered from a dedicated 480V distribution panel, controlled automatically by the Building Management System (BMS), and connected to a pressurized chilled water supply.

Which of the following actions is **required** to establish a zero-energy state before physical maintenance begins?

* **A)** Stop the CRAHU through the BMS interface and place a software override on the fan start command.
* **B)** Open the local disconnect switch, rely on BMS telemetry to verify zero voltage, and affix a single department lock.
* **C)** Isolate the electrical disconnect, depressurize/lock out relevant fluid/thermal lines, verify absence of voltage using the Live-Dead-Live method, and have each technician apply their individual lock.
* **D)** Place a single Lockout/Tagout tag on the main breaker without a physical lock, provided the maintenance task takes less than 30 minutes.

**Correct Answer: C**

* **Explanation:** Safe LOTO requires isolating all sources of energy (electrical, mechanical, pneumatic/hydraulic/thermal), physically applying individual locks for every worker involved, and verifying absence of voltage with a verified tester (Live-Dead-Live method). Software stops (BMS) or pushbuttons are never primary isolating devices, and tags alone cannot replace locks when locking mechanisms are available.

---

**GitHub Repository Blueprint**

```text
hazardous-energy-control-dc/
├── README.md
├── LICENSE
├── docs/
│   ├── 01-hazardous-energy-types.md
│   ├── 02-loto-procedures-simple-vs-complex.md
│   ├── 03-verification-live-dead-live.md
│   └── 04-equipment-guarding-standards.md
├── templates/
│   ├── complex-loto-plan-template.md
│   ├── hazard-observation-report.md
│   └── return-to-service-checklist.md
└── assessments/
    └── loto-knowledge-check.json

```

**`README.md` Template**

```markdown
# Data Center Hazardous Energy Control (LOTO & Guarding)

An operational training guide and procedure repository for controlling hazardous energy (electrical, mechanical, thermal, pneumatic, hydraulic, and chemical) in mission-critical data center environments.

## Core Topics Covered
- **Types of Hazardous Energy:** Identification of electrical, thermal, chemical (diesel/water treatment), mechanical, and stored potential energy.
- **Lockout/Tagout (LOTO) Procedures:**
  - **Simple LOTO:** Single-source/circuit part isolation, direct authorized installer responsibility.
  - **Complex LOTO:** Multi-energy, multi-crew, multi-shift coordination, group lockboxes, and written plans.
- **Absence of Voltage Verification:** Standards for Live-Dead-Live (LDL) testing and rated Absence of Voltage Testers (AVTs).
- **Physical Equipment Guarding:** Safeguards for AHUs, cooling towers, generators, and rotating equipment.

## Standard Workflow
1. **Briefing & Hazard Identification:** Review single-lines; identify all electrical and stored energy sources.
2. **Isolation & De-energization:** Open manual disconnects, breakers, and line valves (never pushbuttons or BMS controls alone).
3. **Device Application:** Install individualized keyed locks and single-use 50 lb-rated danger tags.
4. **Zero-Energy Verification:** Perform Live-Dead-Live testing on electrical sources; bleed stored pressure.
5. **Post-Maintenance Return:** Clear tools, reinstall guards, verify worker clearance, and ensure lock removal by original installers.

## Contributing & Site Procedures
All site-specific deviations or complex LOTO work plans must be submitted via pull request using the templates in `/templates`.

```
