# Truck Electrification Network — Technical Brief v1
**Status:** SPEC · Soft-PASS · Not live · DFW Node dark  
**Owner narrative:** Chris Olsen · Advisors: Strip Electrical · Yard Software · Power Pod · Helios  
**Pitch:** https://skiiwa67-collab.github.io/yard-energy-console/  
**Repo:** https://github.com/skiiwa67-collab/yard-energy-console  
**Date:** 2026-09-19

---

## 1. One-sentence vision
Turn an LTL dock into a bidirectional energy node: trailers charge (and backfeed) through the landing gear while spotted, hybrid axle-2 kits cut city fuel burn, and a later city mesh shares surplus across yards — without waiting on a Megacharger fleet swap.

## 2. Product in two layers

| Layer | What it does | Gen 1 |
|-------|----------------|-------|
| **YARD** | Move watts between building bank ↔ pad ↔ trailer modules ↔ Power Pod / BEV | **Ship target** |
| **CITY** | ARL ↔ Dallas ↔ GRP ↔ Lone Star: EXPORT / CHARGE / ISLAND | **Parked** until real interconnect |

Gen 1 does **not** need a utility signature to light one bay.

## 3. Architecture (power path)

```
Roof / skin PV
      ↓
Building powerpacks (under slab)     ←→  site DC bus (HV class, orange)
      ↓
Flush landing-gear PAD (cassette run at GEAR LINE)
      ↓  weight closes mechanical switch
Gear shoe → jumper UP INSIDE landing-gear tubes
      ↓
Trailer junction → snap-in battery modules
      ↓
Power Pods (axle 2)  and/or  BEV tractor pack
```

- Bidirectional equalize — **not** a charger gun on the cab.  
- Skin PV can still feed modules when the pad is idle.  
- Steel landing leg is **not** the bus.  
- Road regen is a **separate** path into the same modules (do not draw lightning at the wheels as “the pad”).

## 4. Gen 1 pad (Strip Electrical)

| Rule | Spec |
|------|------|
| Form | Flush modular **snap-out cassettes** in a recessed pan |
| Housing | Recycled-tire crumb (chew face; **not** the conductor) |
| Alignment | Full door-run at the **gear line** (Chris green/red band on bays 66–60 photo) — not threshold, not skinny bar |
| Switch | **Weight** → mechanical plunger/rocker (Gen 1). Squish-to-conduct / hybrid = later gens |
| Safety | Both shoes closed or **no watts**. Seam = dead rubber |
| Isolation | One WORN/FAULT bay does **not** kill neighbors / ~201 doors |
| Laterals | Fatter pipe from band → dock wall at ampacity intervals (not door count) |
| First article | **One** cassette + **one** lateral + **one** bay (trailer on 62). Prove drain/slope, wet wipe, either-way lateral |

**Lamps (own loop, not HV):** CONDUCTING green · IDLE dim · WORN amber · FAULT red. Ice = weather. Island = yard **mode**, not a pad lamp.

**Voltage class:** inherited from published powerpack / Megapack analogs (site AC 480 V is **not** the pad). Pad amps Soft-FAIL invent — Soft-PASS closest building analog ~66 A class, **not** Megacharger 1100 A.

## 5. Power Pod (hybrid axle-2)

| Lock | Detail |
|------|--------|
| Axle 1 | Diesel remains one rear drive axle |
| Axle 2 | Two Tesla-**class** compact drive units (one per wheel) = the Power Pods |
| Mount | Snap-on, bolted, liquid cool, orange HV |
| Energy | Snap-in **trailer** modules (+ short hitch hop). Not a wall plug on the cab |
| Fleet stamps | BEV SEMI · DIESEL DOUBLES · DIESEL+POD (only DIESEL+POD takes pods) |
| Gen 1 charge money | Charge the **dropped** trailer on the pad (never crosses fifth wheel) |
| Gen 1 hitch | Manual HV hop + **HVIL** (open = pods offline). Auto-mate = Gen 2 |

**Software half:** per-wheel torque/slip (ice/wet/light trailer); electric torque ms; log slip/torque for a future insurance path — Soft-FAIL any %.

**MPG:** Soft-FAIL kit number. Closest Soft-PASS analog: NREL Coca-Cola Eaton hybrid **+13.7%** in-service; city EST higher; highway near flat. DFW P&D/shuttle **180–280 mi** = city case.

## 6. Yard router (Yard Software)

- Object of dispatch = **CONDUCTING cassette ID**, not door number.  
- Doors = layout only. Weight = switch.  
- HUD chips locked Soft-PASS: **201 doors EST** (Loop 820) · **22.0 MWh EST** · SOC = dash until measured (no fake %).  
- Comms: cell first; sat hop when cell dies. **Not** radios / 911 (other project).

## 7. City mesh (parked)

Four-yard DFW prototype: **ARL ↔ Dallas ↔ GRP ↔ Lone Star**.  
Verbs: EXPORT · CHARGE · ISLAND.  
Soft-FAIL: MW number, signed interconnect, ERCOT takeover claims. Show as plate until real paperwork.

## 8. Who pays / incentives (frame only)

| Public | Private |
|--------|---------|
| Warehouse electrify + truck electrify + hybrid-axle write-off path | Freight customers keep moving freight |

Soft-FAIL: specific $ / appropriation numbers. Do not invent.

## 9. First-check sequence (do not skip)

1. Show HUD  
2. One believer  
3. One node — Loop 820 (~201 doors)  
4. Film  

Do **not** hire OEM/legal before step 3.

## 10. Open Soft-FAIL (tape / measure before inventing)

Wall-to-band offset · L/R foot spacing · round shoe diameter · contact patch + fault current before pad V/A · flush-pan drain/slope · 53-ft vs 28-ft pup offset · module kWh / pod kW · hitch pinout · live SOC log · Steve cassette-ID code status since Aug.

---

*Presentation Soft-PASS. Sources: Strip / Yard / Power Pod Soft-PASS dumps + box project specs. Helios + Tinkabot cleanup 2026-09-19.*
