# Firmware Guide — Bruce Firmware for Stick RF 424

> **[Buy Stick RF 424 — $24.98 USD](https://www.pingequa.com/products/stick-rf-424-module?utm_source=github&utm_medium=wiki&utm_campaign=stick-rf-424)** | [Back to Wiki Home](Home) | [Bruce Firmware Flasher](https://bruce.computer/flasher)

---

## Required Firmware

The Stick RF 424 requires **Bruce firmware (latest beta)** on M5StickC Plus.

| Firmware Version | CC1101 Support | nRF24 Support | Notes |
|-----------------|---------------|--------------|-------|
| Latest beta | ✅ Yes | ✅ Yes | **Recommended — use this** |
| v1.13 stable | ❌ No | ⚠️ Partial | Known SPI bug on StickC Plus 1.1 |
| < v1.13 | ❌ No | ❌ No | Unsupported |

---

## Why Avoid Bruce v1.13 Stable?

Bruce v1.13 stable introduced a **SPI bus timing regression** that affects M5StickC Plus 1.1 hardware. The root causes:

1. **SPI initialization bug** — Changed SPI timing parameters break CC1101 communication, causing `CC1101 NOT FOUND`.
2. **AXP2101 power management** — Improper initialization of the AXP2101 PMIC on M5StickC Plus 1.1 can prevent stable module power-up.

The latest Bruce beta includes critical patches for both issues, restoring **100% module recognition** on M5StickC Plus 1.1.

---

## How to Flash the Latest Bruce Beta

### Using the Web Flasher (Recommended)

1. Open **[bruce.computer/flasher](https://bruce.computer/flasher)** in Chrome or Edge.
2. Connect M5StickC Plus via USB-C.
3. Select **M5StickC Plus** as target device.
4. Select the **latest beta** from the version dropdown.
5. Click **Flash** and wait for completion.
6. Reboot the device.

> Web Serial API requires Chrome or Edge. Firefox and Safari are not supported.

### Manual Flashing (Advanced)

```bash
esptool.py --chip esp32 --port /dev/ttyUSB0 write_flash 0x0 bruce-stickc-plus-beta.bin
```

Replace the port and filename with your actual values.

---

## After Flashing

1. Attach the Stick RF 424 module.
2. Slide switch to 433 MHz for CC1101.
3. Navigate: `RF → CONFIG → RF MODULE → CC1101 (Legacy)`
4. Or slide to 2.4 GHz and select `NRF24 (Legacy)`.

See [Setup Guide](Setup-Guide) for full walkthrough.

---

## Bruce Firmware Resources

| Resource | Link |
|----------|------|
| Web Flasher | [bruce.computer/flasher](https://bruce.computer/flasher) |
| Bruce GitHub | [github.com/pr3y/Bruce](https://github.com/pr3y/Bruce) |
| Bruce Wiki | [github.com/pr3y/Bruce/wiki](https://github.com/pr3y/Bruce/wiki/) |
| Bruce Releases | [github.com/pr3y/Bruce/releases](https://github.com/pr3y/Bruce/releases) |

---

> *For educational and authorized research purposes only.*
