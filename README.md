# FlexiCure

**A non-insertable, two-part wearable that senses abdominal muscle tension and responds with heat.**
Team FLEXICURE, PrintoCent InnoFest 2026 (Oulu, Finland). Winner of the Attitude Prize.

> Status: concept stage. Nothing here has been bench-tested or clinically validated. See [Limitations](#limitations).

## The idea in one paragraph

Menstrual cramping and everyday abdominal muscle tension are managed by guesswork: a heat wrap or a painkiller applied on a hunch, with no signal for when tension builds or whether it helped. FlexiCure senses first, then warms automatically, and learns each user's pattern from one-tap comfort logging.

## Two-part hardware

| Part | What it is | Key specs (design targets) |
| --- | --- | --- |
| **Electronics module ("puck")** | Reusable, rechargeable | About 25 x 20 x 4 mm, under 3 g. Hybrid analog front end (AFE, the chip that reads tiny body signals), Bluetooth Low Energy (BLE) radio, battery. Target: 7 days of sensing per charge. |
| **Attachable part ("patch")** | Disposable, replaced every 2-4 days | 80 x 50 mm, 0.3-0.5 mm thick. Printed Ag/AgCl (silver / silver chloride) electrodes, strain layer, thin-film resistive heater, skin adhesive, and its own single-use cell for the heater only. |

Why the split: sensing needs roughly 150-200 microwatts, while one heat session needs 0.5-1 watt for 10-15 minutes. A single heat session can use more energy than a week of sensing, so heater power is kept off the module's battery. These are estimates, not measurements.

## How it works

- **Sense:** EMG (electromyography, muscle electrical activity), GSR (galvanic skin response, skin conductance) and strain, worn on the lower abdomen. The method builds on electrohysterography (EHG), a non-invasive technique used clinically for uterine monitoring. EHG detected about 94% of contractions versus about 54% for tocodynamometry in a 2026 study (Sensors 2026, 26(15), 4669).
- **Respond:** heat at about 40 C (skin injury threshold is about 44 C). A randomized, double-blind, placebo-controlled trial (Machado et al. 2019, 88 participants) found thermotherapy beat TENS and placebo for menstrual pain.
- **Respond+:** optional compatibility with third-party Bluetooth heat or vibration devices. FlexiCure deliberately builds in no electrical stimulation, because TENS (transcutaneous electrical nerve stimulation) is a regulated device (FDA Class II).
- **App:** Comfort Check (tap Easy / Manageable / Hard / Severe), Period Log, Comfort Forecast, Adaptive Comfort Engine (personalised heat thresholds), live signals, manual heat, patch status.

## Business model

Razor and blades: sell the module once, patches repeatedly. Planning estimates only: module COGS (cost of goods sold) EUR 8-14, patch COGS EUR 2-3.50, proposed module price EUR 39-49 (not locked), patch 3-pack about EUR 15 per month. Comparable devices: Elvie EUR 149-199, Perifit EUR 99-149.

## Repository map

| Path | Contents |
| --- | --- |
| [`docs/case-study.md`](docs/case-study.md) | Full case study and technical report (Markdown) |
| [`docs/FlexiCure_Case_Study.docx`](docs/FlexiCure_Case_Study.docx) | Same report as a Word file, 13 pages |
| [`slides/FlexiCure_Deck.pptx`](slides/FlexiCure_Deck.pptx) | 13-slide pitch deck with speaker notes |
| [`slides/deck-text.md`](slides/deck-text.md) | Text and notes of the deck, readable on GitHub |
| [`docs/pitch-script.md`](docs/pitch-script.md) | 3-minute Day-1 and 1-minute Day-2 pitch scripts |
| [`docs/qa-prep-sheet.md`](docs/qa-prep-sheet.md) | 20 hard judge questions with honest answers |
| [`research/references.md`](research/references.md) | Verified sources and what each supports |
| [`research/open-questions.md`](research/open-questions.md) | Unresolved engineering and business questions |

## Limitations

- The 7-day battery life is a design target. It has not been bench-engineered.
- The Adaptive Comfort Engine and the EHG-to-cramp link at the skin surface are unvalidated.
- Adhesive wear, skin irritation, heater thermal safety and the module-to-patch connector are untested.
- Prices are planning estimates; no supplier quotes exist.
- No IP filed. No regulatory strategy done. The product is framed as a wellness device, not a diagnostic one.

## Glossary

AFE: analog front end. BLE: Bluetooth Low Energy. COGS: cost of goods sold. EHG: electrohysterography. EMG: electromyography. GSR: galvanic skin response. NSAID: non-steroidal anti-inflammatory drug (for example ibuprofen). TENS: transcutaneous electrical nerve stimulation. The case study has the full glossary.

## License

No license chosen yet. Until one is added, all rights are reserved by the authors. Add a `LICENSE` file before making the repo public if you want others to reuse it.
