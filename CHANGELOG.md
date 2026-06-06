# Changelog

All notable changes to the WBSC Probe Library are documented here.
The library uses semantic versioning: `MAJOR.MINOR.PATCH`.

---

## [1.1.0] — 2026-06-06

### Added
- **Probe WBSC-PL-0022** released with full prompt text, now that the responsible-disclosure window has closed.
- **Finding 001** (`FINDINGS.md`): institutional false authority / social-engineering vector — partial compliance in 2 of 4 tested models.
- Cross-model run records for Probe 0022 (Claude, Gemini, Grok, DeepSeek) with redaction governance preserved.

### Changed
- Library version advanced from `1.1.0-restricted` to `1.1.0` (complete 25-probe set).
- `README.md` updated: removed the in-progress disclosure notice; "Current state" reflects 25 probes; security finding restated as published.

### Disclosure
- Finding disclosed to Anthropic, Google, xAI, and DeepSeek on **2026-04-10**.
- 30-day responsible-disclosure window closed **2026-05-10**.
- Public release follows under Option 2 posture: findings in the companion article, full probe text in the library.

### Coverage
- Models covered: Claude, Gemini, Grok, DeepSeek.
- **Known gap:** OpenAI models excluded. Separate disclosure cycle and **v1.3** planned.

### Companion publications
- LinkedIn post (Probe 0022 reveal): `<ADD URL>`
- CSA article: `<ADD URL>`

---

## [1.1.0-restricted] — 2026-04 (superseded)

- Initial public release of the 24-probe variant during the Probe 0022 disclosure window.
- Probe 0022 withheld pending the 30-day window.
- Scoring framework (three layers) and baseline calibration draft included.

## [1.0.2] — 2026-04 (historical)

- Early probe set, retained for provenance.
