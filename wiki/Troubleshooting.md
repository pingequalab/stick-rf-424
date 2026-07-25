# Troubleshooting — Stick RF 424 for M5StickC Plus

> **[Buy Stick RF 424 — $24.98 USD](https://www.pingequa.com/products/stick-rf-424-module?utm_source=github&utm_medium=wiki&utm_campaign=stick-rf-424)** | [Back to Wiki Home](Home) | [PINGEQUA Support](https://www.pingequa.com/pages/support-m5stack-stickc-plus-2-in-1-module?utm_source=github&utm_medium=wiki&utm_campaign=stick-rf-424)

---

## Problem: "CC1101 NOT FOUND"

**Symptom:** Device shows `CC1101 NOT FOUND` in the RF menu.

**Cause:** Bruce v1.13 stable is installed. This version has a known SPI timing bug on M5StickC Plus 1.1.

**Fix:**
1. Flash the **latest Bruce beta** at [bruce.computer/flasher](https://bruce.computer/flasher).
2. Reboot the device.
3. Confirm CC1101 appears in the RF menu.

---

## Problem: CC1101 Not Working After Flashing Beta

**Symptom:** Latest beta installed but CC1101 still not detected.

| Cause | Fix |
|-------|-----|
| Slide switch in wrong position | Move switch to the **433 MHz** side |
| Module not configured as Legacy | Set to `RF → CONFIG → RF MODULE → CC1101 (Legacy)` |
| Module not fully connected | Power off, re-seat the GPIO header connection, power on |
| Wrong firmware variant flashed | Confirm you flashed the **M5StickC Plus** variant |

---

## Problem: nRF24 Not Responding

**Symptom:** nRF24 features produce no results or errors.

**Fix:**
1. Slide the switch to the **2.4 GHz** position.
2. In Bruce: `RF → CONFIG → RF MODULE → NRF24 (Legacy)`
3. Confirm the module is fully seated on the GPIO header.

Note: nRF24 range is limited on this hardware due to low-power design constraints.

---

## Problem: Unstable Signal / Dropped Transmissions

**Symptom:** Intermittent transmissions or weak signal.

| Cause | Fix |
|-------|-----|
| Loose GPIO connection | Re-seat the module with device powered off |
| Low battery | Charge M5StickC Plus fully |
| Environmental 2.4GHz congestion | Move to a less congested area for 2.4GHz testing |
| Wrong chipset selected | Ensure slide switch matches the module you want to use |

---

## Problem: Device Won't Boot After Attaching Module

**Symptom:** M5StickC Plus freezes or fails to boot with module attached.

**Fix:**
1. Remove the module and confirm the device boots normally.
2. Inspect GPIO header for bent pins or debris.
3. Re-attach module carefully with device powered off.
4. If the issue persists, contact [PINGEQUA support](https://www.pingequa.com/policies/contact-information?utm_source=github&utm_medium=wiki&utm_campaign=stick-rf-424).

---

## Problem: Web Flasher Not Detecting Device

**Fix:**
- Use **Chrome** or **Edge** (Web Serial API is required).
- Try a different USB-C cable (data cable, not charge-only).
- On macOS/Linux: run `ls /dev/tty.*` to confirm the device appears.
- Hold the boot button on M5StickC Plus while connecting USB to enter download mode.

---

## Still Having Issues?

- [PINGEQUA Support Page](https://www.pingequa.com/pages/support-m5stack-stickc-plus-2-in-1-module?utm_source=github&utm_medium=wiki&utm_campaign=stick-rf-424)
- [YouTube @PINGEQUA](https://www.youtube.com/@PINGEQUA)
- Email: [pingltd@hotmail.com](mailto:pingltd@hotmail.com)

---

> *For educational and authorized research purposes only.*
