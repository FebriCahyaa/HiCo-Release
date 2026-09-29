# HiCo Thermal Changelog

## HiCo Thermal v1.4.0

#### ✨ Features

- **webui:** About as HiCo's identity, system and trust page (`6334fd7`)
- **webui:** native diagnostic screen for Log (`67d81da`)
- **webui:** Android-system-settings layout for Settings and Advanced (`c9ed0cc`)
- **webui:** native-feeling Scenarios and Presets controls (`7bd05c6`)
- **webui:** thermal monitor as the primary native-utility screen (`ad582a9`)
- **webui:** floating glass navigation and hero temperature readout (`a87cf45`)

#### 🐛 Bug Fixes

- **tests:** update stale mapping-matrix artifact name assertion (`32f811e`)
- **ci:** stop full-mapping merge job from corrupting shard JSON (`1e79f04`)
- **tests:** use correct vendor subdirectory path for stale-table check (`654ed47`)
- **ci:** regenerate WebUI integrity manifest after native-evolution changes (`58cc121`)
- **tests:** update stale generated_from() assertion for multi-vendor db (`5d397e1`)
- **ingest:** rom-vendor-blobs ignored --jobs, always ran 32 parallel probes (`d01c20f`)
- **seed:** correct exit-code capture for sparse_fetch.py failures (`7e05e6e`)
- **webui:** global consistency pass across all redesigned screens (`8ade2f1`)

#### 🧹 Maintenance

- ignore tools/seed_local.sh run logs (`a93ff3d`)

#### 📝 Other Changes

- **2026-09-29-run3:** fetch delta from upstream (`2902262`)
- remap HiCo thermal database (`d7594a7`)
- **seed:** fetch batch thermal files (`57a8a8e`)
- add seed_local.sh — complete one-time local seed script (`6b965b0`)
- tadiphone is public — no token needed, fix fallback bug (`f6633f8`)
- multi-vendor OEM dumps, ROM-gating filter, multi-branch fetch (`253eade`)
- expand to multi-vendor — Samsung, OnePlus, OPPO, Realme, Motorola, Google (`5664cb0`)
- provision production integrity key (`160e329`)



## HiCo Thermal v1.3.0

#### ✨ Features

- **ingest:** local-seed + delta-only ingest pipeline (`2bad6da`)
- **sources:** expand ingest coverage to 16 Custom ROMs + 3 OEM dumps (`df71304`)
- **evidence:** phase 2.6a deterministic evidence parsers (`4f19498`)
- **evidence:** add rich canonical evidence resolver (`bde40e7`)
- **evidence:** add canonical relationship evidence layer (`518fcee`)
- **relationships:** add universal source relationship graph (`c354e23`)
- **collector:** gate sync with thermal candidates (`71140db`)
- **filter:** add universal thermal candidate filter (`4de821c`)
- **discovery:** add universal repository discovery and safe merge (`9b42137`)
- **schema:** add universal device rom thermal model (`c0516aa`)
- **ci:** add optional AWS CodeBuild offload for thermal ingestion (`80c949c`)
- **database:** add original-versus-candidate thermal tables (`4914af4`)
- **database:** add multi-source thermal ingestion and mapping (`66afb58`)
- **tools:** add generic thermal codec and unpack pipeline (`187023a`)

#### 🐛 Bug Fixes

- remove -mfpu= flag from arm64-v8a build flags (`e8bab73`)
- skip non-dict JSON files in merge_mappings (`06e4ce4`)
- **database:** archive ingest shards before artifact upload (`f1bb73c`)
- **aws:** allow CloudFormation to read role inline policies (`de00f65`)
- **ci:** align AWS OIDC and CodeBuild batch limits (`d54b3e7`)
- **ci:** remove device-specific thermal test dependency (`d04f41a`)
- **ci:** use the actual CMake host binary path in database preflight (`f4357f0`)
- **ci:** refresh WebUI integrity baseline (`9f3edd2`)
- **ci:** harden thermal matrix execution and artifact handoff (`a15ad70`)
- **ci:** keep ingestion matrix output within GitHub limits (`31a47c7`)
- **ci:** refresh WebUI integrity manifest (`2fbaacc`)

#### ♻️ Refactoring

- **thermal:** switch to local collection and HiCo generation (`f92111e`)
- **monitor:** make live monitoring thermal-only (`9688e46`)

#### 📚 Documentation

- document thermal database architecture and provenance (`b644103`)

#### 📦 Build & Dependencies

- ARM64/ARMv7 architecture tuning flags + O3 + linker ICF (`785fa13`)

#### 🔧 CI

- **evidence:** add coverage audit for multi-OEM pilot (`354fcda`)
- **evidence:** add multi-OEM evidence pilot (`7d8f578`)
- **evidence:** verify canonical source relationships (`4decaa9`)
- diagnose GitHub OIDC claims (`e8aef70`)
- **aws:** move infrastructure deployment to GitHub Actions (`6f77cdb`)
- **release:** build the thermal Monitor WebUI in release packages (`1b81dd3`)
- replace Xiaomi-only device workflow with unified pipelines (`070e673`)

#### 🧹 Maintenance

- **repo:** introduce two-zone layout — stock/ (input) and generated/ (derived) (`7bea9d7`)

#### 📝 Other Changes

- Tamper detection: signed releases, runtime self-check, revocation list (`2af50b2`)
- **2026-09-28-run2:** fetch delta from upstream (`2b3b4ff`)
- ROM org vendor blobs and MediaTek thermal policies (`fe49b71`)
- Thermal per scenario and a thermal-focused WebUI (`07b83f0`)
- seed custom-ROM device trees and TheMuppets thermal blobs (`206c2d6`)
- delta-only pipeline that works, vendor blobs, Daily preset (`d81142e`)
- Ingest thermal from LineageOS device trees + TheMuppets vendor blobs (`7389df9`)
- Daily preset, thermal coverage roadmap, ingest scaffolding (`f82d8f8`)
- seed normalized thermal database from repository records (`43330ae`)



## HiCo Thermal v1.2.2

#### 📝 Other Changes

- shorter device line, one line per relax (`94075a6`)
- heavy throttling only for real caps; say when the caps are vendor's (`15b23cb`)



## HiCo Thermal v1.2.1

#### 📝 Other Changes

- Max level only with headroom below the safety limits (`4514ae1`)
- save the log to Download (`23fd1e6`)



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

