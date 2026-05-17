# WBSC-PL Release Checklist

Reusable checklist for every WBSC-PL release. Copy the relevant sections into a GitHub Issue per release (e.g. "v1.2 release checklist"), tick as you go, close when done.

The checklist is conservative by design. Skipping items is a governance decision, not a default.

---

## Pre-release — content

- [ ] All new/modified probes have `status`, `probe_type`, `wbsc_field`, and `notes` fields populated
- [ ] All run records have raw response + SHA-256 hash + signal type + rater identity
- [ ] Run records for security-relevant probes have boundary descriptions and approach-to-limit phrasing **redacted** per governance note
- [ ] Any probe that produced a confirmed security finding has been through responsible disclosure (30-day window closed) before inclusion
- [ ] Cross-model results are consistent with the test_results block in each probe entry
- [ ] No probe in the release is designed to produce a predetermined result favourable to any AI developer

## Pre-release — documentation

- [ ] `CHANGELOG.md` updated with version, date, scope of changes, known coverage gaps
- [ ] `README.md` reviewed for accuracy: probe count, field coverage, model coverage, version references
- [ ] `README.md` includes the methodology bridge line ("treats prompts as structured elicitation instruments")
- [ ] `CONTRIBUTING.md` reviewed; disclosure-first rule restated if any new finding categories were added
- [ ] `FINDINGS.md` updated with any new confirmed findings (one section per finding, with disclosure dates and companion article links)
- [ ] Citation block in `README.md` reflects the new version

## Pre-release — governance

- [ ] Responsible disclosure status confirmed for every security-relevant probe in the release
- [ ] Coverage gaps named explicitly (e.g. "OpenAI excluded, v1.X planned")
- [ ] Rater-not-equal-to-system-under-test rule held across all run records
- [ ] CC0 licence file present and unchanged

## Release

- [ ] Companion LinkedIn article (or other primary venue) scheduled or published — capture URL
- [ ] Tag the release in Git (`vX.Y.Z`)
- [ ] GitHub release notes link to: CHANGELOG entry, companion article, prior version
- [ ] README top banner updated **after** companion article publishes, not before
- [ ] CSA / academic / external venue companion pieces noted as forthcoming if applicable

## Post-release

- [ ] Companion article links added to FINDINGS.md entries
- [ ] Tracker (private) updated: release closed, next-version backlog opened
- [ ] One-week check: any disclosure responses received from developers? Log and acknowledge
- [ ] One-month check: probe results being cited or replicated externally? Note for ArXiv / FAccT track

---

*Last reviewed: [date]. Maintainer: [name]. CC0.*
