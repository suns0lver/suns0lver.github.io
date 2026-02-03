# EBOPFS · Project0001.A  
## SP-005 — Climate, Airflow & CO₂ Control

### R&D Framing (Non-Negotiable)
SP-005 exists to benchmark and validate best-in-class environmental control systems for dense vertical growing environments, with an emphasis on:
- Uniform airflow at canopy level
- Humidity control without condensation
- Temperature stability without stratification
- CO₂ enrichment that is measurable and safe

This SP is about preventing invisible failure (mold, stress, uneven growth).

---

## Phase 0 — Environmental Requirements Definition  
*(Before ducts or fans)*

### Modeling & Analysis
- Crop-specific temperature and humidity targets
- Vapor pressure deficit (VPD) modeling by growth stage
- Heat load modeling (lighting + plant metabolism)
- Air exchange requirements per rack zone

**~$3k – $15k**

**R&D Value:**  
Defines environmental truth before hardware selection.

---

## Phase 1 — Air Movement & Distribution (The Spine)

### Airflow Hardware
- Variable-speed EC fans (industrial / horticultural grade)  
  ~$300 – $2,000 per unit
- Inline duct fans (sealed, low-noise)  
  ~$200 – $1,500 per unit
- Laminar airflow diffusers  
  ~$100 – $800 per zone

### Ducting & Distribution
- Food-safe ducting (rigid + flexible)
- Adjustable diffusers per rack tier
- Backdraft dampers

**~$2k – $15k per rack zone**

**R&D Value:**  
Ensures no dead zones, no stagnant layers, no mold havens.

---

## Phase 2 — Temperature Control

### Heating & Cooling
- High-efficiency heat pumps  
  ~$5k – $25k per unit
- Radiant heating elements (bench / zone-level)  
  ~$1k – $10k
- Chilled water or DX cooling interfaces (evaluation)  
  ~$3k – $20k

**Design Principle:**  
Temperature must be uniform across height, not just averaged.

**R&D Value:**  
Prevents vertical stratification that silently kills yield.

---

## Phase 3 — Humidity & Moisture Management

### Dehumidification
- Commercial desiccant or refrigerant dehumidifiers  
  ~$3k – $20k per unit
- Condensate recovery systems

### Humidification (Controlled)
- Ultrasonic or high-pressure fogging systems  
  ~$1k – $8k

### Targets
- Relative humidity: 50–70%
- VPD maintained within crop-specific bands

**R&D Value:**  
Balances transpiration without inviting pathogens.

---

## Phase 4 — CO₂ Enrichment & Monitoring

### CO₂ Delivery
- Food-grade CO₂ tanks or generation system  
  ~$2k – $15k
- Precision regulators and solenoid valves  
  ~$300 – $2k
- Zoned injection manifolds

### Monitoring
- NDIR CO₂ sensors (research-grade)  
  ~$200 – $1,500 per node
- Safety shutoff interlocks
- Alarm and ventilation override

### Target Range
- 800–1,200 ppm (crop-dependent)

**R&D Value:**  
Enables yield gains without safety blind spots.

---

## Phase 5 — Sensing, Verification & Mapping

### Environmental Sensors
- Temperature sensors (multi-height arrays)
- RH sensors (condensation-resistant)
- Airflow velocity sensors
- Differential pressure sensors

**~$1k – $10k per rack zone**

### Diagnostic Tools
- Smoke / tracer visualization tools  
  ~$200 – $1k
- Thermal cameras (shared with SP-003)  
  ~$1k – $10k

**R&D Value:**  
Makes the invisible visible.

---

## Phase 6 — Filtration & Biosecurity (Air Side)

### Filtration
- HEPA or MERV-rated filters
- Activated carbon (odor & VOC control)
- Filter pressure monitoring

**~$1k – $8k per air loop**

**R&D Value:**  
Prevents airborne contamination and cross-zone spread.

---

## Phase X — Reference Only  
### Instant Full-Scale Build-Out @ Current Market Prices (Non-Binding)

> This phase represents a hypothetical, immediate full-scale environmental control deployment using current market pricing.  
> It is not part of Phases 0–6 and does not represent planned expenditure.  
> Included to anchor realism and support future ARGENT-based reinvestment modeling.

### Assumptions
- ~20 floors
- ~20,000 trays per floor (~400,000 trays)
- Dense microgreens canopy
- Tight VPD and temperature tolerances
- CO₂ enrichment across all grow zones
- Redundancy prioritized over minimum cost

---

### Order-of-Magnitude Cost Reference

#### Airflow & Distribution Infrastructure
- Fans, ducting, diffusers, dampers, zone isolation

➡️ **~$30M – $80M**

---

#### Heating & Cooling Capacity
- Heat pumps, radiant systems, chilled water / DX interfaces
- Cold-climate oversizing and redundancy

➡️ **~$40M – $100M**

---

#### Humidity Control (Dehumidification + Humidification)
- Industrial dehumidifiers
- Fogging / humidification systems
- Condensate handling

➡️ **~$20M – $60M**

---

#### CO₂ Delivery & Safety Systems
- Storage / generation
- Distribution manifolds
- Sensors, alarms, interlocks

➡️ **~$10M – $30M**

---

#### Sensors, Mapping & Biosecurity
- Environmental sensors
- Filtration systems
- Diagnostic and verification tooling
- Spares and redundancy

➡️ **~$10M – $25M**

---

### Reference Total (SP-005 Only)
> **~$110M – $295M+ USD**

This excludes:
- Structural tower
- Grow racks & trays (SP-002)
- Lighting (SP-003)
- Irrigation & nutrients (SP-004)
- Robotics (SP-006)
- Control software & AI (SP-007)
- Labor, land, permits

---

## Contribution Modes (Explicit)
- HVAC engineering expertise
- Equipment evaluation units
- Environmental modeling support
- Industrial airflow design input
- Funding earmarked SP-005 only

---

## Explicitly Out of Scope
- Lighting (SP-003)
- Irrigation & nutrients (SP-004)
- Robotics (SP-006)
- Control software & AI (SP-007)

Interfaces only — no scope bleed.

---

## Status
**Current:** Environmental architecture definition  
**Next Gate:**  
✔ Uniform airflow validated  
✔ VPD stability demonstrated  
✔ CO₂ delivery proven safe and measurable

---

### Why SP-005 Is Make-or-Break
If air lies:
- mold wins
- plants stress
- sensors mislead
- automation learns the wrong lesson

SP-005 ensures the atmosphere tells the truth.
