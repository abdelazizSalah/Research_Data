# Industrial Control Systems (ICS) Honeypot Research Collection

This repository documents and organizes an extensive literature review on **Industrial Control Systems (ICS) honeypots**, carried out as part of my **HiWi (Student Research Assistant) work at BTU.  
It reflects a sustained and in-depth study of academic and applied research on ICS deception technologies, with a strong focus on realism, attacker interaction, and data generation for security research.

---

## What are Industrial Control Systems (ICS)?

**Industrial Control Systems (ICS)** are specialized computing and networking systems used to monitor and control physical industrial processes. They are a core part of **Operational Technology (OT)** environments and are commonly found in:

- Power grids  
- Water distribution and treatment plants  
- Manufacturing and industrial automation  
- Oil and gas pipelines  
- Transportation systems  

Typical ICS components include **Programmable Logic Controllers (PLCs)**, **Remote Terminal Units (RTUs)**, **sensors**, **actuators**, and **SCADA (Supervisory Control and Data Acquisition)** systems.  
Unlike traditional IT systems, ICS environments are **deterministic, timing-sensitive, safety-critical**, and tightly coupled with physical processes.

---

## What are Honeypots?

A **honeypot** is a deliberately deployed decoy system designed to attract, detect, observe, and analyze malicious activity.  
In the context of ICS, honeypots emulate industrial devices, protocols, or even physical processes to interact with attackers in a controlled and observable manner.

ICS honeypots can be broadly classified into:
- **Low-interaction honeypots** (protocol emulation, limited behavior)
- **Medium-interaction honeypots** (partial logic and state handling)
- **High-interaction honeypots** (realistic PLC logic, timing, and process feedback)

---

## Why are ICS Honeypots Important?

ICS honeypots are critical because:

- Real ICS environments **cannot be safely experimented on**
- Attacks on ICS can cause **physical damage, safety risks, and service outages**
- Real-world ICS attack data is **scarce and difficult to share**
- Traditional IT honeypots fail to capture **process-aware attacker behavior**

ICS honeypots enable:
- Safe observation of real attacker techniques
- Generation of realistic datasets for IDS/ML research
- Evaluation of protocol abuse, timing attacks, and MITM scenarios
- Study of attacker decision-making in cyber-physical systems

---

## Scope of This Repository

This repository serves as a **research log and reference collection** of papers related to ICS honeypots, covering:

- Honeypot architectures (low, medium, high interaction)
- Industrial protocol emulation (Modbus/TCP, S7, DNP3, etc.)
- Scan-cycle awareness and timing realism
- Network-only vs. process-aware deception
- Dataset generation for intrusion detection
- Attacker interaction depth and behavioral realism
- Limitations of classical honeypots and emerging approaches

---

## Covered Honeypot Systems & Approaches

The papers in this repository include (but are not limited to) the following influential ICS honeypot methods:

- **Antonioli et al. (MiniCPS-based approaches)**  
  Scan-cycle-aware and CPS-accurate emulation frameworks enabling realistic PLC logic, timing behavior, and attacker feedback. These works form the foundation of many modern high-interaction ICS honeypots.

- **Honeyd (ICS adaptations)**  
  Early low-interaction honeypot concepts adapted to industrial protocols, mainly useful for exposure measurement and reconnaissance detection.

- **HoneyPLC**  
  PLC-focused honeypots emulating control logic and register behavior, bridging the gap between protocol emulation and process awareness.

- **ICSPot**  
  A protocol-level industrial honeypot widely used for Internet-scale attack measurement against ICS services.

- **LLMPot (ongoing work)**  
  A novel research direction exploring **LLM-driven adaptive ICS honeypots**, aiming to model attacker interaction sequences, generate realistic protocol dialogues, and move beyond static rule-based emulation.

---

## Purpose

This repository is intended to:

- Demonstrate **extensive reading and understanding** of ICS honeypot research
- Act as a **reference base** for future work in ICS security and deception
- Support ongoing research activities during my **HiWi position at BTU**
- Serve as groundwork for advanced topics such as:
  - ICS intrusion detection
  - Dataset generation
  - Fuzzing and adversarial interaction
  - LLM-based cyber-physical deception

---

## Status

- 📌 Actively maintained  
- 📌 Continuously expanded as new papers are reviewed  
- 📌 LLMPot research and development in progress  

---
