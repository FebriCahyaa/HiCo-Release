# HiCo Thermal Changelog

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

