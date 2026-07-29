<div align="center">

<img src="https://www.pingequa.com/cdn/shop/files/2_b65696ef-2a3d-4d7e-830c-7a92575a965f.jpg?width=1946" alt="Stick RF 424 for M5StickC Plus — CC1101 and nRF24L01+ Dual RF Module by PINGEQUA" width="720"/>

# Stick RF 424 for M5StickC Plus

**Dual RF Module — CC1101 (Sub-GHz / 433MHz) + nRF24L01+ (2.4GHz) with Physical Slide Switch**

[![Firmware](https://img.shields.io/badge/Firmware-Bruce%20Latest%20Beta-brightgreen)](https://bruce.computer/flasher)
[![Frequency](https://img.shields.io/badge/Frequency-433MHz%20%7C%202.4GHz-blue)](#technical-specifications)
[![Chipsets](https://img.shields.io/badge/Chipsets-CC1101%20%7C%20nRF24L01%2B-orange)](#technical-specifications)
[![Reviews](https://img.shields.io/badge/Reviews-92%20★-yellow)](https://www.pingequa.com/products/stick-rf-424-module?utm_source=github&utm_medium=readme&utm_campaign=stick-rf-424)
[![Buy](https://img.shields.io/badge/Buy-PINGEQUA%20Store-red)](https://www.pingequa.com/products/stick-rf-424-module?utm_source=github&utm_medium=readme&utm_campaign=stick-rf-424)

**[➡ Buy Now — $24.98 USD](https://www.pingequa.com/products/stick-rf-424-module?utm_source=github&utm_medium=readme&utm_campaign=stick-rf-424)**  |  **[Support & Setup Guide](https://www.pingequa.com/pages/support-m5stack-stickc-plus-2-in-1-module?utm_source=github&utm_medium=readme&utm_campaign=stick-rf-424)**  |  **[YouTube @PINGEQUA](https://www.youtube.com/@PINGEQUA)**

</div>

---

## Overview

The **Stick RF 424** is a dual-band RF module for the **M5StickC Plus 1.1 / Plus 2 and the M5Stack Cardputer**. It packs a **CC1101** (Sub-GHz / 433MHz) and an **nRF24L01+** (2.4GHz) onto a single compact board, with a **physical hardware slide switch** that provides true electrical isolation between chipsets — zero latency, zero software overhead.

With 92+ community reviews and compatibility with **Bruce firmware**, the Stick RF 424 is one of PINGEQUA's most popular modules for Sub-GHz signal research, 2.4GHz interaction, and wireless education.

> Built by [PINGEQUA](https://www.pingequa.com?utm_source=github&utm_medium=readme&utm_campaign=stick-rf-424) — *Precision Gear for Hackers.*

---

## Key Features

| Feature | Description |
|---------|-------------|
| **Dual-Band RF** | CC1101 (Sub-GHz / 433MHz) + nRF24L01+ (2.4GHz) |
| **Physical Slide Switch** | Hardware isolation between chipsets — true electrical separation |
| **Bruce Firmware Ready** | CC1101 and NRF24 both supported via "Legacy" module settings |
| **Low-Noise PCB** | Enhanced capacitance design for stable RF transmission |
| **Plug-and-Play** | Inserts into the SD slot, GPIO pins connected with the included Grove cable — no soldering required |
| **Multi-Host Fit** | Designed for StickC Plus 1.1, StickC Plus 2, and M5Stack Cardputer |

---

## Technical Specifications

| Parameter | CC1101 | nRF24L01+ |
|-----------|--------|-----------|
| **Frequency** | Sub-GHz (315 / 433 / 868 / 915 MHz) | 2.400 – 2.525 GHz |
| **Protocol** | FSK / OOK / ASK | Enhanced ShockBurst |
| **Switch Position** | 433 MHz side | 2.4 GHz side |
| **Bruce Config** | RF → CONFIG → RF MODULE → CC1101 (Legacy) | NRF24 (Legacy) — activate and go |

| Component | Spec |
|-----------|------|
| **Isolation** | Physical slide switch (electrical separation) |
| **PCB Design** | Low-noise with enhanced capacitance |
| **Host Device** | M5StickC Plus 1.1 / M5StickC Plus 2 / M5Stack Cardputer |
| **Required Firmware** | Bruce latest beta (avoid v1.13 stable) |
| **Price** | $24.98 USD |
| **Community Reviews** | 92+ reviews |

---

## Compatibility

| Device | Status |
|--------|--------|
| M5StickC Plus 1.1 | ✅ Fully supported |
| M5StickC Plus 2 | ✅ Fully supported |
| Bruce Firmware (latest beta) | ✅ Required |
| Bruce Firmware v1.13 stable | ❌ Known `CC1101 NOT FOUND` bug — do not use |
| M5Stack StickS3 | ❌ Use [RF PACK S3](https://github.com/pingequalab/rf-pack-s3) instead |
| M5Stack Cardputer | ✅ Fully supported |
| M5Stack Cardputer **ADV** | ❌ Use [Hydra RF series](https://www.pingequa.com/pages/wiki?utm_source=github&utm_medium=readme&utm_campaign=stick-rf-424) instead |

---

## Quick Start

### Step 1 — Flash Bruce Firmware (Latest Beta)

> ⚠️ **Do NOT use Bruce v1.13 stable.** It has a known SPI timing bug that causes `CC1101 NOT FOUND` on M5StickC Plus 1.1 hardware. Use the latest beta instead.

Flash at: **[bruce.computer/flasher](https://bruce.computer/flasher)**  
Select the **latest beta** build for M5StickC Plus.

### Step 2 — Attach the Module

Insert the Stick RF 424 board into the host's SD slot, then connect the GPIO pins with the included Grove cable. No soldering required.

A loose Grove cable is a common cause of `CC1101 NOT FOUND` — seat it fully at both ends.

### Step 3 — Select Module with Slide Switch

Physically slide the switch to select the active chipset:

| Switch Position | Active Module |
|-----------------|--------------|
| 433 MHz | CC1101 (Sub-GHz) |
| 2.4 GHz | nRF24L01+ |

### Step 4 — Configure in Bruce Firmware

**CC1101 (433MHz / Sub-GHz):**
```
RF → CONFIG → RF MODULE → CC1101 (Legacy)
```

**nRF24L01+ (2.4GHz):**
```
RF → CONFIG → RF MODULE → NRF24 (Legacy)
```

> Use the **"Legacy"** setting for both modules — this ensures zero-latency module detection.

---

## Product Gallery

<div align="center">

| | | |
|---|---|---|
| <img src="https://www.pingequa.com/cdn/shop/files/2_b65696ef-2a3d-4d7e-830c-7a92575a965f.jpg?width=800" width="220" alt="Stick RF 424 front view"/> | <img src="https://www.pingequa.com/cdn/shop/files/1_9813e3af-68f7-4560-94a4-83a0d5c920cc.jpg?width=800" width="220" alt="Stick RF 424 on M5StickC Plus"/> | <img src="https://www.pingequa.com/cdn/shop/files/3_5e269f77-652c-4bdf-ad27-18650475a3eb.jpg?width=800" width="220" alt="Stick RF 424 slide switch detail"/> |
| <img src="https://www.pingequa.com/cdn/shop/files/5_2e56021b-45fc-4b7e-831e-2cd4bcbc30bc.jpg?width=800" width="220" alt="Stick RF 424 circuit board top"/> | <img src="https://www.pingequa.com/cdn/shop/files/6_b18f4f6d-9635-49e9-a403-2c9fcdca5871.jpg?width=800" width="220" alt="Stick RF 424 installed"/> | <img src="https://www.pingequa.com/cdn/shop/files/7_0d6ea3c7-7446-4ce0-a2bf-1393eaafba40.jpg?width=800" width="220" alt="Stick RF 424 packaging"/> |

</div>

---

## Documentation

| Resource | Link |
|----------|------|
| Setup & Troubleshooting Guide | [PINGEQUA Support Page](https://www.pingequa.com/pages/support-m5stack-stickc-plus-2-in-1-module?utm_source=github&utm_medium=readme&utm_campaign=stick-rf-424) |
| Setup Guide (Wiki) | [Setup Guide](../../wiki/Setup-Guide) |
| Firmware Guide (Wiki) | [Firmware Guide](../../wiki/Firmware-Guide) |
| Troubleshooting (Wiki) | [Troubleshooting](../../wiki/Troubleshooting) |
| FAQ (Wiki) | [FAQ](../../wiki/FAQ) |
| Bruce Firmware Flasher | [bruce.computer/flasher](https://bruce.computer/flasher) |
| Bruce Wiki | [github.com/pr3y/Bruce/wiki](https://github.com/pr3y/Bruce/wiki/) |
| PINGEQUA Wiki | [pingequa.com/pages/wiki](https://www.pingequa.com/pages/wiki?utm_source=github&utm_medium=readme&utm_campaign=stick-rf-424) |

---

## Related Products from PINGEQUA

| Product | For Device |
|---------|-----------|
| [Stick RF 424](https://www.pingequa.com/products/stick-rf-424-module?utm_source=github&utm_medium=readme&utm_campaign=stick-rf-424) | M5StickC Plus 1.1 / 2 · M5Stack Cardputer |
| [RF PACK S3](https://github.com/pingequalab/rf-pack-s3) | M5Stack StickS3 |
| [Hydra RF 424 Cap](https://www.pingequa.com/pages/wiki?utm_source=github&utm_medium=readme&utm_campaign=stick-rf-424) | M5Stack Cardputer |
| [SWITCHBLADE RF 3-in-1](https://www.pingequa.com/pages/wiki?utm_source=github&utm_medium=readme&utm_campaign=stick-rf-424) | Flipper Zero |
| [BW16 Devboard](https://www.pingequa.com/pages/wiki?utm_source=github&utm_medium=readme&utm_campaign=stick-rf-424) | Flipper Zero |

> Explore the full lineup at [pingequa.com/pages/wiki](https://www.pingequa.com/pages/wiki?utm_source=github&utm_medium=readme&utm_campaign=stick-rf-424)

---

## Disclaimer

This product is intended for **educational and authorized research purposes only**. Users bear full legal responsibility for their actions. Always obtain explicit permission from network or device owners before conducting any testing. PINGEQUA does not condone unauthorized use.

---

<div align="center">

**[Buy Stick RF 424 — $24.98 USD](https://www.pingequa.com/products/stick-rf-424-module?utm_source=github&utm_medium=readme&utm_campaign=stick-rf-424)**

Made with precision by [PINGEQUA](https://www.pingequa.com?utm_source=github&utm_medium=readme&utm_campaign=stick-rf-424) · [@PINGEQUA on YouTube](https://www.youtube.com/@PINGEQUA)

</div>
