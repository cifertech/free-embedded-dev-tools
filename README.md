<div align="center">

  <br/>
  <br/>
  <p align="center">
    <a href="https://github.com/cifertech/free-embedded-dev-tools"><img src="https://img.shields.io/static/v1?label=cifertech&message=free-embedded-dev-tools&color=orange&logo=github"/></a>
    <a href="https://github.com/cifertech/free-embedded-dev-tools"><img src="https://img.shields.io/github/stars/cifertech/free-embedded-dev-tools?style=social"/></a>
    <a href="https://github.com/cifertech/free-embedded-dev-tools"><img src="https://img.shields.io/github/forks/cifertech/free-embedded-dev-tools?style=social"/></a>
    <img src="https://img.shields.io/badge/Embedded-Firmware%20%2B%20Hardware-orange?logo=espressif"/>
    <img src="https://img.shields.io/badge/license-MIT-orange"/>
  </p>
  <p align="center">
    <a href="https://twitter.com/techcifer"><img src="https://img.shields.io/badge/Twitter-orange?logo=x&logoColor=black"/></a>
    <a href="https://www.instagram.com/cifertech/"><img src="https://img.shields.io/badge/Instagram-orange?logo=instagram&logoColor=black"/></a>
    <a href="https://www.youtube.com/c/techcifer"><img src="https://img.shields.io/badge/YouTube-orange?logo=youtube&logoColor=black"/></a>
    <a href="https://cifertech.net/"><img src="https://img.shields.io/badge/Website-orange?logo=googlechrome&logoColor=black"/></a>
  </p>
</div>
&nbsp;

<div align="center">

**A curated list of free tools and resources for embedded, firmware, and hardware development.**

PCB design, debugging, simulation, CI, IoT backends, RF, TinyML, and more — one list, kept current.

</div>

---

## :bookmark_tabs: Table of Contents

- [PCB Design & EDA](#triangular_ruler-pcb-design--eda)
- [Debug Probes & JTAG/SWD](#mag-debug-probes--jtagswd)
- [Simulation](#cyclone-simulation)
- [Logic Analyzers & Signal Tools](#chart_with_upwards_trend-logic-analyzers--signal-tools)
- [CI / Build / Firmware Testing](#gear-ci--build--firmware-testing)
- [Free IoT / Cloud Backends](#cloud-free-iot--cloud-backends)
- [Free Firmware OTA Hosting](#satellite-free-firmware-ota-hosting)
- [Enclosure & 3D Printing](#package-enclosure--3d-printing)
- [RF / Antenna Tools](#satellite_orbital-rf--antenna-tools)
- [Component Search & Datasheets](#mag_right-component-search--datasheets)
- [Power Supply & Regulator Design](#zap-power-supply--regulator-design)
- [RTOS & Bootloader Frameworks](#arrows_counterclockwise-rtos--bootloader-frameworks)
- [Code Quality, Static Analysis & Testing](#white_check_mark-code-quality-static-analysis--testing)
- [TinyML / Edge AI](#robot-tinyml--edge-ai)
- [Power Profiling & Current Measurement](#battery-power-profiling--current-measurement)
- [Parts Inventory & BOM Management](#package-parts-inventory--bom-management)
- [Wireless Pre-Compliance & Regulatory Lookup](#scales-wireless-pre-compliance--regulatory-lookup)
- [Hardware Version Control & Collaboration](#arrows_clockwise-hardware-version-control--collaboration)
- [Free Courses & Learning](#books-free-courses--learning)
- [Component Sourcing & Free Samples](#gift-component-sourcing--free-samples)
- [Contributing](#handshake-contributing)

---

## :triangular_ruler: PCB Design & EDA

| Tool | What's Free | Limits / Notes |
|---|---|---|
| [KiCad](https://www.kicad.org/) | Entire suite, no account, no usage cap | Fully open-source (GPLv3), offline, up to 32 copper layers. The safest long-term free choice — no commercial restrictions. |
| [EasyEDA](https://easyeda.com/) | Standard Edition: full schematic capture, layout, SPICE sim, manufacturing export | Cloud-only, tied to JLCPCB's ecosystem and part catalog. Great for quick projects, weaker for complex/high-layer-count boards. |
| [Altium CircuitMaker](https://circuitmaker.com/) | Full Altium-engine EDA, free | Windows-only, cloud-hosted projects, capped at ~5 private projects. Good on-ramp if you'll eventually pay for Altium. |
| [LibrePCB](https://librepcb.org/) | Fully free and open, no limits | Smaller community than KiCad but genuinely unrestricted. |
| [Quilter](https://www.quilter.ai/) (AI routing) | Free tier, full routing engine | Plugs into KiCad/Altium/Cadence as a routing add-on, not a full EDA suite. Free-tier designs are used to train their models — don't upload anything proprietary. |

## :mag: Debug Probes & JTAG/SWD

| Tool | What's Free | Notes |
|---|---|---|
| [OpenOCD](https://openocd.org/) | Free, open-source | The software side of most JTAG/SWD debugging; works with a wide range of adapters. |
| [Black Magic Debug](https://black-magic.org/) | Free firmware for compatible probes, or run standalone | Plug-and-play GDB server, no separate host software needed — just GDB. |
| [ESP-Prog](https://docs.espressif.com/) | Design files are open-source; ~$15 hardware | Espressif's own JTAG+auto-flash board for ESP-IDF work — the standard companion for serious ESP32 firmware debugging. |
| [J-Link EDU / EDU Mini](https://www.segger.com/) | Free-as-in-price for **non-commercial** use only | Real SEGGER hardware/software, but licensing explicitly forbids commercial work — check this before using it on a paid project. |
| [PlatformIO Unified Debugger](https://docs.platformio.org/en/latest/plus/debugging.html) | Free with PlatformIO Core | Zero-config debugging across ~20 supported probes (ST-Link, J-Link, ESP-Prog, Black Magic, etc.) from one interface. |

## :cyclone: Simulation

| Tool | What's Free | Notes |
|---|---|---|
| [ngspice](https://ngspice.sourceforge.io/) / KiCad's built-in SPICE | Free, open-source | Circuit-level simulation baked into KiCad's schematic editor. |
| [Falstad Circuit Simulator](https://www.falstad.com/circuit/) | Free, browser-based | Great for quick intuition/teaching, not for serious design verification. |
| [Wokwi](https://wokwi.com/) | Free tier, browser-based | Simulates ESP32/Arduino/Pi Pico with virtual peripherals (sensors, displays) before you touch real hardware — genuinely useful for firmware logic testing pre-flash. |
| [Renode](https://renode.io/) | Free, open-source | Full system simulation (CPU + peripherals + network) for testing firmware without hardware; used in PlatformIO's debug backends too. |

## :chart_with_upwards_trend: Logic Analyzers & Signal Tools

| Tool | What's Free | Notes |
|---|---|---|
| [PulseView](https://sigrok.org/wiki/PulseView) (sigrok) | Free, open-source | GUI for a huge range of cheap USB logic analyzers (including generic $10 24MHz clones) with protocol decoders for UART/SPI/I2C/etc. |
| [Saleae Logic software](https://www.saleae.com/) | Free software, but requires their (paid) hardware | Software itself has no license fee — only relevant if you already own a Saleae device. |

## :gear: CI / Build / Firmware Testing

| Tool | What's Free | Notes |
|---|---|---|
| [GitHub Actions](https://github.com/features/actions) | 2,000 free CI minutes/month on public+private repos (unlimited on public) | Standard for ESP-IDF/PlatformIO build matrices — most of the ESP32-DIV-style projects already use this. |
| [PlatformIO Core](https://platformio.org/) | Free CLI + build system | Multi-board, multi-framework builds without vendor IDE lock-in. |
| [Wokwi CI](https://docs.wokwi.com/vscode/ci-server) | Free tier for CI-triggered simulation | Run simulated hardware-in-the-loop tests inside GitHub Actions instead of needing physical boards in CI. |

## :cloud: Free IoT / Cloud Backends

| Service | What's Free | Limits |
|---|---|---|
| [HiveMQ Cloud](https://www.hivemq.com/mqtt-cloud-broker/) | Free MQTT broker tier | 100 device connections, capped throughput — fine for prototyping. |
| [ThingSpeak](https://thingspeak.com/) | Free tier | 3,000,000 messages/year at free tier, decent for logging sensor data from a single project. |
| [Adafruit IO](https://io.adafruit.com/) | Free tier | Rate-limited but purpose-built for hobbyist IoT dashboards, works great with ESP32/Arduino out of the box. |
| [Firebase Spark plan](https://firebase.google.com/pricing) | Free tier | Realtime DB + hosting, generous enough for small device fleets. |

## :satellite: Free Firmware OTA Hosting

| Approach | What's Free | Notes |
|---|---|---|
| GitHub Releases + raw manifest | Fully free, no account limits beyond normal GitHub quotas | Host `firmware.bin` as a release asset, host a small `version.json` manifest (GitHub Releases API or a raw file in the repo), device GETs the manifest on boot and compares versions. Zero backend to run — the pattern most solo/hobbyist ESP32 fleets actually use. |
| [JSONhost](https://jsonhost.com/) (or similar free JSON-endpoint hosts) | Free tier | Gives a stable public GET endpoint for the version manifest specifically, if you don't want to depend on GitHub's raw-content URLs. |
| ESP-IDF native OTA (self-hosted) | Free, built into ESP-IDF | HTTPS pull model: device checks your own server, downloads a signed image, validates, swaps partitions. No SaaS, but you own the server. Good once you need proper partition-swap safety instead of a naive re-flash. |
| [Golioth](https://golioth.io/) / [Memfault](https://memfault.com/) free tiers | Free tier for small fleets | Add staged rollouts, rollback, and fleet observability once you outgrow the manifest-file approach — worth knowing about before you build your own fleet dashboard from scratch. |

> Reality check: a GitHub Releases manifest is fine for a handful of devices you personally maintain. Once you're shipping to end users, budget for real signing + rollback — a bad OTA push to a partition scheme with no fallback is how devices get bricked in the field.

## :package: Enclosure & 3D Printing

| Tool | What's Free | Notes |
|---|---|---|
| [FreeCAD](https://www.freecad.org/) | Fully free, open-source | Parametric CAD for enclosures; steeper learning curve than Fusion but zero licensing restrictions. |
| [Fusion 360 Personal Use](https://www.autodesk.com/products/fusion-360/personal) | Free for hobbyist/non-commercial use | The most common choice for maker enclosures; commercial use requires a paid license — check the terms before selling anything designed in it. |
| [Onshape Free Tier](https://www.onshape.com/) | Free for public (non-private) documents | Browser-based, real-time collaborative CAD; free tier designs are publicly visible, same tradeoff as EasyEDA's cloud model. |
| [PrusaSlicer](https://www.prusa3d.com/page/prusaslicer_424/) / [Cura](https://ultimaker.com/software/ultimaker-cura/) | Fully free | Standard slicers, work with virtually any FDM printer, not locked to one vendor. |
| [Printables](https://www.printables.com/) / [Thingiverse](https://www.thingiverse.com/) | Free STL hosting + huge existing library | Worth checking before modeling a standard enclosure shape from scratch — standoffs, DIN rail clips, and battery holders are almost always already out there. |

## :satellite_orbital: RF / Antenna Tools

| Tool | What's Free | Notes |
|---|---|---|
| [NEC2](https://www.nec2.org/) / [4nec2](https://www.qsl.net/4nec2/) | Free, open-source antenna modeling | The standard free tool for simulating wire antenna performance (gain, impedance, radiation pattern) before you cut copper. |
| [openEMS](https://www.openems.de/) | Free, open-source FDTD electromagnetic simulator | Full 3D EM simulation for PCB antennas and RF structures — heavier setup than NEC2 but handles planar/PCB antennas properly. |
| [SimSmith](https://www.ae6ty.com/Smith_Charts.html) | Free | Smith chart tool for matching network design — genuinely useful when tuning antenna matching on ESP32-DIV-class RF front ends. |
| [rtl_433](https://github.com/merbanan/rtl_433) / [GNU Radio](https://www.gnuradio.org/) | Free, open-source | Standard free SDR tooling for decoding and analyzing SubGHz/ISM-band signals during RF firmware development. |

## :mag_right: Component Search & Datasheets

| Tool | What's Free | Notes |
|---|---|---|
| [Octopart](https://octopart.com/) | Free search, no account needed for basic use | Cross-distributor part search (stock, price, datasheets) across DigiKey/Mouser/LCSC/etc in one query — the fastest way to check if a part is actually in stock before designing it in. |
| [Findchips](https://www.findchips.com/) | Free | Similar cross-distributor aggregator, useful as a second opinion when Octopart's data looks stale. |
| [DigiKey](https://www.digikey.com/) / [Mouser](https://www.mouser.com/) / [LCSC](https://www.lcsc.com/) parametric search | Free | Each distributor's own parametric filter search is free and often more detailed than aggregators for that distributor's stock specifically. |
| [SnapMagic (SnapEDA)](https://www.snapeda.com/) | Free schematic symbols + PCB footprints for millions of parts | Downloadable straight into KiCad/Altium/Eagle format — saves the single most tedious part of adding a new component to a design. |

## :zap: Power Supply & Regulator Design

| Tool | What's Free | Notes |
|---|---|---|
| [TI WEBENCH / Power Designer](https://www.ti.com/design-resources/design-tools-simulation/webench-power-designer.html) | Free, browser-based | Input your voltage/current requirements, get a ranked list of TI regulator topologies with a generated schematic and BOM — genuinely saves hours versus manually comparing buck/boost ICs. |
| [Analog Devices ADIsimPower](https://www.analog.com/) | Free | Same category of tool, scoped to ADI's regulator lineup. |
| [Battery life / capacity calculators](https://www.digikey.com/en/resources/design-tools) (various, DigiKey's tool hub) | Free | Quick sanity checks for runtime estimates before committing to a battery + duty-cycle design. |

## :arrows_counterclockwise: RTOS & Bootloader Frameworks

| Tool | What's Free | Notes |
|---|---|---|
| [FreeRTOS](https://www.freertos.org/) | Free, open-source (MIT) | What ESP-IDF is already built on; worth knowing directly when you need finer task/queue/semaphore control than the Arduino abstraction gives you. |
| [Zephyr RTOS](https://www.zephyrproject.org/) | Free, open-source | Broader hardware support than FreeRTOS alone (many non-Espressif chips), Linux Foundation-backed, a real option if a future project moves off ESP32. |
| [MCUboot](https://www.mcuboot.com/) | Free, open-source | The standard secure bootloader for signed, rollback-safe firmware updates — pairs naturally with the OTA hosting section above once you outgrow a naive re-flash. |

## :white_check_mark: Code Quality, Static Analysis & Testing

| Tool | What's Free | Notes |
|---|---|---|
| [cppcheck](http://cppcheck.sourceforge.net/) | Free, open-source | Static analysis for C/C++ — catches real bugs (buffer overruns, null derefs, uninitialized reads) before they become a 2 a.m. field-debugging session. |
| [clang-tidy](https://clang.llvm.org/extra/clang-tidy/) | Free, open-source | Deeper static analysis + auto-fixable style checks, integrates with most editors and CI. |
| [Unity](https://www.throwtheswitch.org/unity) / [Ceedling](https://www.throwtheswitch.org/ceedling) | Free, open-source | Lightweight C unit testing frameworks built specifically for embedded, run on-host or on-target. |
| [PlatformIO Unit Testing](https://docs.platformio.org/en/latest/advanced/unit-testing/index.html) | Free, built into PlatformIO Core | Runs the same test suite on native host and on real target hardware from one config. |
| [PVS-Studio](https://pvs-studio.com/en/pvs-studio/) free license | Free for open-source projects | Commercial-grade static analyzer, free if your repo qualifies as open-source — worth applying for on a starred project like ESP32-DIV. |

## :robot: TinyML / Edge AI

| Tool | What's Free | Notes |
|---|---|---|
| [Edge Impulse](https://www.edgeimpulse.com/) | Free for individual developers | End-to-end data-collect → train → deploy workflow, exports optimized C++ straight to ESP32/Cortex-M targets — the fastest path from "I have a sensor" to "I have a running classifier." |
| [TensorFlow Lite Micro](https://www.tensorflow.org/lite/microcontrollers) | Free, open-source | The underlying inference runtime most TinyML tools (including Edge Impulse's exports) build on; worth knowing directly for full control over model size/arena allocation. |
| [CMSIS-NN](https://github.com/ARM-software/CMSIS-NN) | Free, open-source | ARM's hand-optimized NN kernels for Cortex-M — meaningful speedup over generic TFLM ops on supported chips. |
| [ESP-DL](https://github.com/espressif/esp-dl) | Free, open-source | Espressif's own inference library tuned specifically for ESP32-S3's vector instructions — the most direct fit if you're staying in the ESP32 ecosystem for on-device ML (relevant to anything in the Wispr/adaptive-cal direction). |

## :battery: Power Profiling & Current Measurement

| Tool | What's Free | Notes |
|---|---|---|
| [Nordic Power Profiler Kit II software](https://www.nordicsemi.com/Products/Development-hardware/Power-Profiler-Kit-2) | Free software (requires their ~$80 hardware) | Real-time current measurement down to µA, the standard tool for validating deep-sleep power claims actually match the datasheet. |
| [Joulescope UI](https://www.joulescope.com/) | Free software (requires their hardware) | Similar category, wide dynamic range for capturing both sleep current and active-radio current spikes in one capture. |
| [ESP-IDF power management logging](https://docs.espressif.com/) | Free, built into ESP-IDF | Software-only estimate (not a substitute for a real measurement, but free and zero extra hardware for a first-pass sanity check). |

## :package: Parts Inventory & BOM Management

| Tool | What's Free | Notes |
|---|---|---|
| [InvenTree](https://inventree.org/) | Free, open-source, self-hosted | The most complete free option — stock control, BOM management, supplier data, and a first-class [KiCad plugin](https://inventree.org/blog/2023/09/26/kicad) that exposes your inventory as a native KiCad symbol library. |
| [Ki-nTree](https://github.com/sparkmicro/Ki-nTree) | Free, open-source | Pulls part data directly from DigiKey/Mouser/LCSC/Element14 APIs and auto-creates matching InvenTree + KiCad library entries in one step — removes most of the manual data entry when adding a new part. |
| [Part-DB](https://github.com/Part-DB/Part-DB-server) | Free, open-source, self-hosted | Similar scope to InvenTree, also has KiCad integration; a reasonable alternative if InvenTree's Django/React stack is heavier than you want to self-host. |
| [PartKeepr](https://github.com/partkeepr/PartKeepr) | Free, open-source | Older, simpler option, originally built for hackerspaces with multiple users sharing one stock of parts. |

##  Wireless Pre-Compliance & Regulatory Lookup

| Tool | What's Free | Notes |
|---|---|---|
| [FCC Table of Frequency Allocations](https://www.fcc.gov/oet/ea/rfdevice) | Free, official | The authoritative source for which bands you're legally allowed to transmit on in the US before you commit an antenna design to a PCB. |
| [FCC ID Search](https://www.fcc.gov/oet/ea/fccid) | Free, official | Look up any existing FCC ID to see what an already-certified module's test filing looked like — useful reference before starting your own. |
| [FCC Equipment Authorization guidance](https://www.fcc.gov/oet/ea/rfdevice) | Free, official | Explains whether your device needs SDoC (Supplier's Declaration of Conformity) or full Certification — this determines how expensive/slow the compliance path will be, worth checking early. |
| Pre-compliance with a cheap SDR/spectrum analyzer | Free (software side) | You still need RF hardware (even a $30 RTL-SDR gives a rough first look), but the analysis software itself (GNU Radio, from the RF section above) costs nothing — catches obvious spurious emissions before you pay for a real EMC lab session. |

> Reality check: nothing here replaces an actual accredited test lab before you sell a product with a radio in it. These are free ways to avoid an expensive surprise at that stage, not a substitute for it.

## :arrows_clockwise: Hardware Version Control & Collaboration

| Tool | What's Free | Notes |
|---|---|---|
| [Git](https://git-scm.com/) + [GitHub](https://github.com/) free tier | Free | KiCad projects are plain text (schematic/PCB files), so standard git diffs and PRs work — the same workflow you already use for firmware works for hardware too. |
| [KiCad's built-in git integration](https://www.kicad.org/) | Free, built-in (KiCad 7+) | Native project-history and diffing inside the KiCad GUI itself, no separate tool needed for basic version tracking. |
| [OSHWLab](https://oshwlab.com/) | Free project hosting | EasyEDA's project-sharing platform if you want a public, forkable hardware project page similar to a GitHub repo, specifically for EDA files. |

## :books: Free Courses & Learning

| Resource | What's Free | Notes |
|---|---|---|
| [HarvardX TinyML EdX course](https://www.edx.org/) | Free to audit | The standard intro course pairing with the Arduino Tiny Machine Learning Kit mentioned in the TinyML section above. |
| [Espressif's official ESP-IDF Programming Guide](https://docs.espressif.com/) | Free, official | Not a "course" exactly, but the single most authoritative free resource for anything ESP32-specific — worth listing since so many Stack Overflow answers are outdated compared to current docs. |
| [KiCad official documentation + forum](https://forum.kicad.info/) | Free | Active community, most common questions already answered — search before posting. |
| [Interrupt (Memfault's blog)](https://interrupt.memfault.com/) | Free | Deep, practical firmware engineering write-ups (debug tooling, OTA, power profiling) from working embedded engineers — one of the better free technical resources in the space. |

## :gift: Component Sourcing & Free Samples

| Source | What's Free | Notes |
|---|---|---|
| [TI Sample Program](https://www.ti.com/) | Free samples of most parts, small qty | Business/edu email speeds approval but isn't strictly required. |
| [Analog Devices Samples](https://www.analog.com/) | Free samples | Similar process to TI. |
| [Microchip Samples](https://www.microchip.com/) | Free samples | — |
| [JLCPCB new-user credit](https://jlcpcb.com/) | Varies, changes monthly | Check current promo before ordering — codes rotate. |

---

## :handshake: Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines. Short version: one row per tool, keep the "what's free" column honest (no "free trial" entries unless clearly labeled as such), and note real limits so nobody gets surprised mid-project.

## :warning: Disclaimer

Free tiers, pricing, and limits change without notice. Entries here reflect the best information available at time of writing — always double-check current terms on the provider's own site before relying on something for a production project. This list explicitly excludes anything that isn't a legitimate, above-board offering (e.g. abusing trial accounts, ToS violations).

## :warning: License

💬 Found something outdated or missing? [Open an Issue](https://github.com/cifertech/free-embedded-dev-tools/issues)

⭐ Find this useful? Star the repo!

🛠 Want to contribute? Fork it and submit a pull request.

<!-- Contact -->
## :handshake: Contact

▶ Support me on Patreon [patreon.com/cifertech](https://www.patreon.com/cifertech)

CiferTech - [@techcifer](https://twitter.com/techcifer) - CiferTech@gmail.com

Project Link: [https://github.com/cifertech/free-embedded-dev-tools](https://github.com/cifertech/free-embedded-dev-tools)
