<div align="center">

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

**A curated list of free tools and resources for embedded, firmware, and hardware development.**

PCB design, debugging, simulation, CI, IoT backends, RF, TinyML, and more.

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
| [KiCad](https://www.kicad.org/) | Entire suite, no account, no usage cap | Open-source (GPLv3), offline, up to 32 copper layers. No commercial restrictions. |
| [EasyEDA](https://easyeda.com/) | Standard Edition: schematic, layout, SPICE sim, manufacturing export | Cloud-only, tied to JLCPCB. Good for quick projects; weaker for complex boards. |
| [Altium CircuitMaker](https://circuitmaker.com/) | Full Altium-engine EDA | Windows-only, cloud-hosted projects, ~5 private projects max. |
| [LibrePCB](https://librepcb.org/) | Fully free and open | Smaller community than KiCad, but unrestricted. |
| [Quilter](https://www.quilter.ai/) (AI routing) | Free tier, full routing engine | Add-on for KiCad/Altium/Cadence, not a full EDA suite. Free-tier designs may be used for model training; avoid proprietary designs. |

## :mag: Debug Probes & JTAG/SWD

| Tool | What's Free | Notes |
|---|---|---|
| [OpenOCD](https://openocd.org/) | Free, open-source | Software side of most JTAG/SWD debugging; works with many adapters. |
| [Black Magic Debug](https://black-magic.org/) | Free firmware for compatible probes, or run standalone | Plug-and-play GDB server; no separate host software needed. |
| [ESP-Prog](https://docs.espressif.com/) | Open-source design files; ~$15 hardware | Espressif JTAG + auto-flash board for ESP-IDF work. |
| [J-Link EDU / EDU Mini](https://www.segger.com/) | Free for **non-commercial** use only | Real SEGGER hardware/software. Check licensing before commercial use. |
| [PlatformIO Unified Debugger](https://docs.platformio.org/en/latest/plus/debugging.html) | Free with PlatformIO Core | Debugging across ~20 probes (ST-Link, J-Link, ESP-Prog, Black Magic, etc.) from one interface. |

## :cyclone: Simulation

| Tool | What's Free | Notes |
|---|---|---|
| [ngspice](https://ngspice.sourceforge.io/) / KiCad's built-in SPICE | Free, open-source | Circuit-level simulation in KiCad's schematic editor. |
| [Falstad Circuit Simulator](https://www.falstad.com/circuit/) | Free, browser-based | Good for quick intuition and teaching, not design verification. |
| [Wokwi](https://wokwi.com/) | Free tier, browser-based | Simulates ESP32/Arduino/Pi Pico with virtual peripherals before hardware is available. |
| [Renode](https://renode.io/) | Free, open-source | Full system simulation (CPU, peripherals, network) for firmware testing without hardware. |

## :chart_with_upwards_trend: Logic Analyzers & Signal Tools

| Tool | What's Free | Notes |
|---|---|---|
| [PulseView](https://sigrok.org/wiki/PulseView) (sigrok) | Free, open-source | GUI for cheap USB logic analyzers with UART/SPI/I2C protocol decoders. |
| [Saleae Logic software](https://www.saleae.com/) | Free software | Requires Saleae hardware. |

## :gear: CI / Build / Firmware Testing

| Tool | What's Free | Notes |
|---|---|---|
| [GitHub Actions](https://github.com/features/actions) | 2,000 free CI minutes/month (unlimited on public repos) | Common choice for ESP-IDF and PlatformIO build matrices. |
| [PlatformIO Core](https://platformio.org/) | Free CLI + build system | Multi-board, multi-framework builds without vendor IDE lock-in. |
| [Wokwi CI](https://docs.wokwi.com/vscode/ci-server) | Free tier for CI-triggered simulation | Run simulated hardware-in-the-loop tests in GitHub Actions. |

## :cloud: Free IoT / Cloud Backends

| Service | What's Free | Limits |
|---|---|---|
| [HiveMQ Cloud](https://www.hivemq.com/mqtt-cloud-broker/) | Free MQTT broker tier | 100 device connections, capped throughput. |
| [ThingSpeak](https://thingspeak.com/) | Free tier | 3,000,000 messages/year. |
| [Adafruit IO](https://io.adafruit.com/) | Free tier | Rate-limited; works well with ESP32/Arduino. |
| [Firebase Spark plan](https://firebase.google.com/pricing) | Free tier | Realtime DB + hosting for small device fleets. |

## :satellite: Free Firmware OTA Hosting

| Approach | What's Free | Notes |
|---|---|---|
| GitHub Releases + raw manifest | Free within normal GitHub quotas | Host `firmware.bin` as a release asset and a `version.json` manifest. Device checks the manifest on boot and compares versions. No backend required. |
| [JSONhost](https://jsonhost.com/) (or similar) | Free tier | Stable public GET endpoint for a version manifest if you prefer not to use GitHub raw URLs. |
| ESP-IDF native OTA (self-hosted) | Built into ESP-IDF | HTTPS pull with signed images and partition swap. You run the server. |
| [Golioth](https://golioth.io/) / [Memfault](https://memfault.com/) free tiers | Free tier for small fleets | Staged rollouts, rollback, and fleet observability beyond a simple manifest file. |

> For personal projects, a GitHub Releases manifest is usually enough. For end-user devices, plan for signing and rollback to avoid bricked updates.

## :package: Enclosure & 3D Printing

| Tool | What's Free | Notes |
|---|---|---|
| [FreeCAD](https://www.freecad.org/) | Fully free, open-source | Parametric CAD for enclosures. Steeper learning curve than Fusion, no licensing restrictions. |
| [Fusion 360 Personal Use](https://www.autodesk.com/products/fusion-360/personal) | Free for hobbyist/non-commercial use | Common for maker enclosures. Commercial use requires a paid license. |
| [Onshape Free Tier](https://www.onshape.com/) | Free for public documents | Browser-based collaborative CAD. Free-tier designs are publicly visible. |
| [PrusaSlicer](https://www.prusa3d.com/page/prusaslicer_424/) / [Cura](https://ultimaker.com/software/ultimaker-cura/) | Fully free | Standard slicers for most FDM printers. |
| [Printables](https://www.printables.com/) / [Thingiverse](https://www.thingiverse.com/) | Free STL hosting + library | Check existing models before designing standoffs, DIN rail clips, or battery holders from scratch. |

## :satellite_orbital: RF / Antenna Tools

| Tool | What's Free | Notes |
|---|---|---|
| [NEC2](https://www.nec2.org/) / [4nec2](https://www.qsl.net/4nec2/) | Free, open-source antenna modeling | Wire antenna simulation (gain, impedance, radiation pattern). |
| [openEMS](https://www.openems.de/) | Free, open-source FDTD simulator | 3D EM simulation for PCB antennas and RF structures. Heavier setup than NEC2. |
| [SimSmith](https://www.ae6ty.com/Smith_Charts.html) | Free | Smith chart tool for matching network design. |
| [rtl_433](https://github.com/merbanan/rtl_433) / [GNU Radio](https://www.gnuradio.org/) | Free, open-source | SDR tooling for SubGHz/ISM-band signal decoding and analysis. |

## :mag_right: Component Search & Datasheets

| Tool | What's Free | Notes |
|---|---|---|
| [Octopart](https://octopart.com/) | Free search, no account for basic use | Cross-distributor search (stock, price, datasheets) across DigiKey/Mouser/LCSC. |
| [Findchips](https://www.findchips.com/) | Free | Similar aggregator; useful when Octopart data looks stale. |
| [DigiKey](https://www.digikey.com/) / [Mouser](https://www.mouser.com/) / [LCSC](https://www.lcsc.com/) parametric search | Free | Each distributor's own parametric filters, often more detailed for their stock. |
| [SnapMagic (SnapEDA)](https://www.snapeda.com/) | Free symbols + footprints for millions of parts | Downloadable into KiCad/Altium/Eagle format. |

## :zap: Power Supply & Regulator Design

| Tool | What's Free | Notes |
|---|---|---|
| [TI WEBENCH / Power Designer](https://www.ti.com/design-resources/design-tools-simulation/webench-power-designer.html) | Free, browser-based | Input voltage/current requirements; get ranked TI regulator topologies with schematic and BOM. |
| [Analog Devices ADIsimPower](https://www.analog.com/) | Free | Same category, scoped to ADI regulators. |
| [Battery life / capacity calculators](https://www.digikey.com/en/resources/design-tools) (DigiKey tool hub) | Free | Quick runtime estimates before committing to a battery design. |

## :arrows_counterclockwise: RTOS & Bootloader Frameworks

| Tool | What's Free | Notes |
|---|---|---|
| [FreeRTOS](https://www.freertos.org/) | Free, open-source (MIT) | What ESP-IDF is built on. Direct access to tasks, queues, and semaphores. |
| [Zephyr RTOS](https://www.zephyrproject.org/) | Free, open-source | Broader hardware support than FreeRTOS alone; Linux Foundation-backed. |
| [MCUboot](https://www.mcuboot.com/) | Free, open-source | Secure bootloader for signed, rollback-safe firmware updates. Pairs well with the OTA section above. |

## :white_check_mark: Code Quality, Static Analysis & Testing

| Tool | What's Free | Notes |
|---|---|---|
| [cppcheck](http://cppcheck.sourceforge.net/) | Free, open-source | Static analysis for C/C++: buffer overruns, null derefs, uninitialized reads. |
| [clang-tidy](https://clang.llvm.org/extra/clang-tidy/) | Free, open-source | Deeper static analysis and style checks; integrates with editors and CI. |
| [Unity](https://www.throwtheswitch.org/unity) / [Ceedling](https://www.throwtheswitch.org/ceedling) | Free, open-source | Lightweight C unit testing for embedded; runs on-host or on-target. |
| [PlatformIO Unit Testing](https://docs.platformio.org/en/latest/advanced/unit-testing/index.html) | Free, built into PlatformIO Core | Same test suite on native host and real hardware from one config. |
| [PVS-Studio](https://pvs-studio.com/en/pvs-studio/) free license | Free for open-source projects | Commercial-grade static analyzer; apply if your repo qualifies. |

## :robot: TinyML / Edge AI

| Tool | What's Free | Notes |
|---|---|---|
| [Edge Impulse](https://www.edgeimpulse.com/) | Free for individual developers | Data collect, train, deploy workflow; exports optimized C++ to ESP32/Cortex-M targets. |
| [TensorFlow Lite Micro](https://www.tensorflow.org/lite/microcontrollers) | Free, open-source | Inference runtime used by many TinyML tools; direct control over model size and arena allocation. |
| [CMSIS-NN](https://github.com/ARM-software/CMSIS-NN) | Free, open-source | ARM-optimized NN kernels for Cortex-M. |
| [ESP-DL](https://github.com/espressif/esp-dl) | Free, open-source | Espressif inference library tuned for ESP32-S3 vector instructions. |

## :battery: Power Profiling & Current Measurement

| Tool | What's Free | Notes |
|---|---|---|
| [Nordic Power Profiler Kit II software](https://www.nordicsemi.com/Products/Development-hardware/Power-Profiler-Kit-2) | Free software (~$80 hardware) | Current measurement down to µA for validating deep-sleep claims. |
| [Joulescope UI](https://www.joulescope.com/) | Free software (hardware required) | Wide dynamic range for sleep and active-radio current spikes. |
| [ESP-IDF power management logging](https://docs.espressif.com/) | Built into ESP-IDF | Software-only estimate; not a substitute for real measurement. |

## :package: Parts Inventory & BOM Management

| Tool | What's Free | Notes |
|---|---|---|
| [InvenTree](https://inventree.org/) | Free, open-source, self-hosted | Stock control, BOM management, supplier data, and a [KiCad plugin](https://inventree.org/blog/2023/09/26/kicad) for native symbol libraries. |
| [Ki-nTree](https://github.com/sparkmicro/Ki-nTree) | Free, open-source | Pulls part data from DigiKey/Mouser/LCSC/Element14 and creates InvenTree + KiCad entries in one step. |
| [Part-DB](https://github.com/Part-DB/Part-DB-server) | Free, open-source, self-hosted | Similar scope to InvenTree with KiCad integration. |
| [PartKeepr](https://github.com/partkeepr/PartKeepr) | Free, open-source | Older, simpler option for shared hackerspace inventory. |

## :scales: Wireless Pre-Compliance & Regulatory Lookup

| Tool | What's Free | Notes |
|---|---|---|
| [FCC Table of Frequency Allocations](https://www.fcc.gov/oet/ea/rfdevice) | Free, official | Which bands are allowed for transmission in the US. |
| [FCC ID Search](https://www.fcc.gov/oet/ea/fccid) | Free, official | Look up existing FCC IDs and certified module test filings. |
| [FCC Equipment Authorization guidance](https://www.fcc.gov/oet/ea/rfdevice) | Free, official | SDoC vs full Certification requirements and cost implications. |
| Pre-compliance with a cheap SDR/spectrum analyzer | Free (software side) | Still need RF hardware (e.g. RTL-SDR), but analysis software (GNU Radio) is free. Catches obvious spurious emissions before a paid EMC lab session. |

> These tools help avoid surprises; they do not replace an accredited test lab before selling a product with a radio.

## :arrows_clockwise: Hardware Version Control & Collaboration

| Tool | What's Free | Notes |
|---|---|---|
| [Git](https://git-scm.com/) + [GitHub](https://github.com/) free tier | Free | KiCad projects are plain text, so standard git diffs and PRs work for hardware too. |
| [KiCad's built-in git integration](https://www.kicad.org/) | Built into KiCad 7+ | Project history and diffing inside the KiCad GUI. |
| [OSHWLab](https://oshwlab.com/) | Free project hosting | EasyEDA's public, forkable hardware project platform. |

## :books: Free Courses & Learning

| Resource | What's Free | Notes |
|---|---|---|
| [HarvardX TinyML EdX course](https://www.edx.org/) | Free to audit | Intro course; pairs with the Arduino Tiny Machine Learning Kit. |
| [Espressif's official ESP-IDF Programming Guide](https://docs.espressif.com/) | Free, official | Authoritative ESP32 documentation. |
| [KiCad official documentation + forum](https://forum.kicad.info/) | Free | Active community; search before posting. |
| [Interrupt (Memfault's blog)](https://interrupt.memfault.com/) | Free | Practical firmware engineering articles on debugging, OTA, and power profiling. |

## :gift: Component Sourcing & Free Samples

| Source | What's Free | Notes |
|---|---|---|
| [TI Sample Program](https://www.ti.com/) | Free samples, small qty | Business/edu email speeds approval but is not required. |
| [Analog Devices Samples](https://www.analog.com/) | Free samples | Similar process to TI. |
| [Microchip Samples](https://www.microchip.com/) | Free samples | Similar process to TI. |
| [JLCPCB new-user credit](https://jlcpcb.com/) | Varies monthly | Check current promo before ordering. |

---

## :handshake: Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). One row per tool, keep the "what's free" column honest, and note real limits.

## Disclaimer

Free tiers, pricing, and limits change without notice. Verify current terms on the provider's site before relying on anything for production. This list excludes anything that is not a legitimate offering (e.g. abusing trial accounts or violating ToS).

## License

MIT. See [LICENSE](LICENSE).

---

Found something outdated or missing? [Open an issue](https://github.com/cifertech/free-embedded-dev-tools/issues).

## Contact

- Patreon: [patreon.com/cifertech](https://www.patreon.com/cifertech)
- Twitter: [@techcifer](https://twitter.com/techcifer)
- Email: CiferTech@gmail.com
- Repo: [github.com/cifertech/free-embedded-dev-tools](https://github.com/cifertech/free-embedded-dev-tools)
