## 🧾 RV Electrical Upgrade – Phase 1 Plan (Markdown Summary)

---

## 🧠 Overview

This project upgrades the RV’s charging systems to support **future LiFePO4 batteries** while remaining compatible with the current lead-acid setup.

**Stock (as verified on coach):** house and chassis are tied by a **simple relay with a time delay** only (no microprocessor isolator). Phase 1 removes that **direct parallel** path in favor of regulated DC-DC charging.

Key goals:
- Replace the isolator **relay** path with **DC-DC charging**
- Add **lithium-compatible shore charging**
- Install proper **wiring and circuit protection**
- Enable **drop-in lithium upgrade later with no rewiring**

---

## 🔋 System Architecture

### Alternator Charging
- Victron Orion XS DC-DC battery charger (Orion XS 1400 family: **up to 50A** input/output per manual — do not plan above 50A)
- Mounted under passenger seat (cool, ventilated area)
- Configured for up to **~50A** output (within alternator and thermal limits)
- Using **engine shutdown detection** in VictronConnect by default (no separate ignition wire initially unless testing shows you need one)

---

### Shore Power Charging
- Progressive Dynamics PD4655V Converter Charger
- Lithium-compatible mode (switchable)
- Direct replacement for existing converter

---

## 🔌 Wiring & Protection

### Cable
- 4 AWG copper cable (positive and negative)

### Terminations
- Tinned copper lugs (Selterm)
- Adhesive heat shrink
- Hydraulic hex crimp

---

### Circuit Protection

Using Blue Sea Systems MIDI fuse blocks:

| Location | Fuse Size | Purpose |
|----------|----------|--------|
| Chassis battery → Orion input | **100A MIDI fuse** | Protects input cable |
| Orion output → House battery | **80A MIDI fuse** | Protects output cable |

📍 **Placement:**  
Install each fuse within **6–12 inches of the battery positive terminal**

---

## 🔌 Wiring Diagram

    [Chassis Battery +]
            |
        (100A Fuse)
            |
          4 AWG
            |
       [Victron Orion XS 50A]
            |
          4 AWG
            |
        (80A Fuse)
            |
    [House Battery +]


    Negatives:
    [Chassis Battery -] -----------.
                                   \
                                    ---> [Common Chassis Ground]
                                   /
    [House Battery -] -------------'

---

## 🔧 Installation Decisions

- Old battery isolator/relay system **removed**
- Shared **chassis ground retained** (verified clean + solid)
- Charger mounted **inside conditioned space** (better thermal performance)
- Batteries remain in **under-step compartment**

---

## 🔋 Future Phase (Lithium Upgrade)

When installing LiFePO4 batteries:

- Set:
  - Victron charger → **Lithium profile**
  - PD converter → **Lithium mode**
- No wiring changes required

---

# ✅ Pre-Install Checklist

## 🔍 Planning
- [ ] Measure and confirm all cable lengths
- [ ] Verify mounting locations (charger + fuse blocks)
- [ ] Ensure airflow clearance around charger (2–4” minimum)

---

## 🔌 Electrical Components
- [ ] 4 AWG cable (sufficient length)
- [ ] Tinned copper lugs sized correctly
- [ ] Adhesive heat shrink
- [ ] 100A + 80A MIDI fuses
- [ ] MIDI fuse blocks securely mounted

---

## 🛠 Tools
- [ ] Hydraulic crimper (hex dies)
- [ ] Heat gun
- [ ] Torque wrench (recommended)
- [ ] Multimeter
- [ ] Wire cutters/strippers

---

## 🔧 Grounding
- [ ] Inspect chassis ground points:
  - Clean metal contact
  - No corrosion
  - Tight fasteners

---

## ⚠️ Safety
- [ ] Disconnect all batteries before starting
- [ ] Remove negative terminals first
- [ ] Protect cables from sharp edges (grommets/loom)

---

# ⚡ First Power-Up Procedure

## 1. 🔌 Final Inspection
- [ ] Verify all connections are tight
- [ ] Confirm polarity (no reversed wires)
- [ ] Check fuse installation
- [ ] Ensure no exposed conductors

---

## 2. 🔋 Reconnect Batteries
1. Connect **house battery**
2. Connect **chassis battery**
3. Install fuses last

---

## 3. 📱 Configure Charger

Using Victron app:

- Set battery type:
  - **Lead-acid (Phase 1)**  
- Set charge current:
  - Start at **50A**
- Enable engine detection (default)

---

## 4. 🚐 Engine Test

- Start engine
- Observe:
  - Charger turns on after short delay
  - Charging current ramps up smoothly

---

## 5. 📊 Verify Operation

Using app or multimeter:

- [ ] Input voltage (alternator side) ~13.5–14.5V
- [ ] Output voltage appropriate for battery type
- [ ] Current stable (not oscillating)
- [ ] No excessive heat in:
  - Wiring
  - Lugs
  - Charger

---

## 6. 🔥 Thermal Check (important)

After ~15–20 minutes:

- Touch-check (carefully):
  - Cables → warm is OK, hot is not  
  - Lugs → should remain cool  
- Charger:
  - Warm is normal  
  - Should not be excessively hot or throttling  

---

## 7. 🧪 Road Test

- Drive for 30–60 minutes
- Confirm:
  - Stable charging behavior  
  - No fuse trips  
  - No unexpected shutdowns  

---

# 🧠 Final Notes

- Up to **~50A** charge rate (Orion XS limit) is:
  - Tunable for alternator protection via input current limit  
  - Compatible with future LiFePO4 when configured  
  - Within 4 AWG capacity for typical run lengths (verify fuse table vs. your lengths)  

- Auto engine detection should work well:
  - Add ignition trigger later only if needed  

---

# 🧾 Bottom Line

This is now a:

✅ Safe  
✅ Efficient  
✅ Lithium-ready  
✅ Professionally structured system  

You’ve effectively built a **“install once, upgrade later” electrical foundation**.