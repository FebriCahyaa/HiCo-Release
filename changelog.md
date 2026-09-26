# HiCo Thermal Changelog

## HiCo Thermal v1.2.0

#### 🐛 Bug Fixes

- **device:** detect HyperOS by its MIUI UI code and name custom ROMs (`2c5baaa`)

#### 📝 Other Changes

- avoid GCC 13 -Wrestrict false positive in Release builds (`d6d4094`)
- match the per-device tuning table columns (`d9ae1c5`)
- ROM detection: custom ROMs on Xiaomi vendors are not HyperOS (`280968a`)
- Safety guard: release per tripped sensor, graduated protection, stop HAL loop (`163bf63`)
- Per-device thermal templates for the Xiaomi database (`d9d69f8`)
- mi_thermald verifier: check caps only on raised sections; keep no decrypted copies (`3ed2440`)
- Encrypted mi_thermald configs and per-device thermal templates (`791fd4e`)
- Extreme mode, thermal overclock, templates, Vue WebUI; find devices on custom ROMs (`69728cb`)



## HiCo Thermal v1.1.1

#### ✨ Features

- **devices:** update Xiaomi / Redmi / POCO device profiles (212 devices) (`513f7c0`)

#### 📝 Other Changes

- check the public release repository before building (`677232d`)
- devices workflow: scan Redmi and POCO groups too (`0187f0e`)
- Real-time throttling monitor (hicod monitor + WebUI Monitor tab) (`f4e2028`)
- Redesign the WebUI: tabs, gauges, Flux game list, EN/ID (`1f78302`)



## HiCo Thermal v1.0.1

#### ✨ Features

- chipset thermal tuner, relaxed level, whitelist and blacklist (`feca641`)
- **devices:** keep vendor thermal files and cover Redmi, POCO and pre-Treble dumps (`48f9ba9`)
- **devices:** update Xiaomi device profiles (134 devices) (`eda3b3e`)
- thermal framework with a compiled Xiaomi device database (`eaa475f`)
- **devices:** sparse clone mode for the Xiaomi dump scanner (`7baa09d`)
- private licensing, bilingual EULA and public update channel (`e769bef`)
- **devices:** Xiaomi device profiles from stock firmware dumps (`3edae0c`)
- HiCo Thermal, automatic thermal unlock for Flux games (`1f3237e`)

#### 🐛 Bug Fixes

- **devices:** push each scan to its own branch (`2d7b6c0`)
- **devices:** gaps found by the first real scan of the Xiaomi dumps (`bd62dd8`)
- **ci:** commit the build-module action ignored by .gitignore (`a3e6e78`)

#### 🧹 Maintenance

- drop committed Python cache and ignore it (`ea86d41`)
- initialize repository (`420884e`)

#### 📝 Other Changes

- AOSP ROM support and separate 64-bit / 32-bit builds (`623f39e`)

