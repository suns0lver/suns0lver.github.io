# EBOPFS · Project0001.A  
## Closed Growing Environment — Microgreens Tower

### Parent Project Role
Design and construct a fully automated, closed-loop vertical farming environment capable of continuous, high-density microgreens production with minimal external inputs.  
This project prioritizes food security, repeatability, and operational resilience.

---

## Project Decomposition (Canonical)

Each subproject below is independently contributable, reviewable, and fundable.

---

## SP-001 — Structural & Spatial Architecture

### Scope
- Tower geometry (cylindrical / polygonal)
- Floor-to-floor height and load planning
- Central core design (elevators, utilities)
- Rack density and aisle spacing

### Baseline Parameters
- 20 floors × ~4 m floor-to-floor height
- Central core ~10 m diameter
- Concentric grow zones with robotic aisles

### Outputs
- Floor plans
- Structural load assumptions
- Material selection constraints

---

## SP-002 — Grow Rack & Tray System

### Scope
- Multi-tier rack design (5 levels per floor)
- Tray sizing and layout optimization
- Substrate compatibility (coir, hemp mats)
- Cleaning and sanitation cycle constraints

### Key Metrics
- ~20,200 trays per floor
- Tray size: 1.2 m × 0.6 m
- Airflow and robotic access preserved

### Failure Modes
- Poor airflow → mold
- Vibration affecting trays
- Maintenance access bottlenecks

---

## SP-003 — Lighting Systems & Spectral Control

### Scope
- Full-spectrum LED arrays
- Tier- and crop-specific spectra
- Photoperiod scheduling
- Per-tier spectral addressability for fine-grain control

### Parameters
- 200–400 µmol/m²/s PAR
- Red / blue / green / UV-A mixes per crop class

### Collaboration Surface
- Lighting engineers
- Plant physiologists
- Control software contributors

---

## SP-004 — Irrigation & Nutrient Delivery

### Scope
- NFT, DWC, and drip systems by crop category
- Closed-loop water recycling
- pH and EC monitoring

### Defined Ranges
- EC: ~1.2–2.5 mS/cm
- pH: ~5.5–6.5 depending on crop

### Failure Modes
- Biofilm buildup
- Pump redundancy gaps
- Nutrient drift

---

## SP-005 — Climate, Airflow & CO₂ Control

### Scope
- Tier-specific temperature and humidity control
- CO₂ enrichment
- Mold prevention via airflow management

### Targets
- Temperature: 18–24 °C
- Humidity: 50–70%
- CO₂: 1,000–1,200 ppm

---

## SP-006 — Robotics & Automation Hardware

### Scope
- Robotic arms for planting and harvesting
- Conveyors, AGVs, and pneumatic delivery systems
- Safety interlocks and fault detection

### Derived Workflows
- Tray preparation
- Seeding
- Harvest
- Internal transport

---

## SP-007 — Monitoring, AI & Control Systems

### Scope
- Sensor fusion (light, temperature, humidity, pH, EC)
- Vision-based crop health diagnostics
- Central decision engine

### Key Principle
Automation must be observable and overrideable, not opaque.

- Manual override modes (local, remote, fail-safe)

---

## SP-008 — Processing, Packaging & Traceability

### Scope
- Rinsing and drying systems
- Portioning
- Eco-friendly packaging
- QR-based batch traceability

### Integration
- Conveyor-linked from harvest zones
- Direct feed to storage and delivery systems

---

## SP-009 — Energy & Water Integration

### Scope
- On-site solar generation with storage
- Rainwater harvesting
- Load balancing across systems

### Non-Goal
Grid independence on day one — resilience first, autonomy later.

---

## SP-010 — Logistics & Output Flow

### Scope
- Internal transport (pneumatic and conveyor systems)
- Cold storage
- Delivery batching and staging

### Metric
Time from cut to storage minimized without quality loss.
