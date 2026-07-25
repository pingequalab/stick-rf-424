# Setup Guide — Stick RF 424 for M5StickC Plus

> **[Buy Stick RF 424 — $24.98 USD](https://www.pingequa.com/products/stick-rf-424-module?utm_source=github&utm_medium=wiki&utm_campaign=stick-rf-424)** | [Back to Wiki Home](Home) | [PINGEQUA Support Page](https://www.pingequa.com/pages/support-m5stack-stickc-plus-2-in-1-module?utm_source=github&utm_medium=wiki&utm_campaign=stick-rf-424)

---

## Requirements

| Item | Notes |
|------|-------|
| M5StickC Plus 1.1 or 2 | Required host device |
| Stick RF 424 board | The RF module |
| Bruce firmware (latest beta) | Do NOT use v1.13 stable |
| USB-C cable | For flashing firmware |
| Computer (Chrome or Edge) | For web flasher |

---

## Step 1 — Flash Bruce Firmware (Latest Beta)

> ⚠️ **Critical:** Do NOT use Bruce v1.13 stable. It has a known SPI bus timing bug that causes `CC1101 NOT FOUND` on M5StickC Plus 1.1. Always use the latest beta.

1. Open **[bruce.computer/flasher](https://bruce.computer/flasher)** in Chrome or Edge.
2. Connect your M5StickC Plus via USB-C.
3. Select **M5StickC Plus** as the target device.
4. Choose the **latest beta** build.
5. Click **Flash** and follow on-screen prompts.
6. Reboot after flashing.

---

## Step 2 — Attach the Module

1. Power off your M5StickC Plus.
2. Connect the Stick RF 424 to the GPIO header of the M5StickC Plus.
3. No soldering required.
4. Power on the device.

---

## Step 3 — Select Module with Slide Switch

Use the physical slide switch on the Stick RF 424 to select which chipset is active:

| Switch Position | Active Module |
|-----------------|--------------|
| 433 MHz | CC1101 (Sub-GHz / 433MHz) |
| 2.4 GHz | nRF24L01+ (2.4GHz) |

Only one chipset can be active at a time. This is enforced by physical hardware isolation.

---

## Step 4 — Configure CC1101 in Bruce

With switch in the **433 MHz** position:

```
RF → CONFIG → RF MODULE → CC1101 (Legacy)
```

> Always use **Legacy** mode. This ensures zero-latency module detection.

---

## Step 5 — Configure nRF24 in Bruce

With switch in the **2.4 GHz** position:

```
RF → CONFIG → RF MODULE → NRF24 (Legacy)
```

> Use **Legacy** mode for nRF24 as well.

---

## Verification

- [ ] Bruce firmware is latest beta (check Settings or boot screen)
- [ ] No `CC1101 NOT FOUND` error
- [ ] CC1101 works with switch in 433MHz position
- [ ] nRF24 works with switch in 2.4GHz position

---

## Next Steps

- [Firmware Guide](Firmware-Guide) — Version details and known bug in v1.13
- [Troubleshooting](Troubleshooting) — Fix common errors
- [FAQ](FAQ) — Common questions answered

---

> *For educational and authorized research purposes only.*
