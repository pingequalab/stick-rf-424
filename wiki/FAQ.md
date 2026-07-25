# FAQ — Stick RF 424 for M5StickC Plus

> **[Buy Stick RF 424 — $24.98 USD](https://www.pingequa.com/products/stick-rf-424-module?utm_source=github&utm_medium=wiki&utm_campaign=stick-rf-424)** | [Back to Wiki Home](Home)

---

## Purchasing & Compatibility

**Q: Where can I buy the Stick RF 424?**  
A: At the [PINGEQUA Store](https://www.pingequa.com/products/stick-rf-424-module?utm_source=github&utm_medium=wiki&utm_campaign=stick-rf-424) for $24.98 USD. Ships globally within 48 hours. Delivery: 7–15 business days.

**Q: Which devices are compatible with Stick RF 424?**  
A: M5StickC Plus 1.1 and M5StickC Plus 2 only.

**Q: Does it work with M5Stack Cardputer?**  
A: No. For Cardputer, use the [Hydra RF 424 Cap](https://www.pingequa.com/pages/wiki?utm_source=github&utm_medium=wiki&utm_campaign=stick-rf-424) or [Hydra RF 924 Pro](https://www.pingequa.com/pages/wiki?utm_source=github&utm_medium=wiki&utm_campaign=stick-rf-424).

**Q: Does it work with M5Stack StickS3?**  
A: No. For StickS3, use the [RF PACK S3](https://github.com/pingequalab/rf-pack-s3).

**Q: Does it work with Flipper Zero?**  
A: No. For Flipper Zero, PINGEQUA offers the [SWITCHBLADE RF 3-in-1](https://www.pingequa.com/pages/wiki?utm_source=github&utm_medium=wiki&utm_campaign=stick-rf-424) and other modules.

**Q: What is the return policy?**  
A: 14 days for unused items. Warranty covers manufacturing defects; excludes improper flashing or overvoltage damage.

---

## Firmware

**Q: Which firmware should I use?**  
A: The **latest Bruce beta**. Do NOT use v1.13 stable — it causes `CC1101 NOT FOUND` due to a SPI timing bug on M5StickC Plus 1.1. Flash at [bruce.computer/flasher](https://bruce.computer/flasher).

**Q: Why is v1.13 stable broken?**  
A: Bruce v1.13 introduced a SPI bus timing regression and an AXP2101 PMIC initialization issue that prevents CC1101 recognition on M5StickC Plus 1.1 hardware. The latest beta fixes both.

**Q: How do I know which firmware version is installed?**  
A: Check the version displayed on the Bruce boot screen or in the Settings menu.

---

## Hardware & Setup

**Q: Is soldering required?**  
A: No. Stick RF 424 uses a GPIO header connection — completely solderless.

**Q: How do I switch between CC1101 and nRF24?**  
A: Use the physical slide switch on the board. Slide to **433 MHz** for CC1101, or **2.4 GHz** for nRF24L01+. Then configure the corresponding Legacy module in Bruce.

**Q: Why is there a physical switch instead of software switching?**  
A: A physical switch provides true electrical isolation between chipsets. This eliminates any possibility of firmware conflicts, timing issues, or cross-chip interference — more reliable than software-only switching.

**Q: What does "Legacy" mode mean in Bruce?**  
A: The Legacy setting uses the original driver initialization path for CC1101 and NRF24 on M5StickC Plus hardware. It ensures zero-latency module detection and is the required setting for Stick RF 424.

**Q: How do I configure CC1101 in Bruce?**  
A: Slide switch to 433 MHz, then: `RF → CONFIG → RF MODULE → CC1101 (Legacy)`

**Q: How do I use nRF24?**  
A: Slide switch to 2.4 GHz, then: `RF → CONFIG → RF MODULE → NRF24 (Legacy)`

---

## Technical

**Q: What Sub-GHz frequencies does CC1101 support?**  
A: 315 MHz, 433 MHz, 868 MHz, and 915 MHz (FSK, OOK, ASK modulation).

**Q: What is the nRF24L01+ frequency range?**  
A: 2.400 to 2.525 GHz. Uses Enhanced ShockBurst protocol.

**Q: Why is 2.4GHz range limited?**  
A: The nRF24L01+ on this module is designed for low-power use, which limits its transmission range. This is also related to regional legal constraints on transmission power.

**Q: Can both CC1101 and nRF24 be active at the same time?**  
A: No. The physical slide switch ensures only one chipset is electrically connected at a time.

---

## Support

**Q: Where can I get help?**  
A:
- [PINGEQUA Support Page](https://www.pingequa.com/pages/support-m5stack-stickc-plus-2-in-1-module?utm_source=github&utm_medium=wiki&utm_campaign=stick-rf-424)
- [YouTube @PINGEQUA](https://www.youtube.com/@PINGEQUA)
- Email: [pingltd@hotmail.com](mailto:pingltd@hotmail.com)

---

> *For educational and authorized research purposes only. Always obtain explicit permission before testing on any network or device you do not own.*
