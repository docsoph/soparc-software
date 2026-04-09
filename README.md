# SOPARC Dual-Video Coding Tool

**System for Observing Play and Recreation in Communities — Dual-Video Adaptation**

An open-source adaptation of the validated SOPARC observation protocol designed for use with dual-angle CCTV or video footage. Includes a browser-based coding tool and a printable manual observation form.

---

## Background

SOPARC (McKenzie et al., 2006; ) is a validated system for momentary time-sampling observation of physical activity in community spaces. This adaptation extends the original protocol to support:

- **Dual-video / dual-camera coding** — simultaneously code two angles of the same target area
- **Video synchronisation** — align two footage sources to a shared reference timestamp
- **Dwell time measurement** — log entry and exit timestamps for each individual to calculate how long they used the space
- **Structured data export** — CSV output compatible with Excel, SPSS, R, and other statistical packages

This tool was developed for the *More Sport Their Way* Research Project at Edith Cowan University (ECU), approved under HREC 2023-04756-PENNEY.

---

## Files in this repository

| File | Description |
|------|-------------|
| `soparc_app.html` | Self-contained browser coding tool (no installation required) |
| `soparc_protocol_form_v1.0.docx` | Printable landscape A4 manual coding form |
| `README.md` | This file |
| `CITATION.cff` | Machine-readable citation file for the software |
| `LICENSE` | MIT Licence |

---

## Quick start — browser coding tool

1. Download or clone this repository.
2. Open `soparc_app.html` in any modern web browser (Chrome, Firefox, Edge, Safari).
3. No internet connection or installation is required — the file is fully self-contained.

### Workflow

1. **Load Videos** — click each file input to select Video A and Video B from your computer.
2. **Sync Videos** — play both videos to a shared reference event (e.g., a clock appearing on screen, or a clap). Click **📌 Set Sync** under each video at the matching moment. The tool calculates the offset automatically. Use **▶ Play Both (synced)** to confirm alignment.
3. **Complete the Context tab** — record environmental descriptors once per session (visibility, accessibility, safety, social environment, etc.).
4. **Code persons** — for each individual observed, use **▶ Entry** and **■ Exit** under the relevant video to capture timestamps, then complete gender, age, intensity, and activity fields. Click **+ Add**.
5. **Export** — go to the Export tab to download session/context and observation CSVs.

### Timestamp normalisation

When sync is active, Entry/Exit timestamps captured from Video B are automatically adjusted to the Video A timeline (i.e., all timestamps in the exported data are on a single shared scale).

---

## Observation variables

### Session / Context (recorded once per session)

| Category | Variable | Response options |
|----------|----------|-----------------|
| Session | Temperature | Free text (°C) |
| | Shade | Predominantly shade / Shade-sun mix / Predominantly sun |
| | Observation Start | HH:MM:SS |
| | Observation Stop | HH:MM:SS |
| Area Information | Visibility | Poor / Partially Restricted / Good |
| | Facility type & equipment | Court / Field / Open Space / Playground / Other |
| | Facility/equipment condition | Good / Fair / Poor |
| | Accessible | Good / Fair / Poor |
| Safety & Comfort | Adult role present | Not present / Staff / Parent or caregiver |
| | Lighting | Adequate / Dim / Poor / Natural |
| | Perceived safety | Safe / Moderate / Unsafe |
| | Parking proximity | Adjacent / Near / Far / None |
| | Toilet facility accessibility | Accessible / Nearby / Distant / None |
| | Cleanliness | Clean / Moderate / Poor |
| | Signage pertaining to use | Clear / Somewhat Clear / None |
| Social & Cultural | Peers / role models present | Yes / No / Unclear |
| | Cultural signage / cues | Clear / Somewhat Clear / None |
| | Inclusivity | Inclusive / Partially Inclusive / Exclusive / Unclear |

### Individual observation (recorded per person)

| Variable | Description |
|----------|-------------|
| Number | Count of individuals sharing identical characteristics |
| Video | Which camera angle (A / B / Both) |
| Entry timestamp | HH:MM:SS from video timeline |
| Exit timestamp | HH:MM:SS from video timeline |
| Dwell time | Calculated automatically (Exit − Entry) |
| Gender | Women / Girls (F) / Men / Boys (M) / Non-binary or Unclear (N) |
| Age group | Child / Teen / Adult / Senior |
| Race / Ethnicity | Aboriginal or Torres Strait Islander (ATSI) / White/Anglo-Australian (W/A) / Asian / Other or Unsure |
| Activity type | Organised / Informal / Play / Other |
| Activity / sport | Free text (e.g. "Basketball", "Walking") |
| Intensity | Sedentary (Sed) / Moderate (Mod) / Vigorous (Vig) |
| Notes | Optional free text |

Activity intensity definitions follow SOPARC conventions (McKenzie et al., 2006):
- **Sedentary (Sed)** — lying down, sitting, or standing still
- **Moderate (Mod)** — walking at any speed or light activity
- **Vigorous (Vig)** — any activity more intense than walking (running, jumping, active sport)

---

## Ethics and data use

This coding tool does not collect, store, or transmit any data outside your computer. All data remains in your browser session and is only saved when you click an Export button.

**If you are collecting data from CCTV footage in a public space**, it is your responsibility to ensure appropriate ethics approval, signage, and informed consent procedures are in place. Example signage text is provided in the protocol document.

---

## Citation

### SOPARC protocols and coding forms

McKenzie TL, Cohen DA, Sehgal A, Williamson S, Golinelli D. System for Observing Play and Recreation in Communities (SOPARC): Reliability and Feasibility Measures. *J Phys Act Health.* 2006;3(Suppl 1):S208–S222. PMID: 20976027; PMCID: PMC2957838.
Marquet, O., Hipp, J. A., Alberico, C., et. al. (2019). Use of SOPARC to assess physical activity in parks: Do race/ethnicity, contextual conditions, and settings of the target area, affect reliability? *BMC Public Health.* 2019;19(1):1730-1744. PMID: 31870351; PMCID: PMC6929368.

### This software

Nimphius, S. (2026). *SOPARC Dual-Video Coding Tool* [Open-source software]. More Sport Their Way Research Project, Edith Cowan University. https://github.com/docsoph/soparc-software. https://doi.org/10.5281/zenodo.19484775

A `CITATION.cff` file is included for automated citation support in GitHub and Zenodo.

---

## Acknowledgements

- Developed as part of the *More Sport Their Way* Research Project, Edith Cowan University (HREC 2023-04756-PENNEY).
- SOPARC protocol adapted from McKenzie et al. (2006) and CC-BY-4.0 template in Marquet et al. (2019).
- **Funding:** Penney, D. et al. *More Sport, Their Way! Promoting women's informal sport participation in WA.* Healthway (WA Health Promotion Foundation), Health Promotion Research – Exploratory Research Grants, 2024–2026.
- **AI Assistance:** Software developed with assistance from Claude Sonnet 4.6 (Anthropic, 2025).

---

## Licence

MIT Licence — free to use, adapt, and redistribute with attribution. See `LICENSE` for full terms.
