**FlexiCure**

*A Non-Insertable Wearable for Abdominal Muscle Tension and Comfort*

A Case Study and Technical Report

**Team FLEXICURE**

PrintoCent InnoFest 2026 · Oulu, Finland · 17-18 September 2026

*Prepared for the PrintoCent InnoFest business case and jury review*

Abstract

Menstrual cramping and everyday abdominal muscle tension are, for most women, managed by guesswork: over-the-counter heat wraps and painkillers applied on a hunch, with no objective signal for when tension is actually building or whether a given intervention helped. This report documents FlexiCure, a non-insertable wearable developed by Team FLEXICURE for the PrintoCent InnoFest 2026 innovation competition, designed to sense abdominal muscle tension directly and respond automatically with heat. FlexiCure uses a two-part hardware architecture: a small, rechargeable electronics module, worn continuously and lasting seven days per charge, and a low-cost, disposable attachable part, replaced regularly, that carries the printed sensing electrodes, the heating element, and the skin adhesive. The sensing approach, abdominal surface electromyography, is grounded in electrohysterography, an established, non-invasive clinical technique already used to monitor uterine muscle activity from the skin surface. This report documents the physiological and engineering theory behind the sensing and actuation layers, the two-part hardware and power architecture, the companion application's adaptive comfort-logging design, the business case, the differentiation from the existing pelvic-wellness device market, and the limitations and validation work that remain outstanding.

1\. Introduction

PrintoCent InnoFest is an annual innovation competition organized by the PrintoCent industry cluster, coordinated by VTT Technical Research Centre of Finland together with the University of Oulu, Oulu University of Applied Sciences (OAMK), and BusinessOulu. The competition challenges teams to develop a business case around Printed Intelligence, the use of printed, flexible electronic components to extend the functionality of everyday materials and surfaces beyond conventional rigid electronics.

This report documents FlexiCure, the concept developed by Team FLEXICURE for InnoFest 2026. The concept was developed iteratively: early versions explored a broader set of clinical applications, including wound recovery and joint mobility, and considered whether continuous sensing could support earlier detection of underlying gynecological conditions. Over the course of development, the team deliberately narrowed and repositioned the concept twice. First, toward a single, well-scoped application: women's abdominal muscle tension and menstrual comfort. Second, away from a medical or diagnostic framing entirely, toward a general consumer wellness product, on the reasoning that a non-medical wellness device avoids the regulatory and validation burden of a diagnostic claim while still addressing a real, everyday, underserved need.

The purpose of this report is to document, in one place, the theoretical and engineering grounding for each design decision, the two-part hardware architecture, the business case, and, in the interest of intellectual honesty, the aspects of the concept that remain unvalidated hypotheses rather than demonstrated results.

2\. Problem Statement

The problem statement follows the four-question business case framework taught during the InnoFest kickoff session: what is the problem, whose problem is it, how is it solved today, and why is the proposed solution better.

2.1 What Is the Problem

Abdominal muscle tension and menstrual cramping are managed almost entirely by guesswork. A person applies a heat wrap or takes a painkiller based on how they feel in the moment, with no objective signal for when tension is actually building, how severe it is relative to their own baseline, or whether a given intervention actually helped. This is a genuinely common, everyday experience, not a rare clinical scenario.

2.2 Whose Problem It Is

The direct beneficiaries are women managing menstrual cramping or general abdominal muscle tension, a broad, everyday population rather than a narrow clinical one. A relevant early-adopter segment is women who already purchase pelvic wellness devices, such as Elvie or Perifit, but who find an insertable device uncomfortable or unappealing.

2.3 How It Is Solved Today

Existing approaches fall into two categories, and neither senses anything. The first is manual, open-loop self-care: heat wraps, heating pads, and over-the-counter analgesics, applied entirely on the user's own judgment, with no sensing layer at all. The second is the pelvic wellness device category, led by products such as Elvie Trainer and Perifit, which do include sensing and a companion application, but are built around a fundamentally different job: gamified Kegel exercise and pelvic floor strengthening, delivered through an internally-inserted probe. None of these existing options sense abdominal muscle tension directly or respond to it automatically.

2.4 Why the Proposed Solution Is Better

FlexiCure senses abdominal muscle tension directly, using surface electromyography, and closes the loop with an automatic heat response, without requiring insertion. It addresses a different muscle group and a different job (tension and comfort, not exercise and strengthening) than the existing pelvic wellness device category, while remaining accessible to the same buyer through the same purchase channel.

3\. Related Work and Competitive Context

3.1 The Existing Pelvic Wellness Device Market

The most relevant existing market is the pelvic floor device category, a real, sized, and growing consumer market. Industry market research estimates this category at approximately USD 892.4 million in 2026, projected to grow to approximately USD 1.89 billion by 2035, a compound annual growth rate of roughly 8.7 percent. Named, funded competitors include Elvie Trainer (priced roughly EUR 149 to 199), Perifit (roughly EUR 99 to 149), and kGoal, all of which are insertable, app-connected biofeedback devices built around gamified pelvic floor exercise. A smaller number of products, such as ELITONE, are external and non-insertable, but rely on electrical stimulation alone, with no sensing layer.

3.2 Why Insertable Devices Cannot Do What FlexiCure Does

The insertable design of Elvie, Perifit, and kGoal is not an arbitrary product choice; it reflects a real anatomical constraint. The pelvic floor muscles sit deep within the pelvis, at its base, and their electrical activity cannot be read with useful signal quality from the skin surface. Reaching them requires internal placement. FlexiCure does not attempt to solve the same sensing problem non-invasively; it senses a different, externally-accessible muscle group and physiological signal entirely, described in Section 4.1.

3.3 Competitive Positioning

|                         |                      |                 |                                  |
|-------------------------|----------------------|-----------------|----------------------------------|
| **Solution**            | **Senses Anything?** | **Insertable?** | **Job**                          |
| Heat wrap / painkiller  | No                   | No              | Manual relief, no sensing        |
| Period-tracking app     | No                   | No              | Calendar logging only            |
| Elvie / Perifit / kGoal | Yes (pelvic floor)   | Yes             | Exercise and strengthening       |
| ELITONE                 | No                   | No              | Electrical stimulation only      |
| FlexiCure (proposed)    | Yes (abdominal wall) | No              | Sense tension, respond with heat |

*Table 0. Comparative positioning of FlexiCure against existing alternatives.*

This comparison makes explicit what distinguishes FlexiCure: it is the only option that both senses a physiological signal and requires no insertion, and it is solving a different problem (tension and comfort) than the exercise-and-strengthening job the entire insertable-device category is built around.

4\. Theoretical and Scientific Foundations

4.1 Electrohysterography and Abdominal Surface Sensing

FlexiCure's core sensing principle rests on electrohysterography (EHG), an established, non-invasive clinical technique. Functionally, EHG is a surface electromyogram of the uterus: adhesive Ag/AgCl electrodes are placed on the abdomen, overlying the uterus, and record the summated electrical activity of the myometrium (uterine muscle) as it is transmitted through the abdominal wall. EHG is already used clinically to monitor uterine contractions, most commonly during labor, and has been shown to substantially outperform older external methods: surface EHG detects approximately 94 percent of contractions confirmed by an invasive intrauterine pressure catheter reference, compared with approximately 54 percent for conventional external tocodynamometry.

There is direct precedent for a wearable patch built around this exact principle. Jo and colleagues (Korea Electronics Technology Institute, 2018) developed an abdomen-attachable uterine EMG acquisition patch measuring approximately 43 by 36 millimeters, closely comparable to FlexiCure's own target footprint. On the commercial side, the Monica AN24, a wireless multi-electrode abdominal patch, is already used clinically to record uterine electrical activity. FlexiCure applies this same, already-validated sensing principle to a different, non-obstetric use case: everyday menstrual and abdominal muscle tension rather than labor monitoring.

4.2 Physiological Sensing Theory

4.2.1 Surface Electromyography (EMG)

Surface electromyography measures the electrical activity generated by muscle fiber contraction, detected non-invasively through electrodes placed on the skin above the muscle of interest. In FlexiCure's case, printed Ag/AgCl electrodes positioned over the lower abdomen capture electrical activity associated with uterine and abdominal wall muscle contraction, the same physiological signal read in clinical electrohysterography.

4.2.2 Galvanic Skin Response (GSR)

Galvanic skin response, also called electrodermal activity, measures the electrical conductance of the skin, which varies with the moisture produced by eccrine sweat glands under sympathetic nervous system control. Because sweat gland activity is governed by the autonomic nervous system rather than voluntary control, GSR is a well-established, objective proxy for autonomic arousal and stress-linked physiological activation.

4.2.3 Piezoresistive Strain Sensing

Piezoresistive sensing exploits a printed conductive ink whose electrical resistance changes measurably under mechanical deformation. Printed as a thin, flexible trace and bonded to the attachable part, the sensor's resistance tracks abdominal wall expansion and contraction, and is used primarily as a cross-check against the EMG channel to reject motion artifact, such as ordinary movement or posture change, that might otherwise be mistaken for a genuine tension event.

4.3 Thermotherapy: The Basis for FlexiCure Respond

FlexiCure Respond, the platform's heat-response layer, is based on superficial heat therapy, a long-established non-pharmacological pain-management technique. The proposed mechanism of action operates through two pathways: improved local blood circulation, and modulation of pain signal transmission at the level of the central nervous system (the gate-control mechanism, by which a non-painful thermal stimulus can reduce the perceived intensity of pain signals).

Clinical evidence supports this mechanism specifically for menstrual cramping. A systematic review and meta-analysis published in Scientific Reports found that heat therapy produced pain relief comparable to analgesic medication and superior to no treatment. More recent meta-analyses, drawing on a larger evidence base of 25 randomized controlled trials and 2,393 participants, report that heat therapy reduces menstrual pain intensity with efficacy comparable to non-steroidal anti-inflammatory drugs, while offering a more favorable safety profile.

A related, distinct relief mechanism, vibration, has separate clinical grounding worth noting as a documented alternative: gate control theory, first proposed by Melzack and Wall in 1965, holds that vibration activates large-diameter nerve fibers that inhibit pain signal transmission at the spinal cord. This is the basis for FlexiCure's optional compatibility with existing third-party vibration devices, described in Section 5.4.

4.4 Glossary of Terms and Abbreviations

This glossary collects every technical term and abbreviation used in this report, for a reader unfamiliar with printed electronics or biomedical sensing. Each term is also defined at its first use in the running text.

|                                |                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Term**                       | **Definition**                                                                                                                                                          |
| EMG                            | Electromyography - electrical activity produced by muscle contraction, read via skin-surface electrodes.                                                                |
| EHG                            | Electrohysterography - the clinical term for surface EMG of the uterus, read from the abdomen.                                                                          |
| GSR                            | Galvanic Skin Response, also called electrodermal activity - skin conductance change caused by sweat gland activity, a proxy for autonomic stress.                      |
| IC (integrated circuit)        | A small conventional (non-printed) electronic chip; the electronics module uses a hybrid IC for signal processing and wireless transmission.                            |
| BLE (Bluetooth Low Energy)     | A low-power wireless communication standard used to sync sensor data from the patch to the companion application.                                                       |
| R2R (roll-to-roll) processing  | A continuous, high-volume printing method suited to mass production.                                                                                                    |
| PET / TPU                      | Polyethylene Terephthalate / Thermoplastic Polyurethane - flexible plastic substrate materials.                                                                         |
| Piezoresistive                 | Describes a material whose electrical resistance changes measurably when mechanically deformed.                                                                         |
| LCR meter                      | An instrument measuring Inductance (L), Capacitance (C), and Resistance (R), used in electronics testing.                                                               |
| TENS / EMS                     | Transcutaneous Electrical Nerve Stimulation and Electric Muscle Stimulation - an established consumer device category FlexiCure Respond+ could integrate with.          |
| COGS (cost of goods sold)      | The direct cost of manufacturing one unit, used here to estimate per-component production cost.                                                                         |
| B2C (business-to-consumer)     | A sales model in which a company sells directly to individual end users.                                                                                                |
| ARR (annual recurring revenue) | A standard subscription-business metric: predictable revenue expected over a year from active subscriptions.                                                            |
| PrinLab                        | OAMK's (Oulu University of Applied Sciences) printed electronics pilot fabrication and testing laboratory, offered as part of the InnoFest first-prize support package. |
| Gate control theory            | A 1965 model of pain perception (Melzack and Wall) holding that non-painful stimuli, such as vibration, can inhibit pain signal transmission at the spinal cord.        |

*Table 1. Glossary of terms and abbreviations.*

5\. System Design and Architecture

5.1 Two-Part Hardware Architecture

FlexiCure is built as two physically separate components, a design chosen deliberately for both cost and power reasons, detailed in Sections 5.1 and 5.2 respectively.

5.1.1 Electronics Module (Reusable)

The electronics module is a small, rechargeable unit containing the hybrid analog front-end integrated circuit, the Bluetooth Low Energy radio, and the rechargeable battery. It is purchased once and reused across many attachable-part replacements, clicking into a standardized connector on each new attachable part. Target specifications are approximately 25 by 20 by 4 millimeters and under 3 grams.

5.1.2 Attachable Part (Disposable)

The attachable part is the disposable layer worn against the skin: printed electrodes, the piezoresistive strain layer, the thin-film resistive heating element, a flexible substrate, and a skin-safe adhesive. It is replaced on a regular cycle, illustratively every two to four days, and carries its own small, single-use power cell dedicated to the heating element, decoupled from the electronics module's battery for reasons explained in Section 5.2. Target specifications are 80 by 50 millimeters and 0.3 to 0.5 millimeters thick.

5.2 Power Architecture

Splitting sensing power from heating power across the two hardware components is a deliberate design decision, not an incidental one, and it is the reason the seven-day electronics module charge claim is credible.

Continuous sensing across three channels, strain, EMG, and GSR, together with batched Bluetooth Low Energy synchronization, draws an estimated 150 to 200 microwatts continuously. Over a full seven-day wear period, this amounts to roughly 25 to 34 milliwatt-hours, comfortably within the budget of a small rechargeable battery sized for the electronics module.

Heating draws dramatically more power by comparison. A thin-film resistive heater sustaining approximately 40 degrees Celsius, the target temperature discussed further in Section 5.4, draws on the order of 0.5 to 1 watt while active, three to four orders of magnitude more than sensing. A single 10 to 15 minute heat session can consume roughly 60 to 190 milliwatt-hours, potentially exceeding an entire week's sensing budget in one session. Powering both functions from a single battery on the electronics module would make the seven-day claim false the moment a user activated heat. Placing the heater's power source on the attachable part instead, replaced every few days rather than every seven, keeps the electronics module's sensing budget and its charge-life claim intact regardless of how frequently heat is used.

5.3 Signal Processing and the Adaptive Comfort Engine

On-device logic performs artifact rejection, cross-checking the strain channel's motion signature against EMG activity so that ordinary movement is not mistaken for a genuine tension event, consistent with the cross-channel gating approach established earlier in this project's development. Confirmed tension events, together with an associated confidence score, are synchronized to the companion application over Bluetooth Low Energy in batches, rather than as a continuous raw stream, to conserve power.

The companion application's Comfort Check feature, described in Section 5.5, provides the input for what this report terms the Adaptive Comfort Engine: rather than applying a single, fixed sensor threshold to every user, each Comfort Check tap becomes a labeled data point that recalibrates the user's own personal heat-trigger threshold over time. A user who consistently logs a given sensor intensity as "Hard" will see the automatic heat trigger recalibrate toward that intensity specifically for them, rather than a population-average setting. This is a design specification, not a validated learning system; its behavior under real usage has not been tested, and this limitation is restated explicitly in Section 9.

5.4 FlexiCure Respond: Heat and Optional Device Compatibility

FlexiCure Respond activates the attachable part's thin-film heating element automatically when a tension event is detected, or on manual demand through the companion application. The target operating temperature is approximately 40 degrees Celsius, chosen deliberately for two reasons. First, it falls within the same range used in the clinical heat-therapy studies described in Section 4.3, so it is grounded in the evidence base for pain relief specifically, not an arbitrary comfortable setting. Second, it sits a meaningful four-degree margin below the generally accepted skin-injury threshold of approximately 44 degrees Celsius, below which skin can tolerate continuous contact indefinitely; the relationship between temperature and burn injury above that threshold is steep rather than linear, so this margin matters for a device intended for continuous, multi-day wear. The system's safety design includes closed-loop temperature regulation with a hardware-level cutoff independent of the firmware, so that a software fault cannot allow the heating element to exceed a safe ceiling.

FlexiCure Respond+ extends this with optional compatibility for existing third-party Bluetooth-enabled heat and vibration devices, for users who want a stronger or longer session than the attachable part's own heater provides. This is a deliberate build-versus-integrate choice: connected heating pads and app-controlled TENS and EMS (Transcutaneous Electrical Nerve Stimulation and Electric Muscle Stimulation) units are already an established consumer product category, so FlexiCure's companion application is designed to pair with and trigger a compatible third-party device using the same fusion logic already used for the built-in response, rather than FlexiCure designing and manufacturing new proprietary accessory hardware. No specific third-party device or partnership is assumed at this stage.

5.5 Companion Application

The companion application is built around a small set of low-friction, high-engagement features, a deliberate response to a pattern observed in the existing pelvic wellness device market: reviews of Elvie and Perifit consistently report meaningful user engagement drop-off after four to six weeks, attributed in part to the effort required by their gamified exercise interaction model.

- Comfort Check: a one-tap logging prompt, Easy, Manageable, Hard, or Severe, requiring no typing or forms, designed to be fast enough to sustain long-term use.

- Period Log: a simple calendar log for period start and end dates, so every sensor event and Comfort Check entry is automatically tagged to a cycle day.

- Comfort Forecast: proactive heat suggestions based on the user's own logged pattern over time, rather than a reactive response only.

- Live sensor readings: EMG, GSR, and strain visible on the home screen at a glance, consistent with the broader design principle of showing underlying data rather than only a summary verdict.

- Manual Respond trigger: heat activated on demand, independent of automatic detection.

- Patch status: electronics module battery level and attachable part wear time, so the user knows when a replacement is due.

6\. Business Model and Market Analysis

6.1 Customer Segments

FlexiCure addresses women managing menstrual cramping or general abdominal muscle tension, a broad, everyday consumer segment. A specific, identifiable early-adopter segment is women who already purchase pelvic wellness devices such as Elvie or Perifit but find an insertable device uncomfortable or unappealing, an audience with an already-demonstrated willingness to spend on this category of product.

6.2 Market Sizing

Industry market research estimates the pelvic floor device market at approximately USD 892.4 million in 2026, projected to grow to approximately USD 1.89 billion by 2035, a compound annual growth rate of roughly 8.7 percent. FlexiCure does not compete for the same job as this market's incumbents, described in Section 3, but it reaches a closely adjacent buyer, and this figure provides a defensible order-of-magnitude sense of that buyer's willingness to spend on connected, app-based wellness hardware in this general product category.

6.3 Unit Economics (Illustrative)

The cost and pricing figures below are early-stage estimates intended to be tested during the pilot phase, not the output of a formal costing exercise.

|                                                                   |                          |                           |
|-------------------------------------------------------------------|--------------------------|---------------------------|
| **Component**                                                     | **Estimated Cost (EUR)** | **Purchase Frequency**    |
| Electronics module (IC, BLE, rechargeable battery, connector)     | 8-14                     | One-time                  |
| Attachable part (printed electrodes, heater, adhesive, substrate) | 2-3.50                   | Recurring, every 2-4 days |

*Table 2. Illustrative unit costs by hardware component.*

This two-part structure is a deliberate razor-and-blades revenue model: the electronics module is sold once, priced with a healthy margin, while the attachable part is sold on a recurring basis, either as a subscription or a multi-pack, at a substantially lower per-unit cost than a single-piece, fully-disposed design would require. As an illustrative, non-projective example: 1,000 electronics modules sold in a first year, each subscribing to attachable-part refills at approximately EUR 15 per month, would represent roughly EUR 180,000 in annual recurring revenue from refills alone, on top of one-time module sales.

6.4 Revenue Streams and Cost Structure Summary

- Revenue: one-time electronics module sales, priced with margin; recurring attachable-part refill sales, subscription or multi-pack.

- Cost structure: printed sensor and heater fabrication for the attachable part (low marginal cost via roll-to-roll or screen-printing); the hybrid IC, BLE radio, and rechargeable battery for the electronics module (the dominant one-time hardware cost); direct-to-consumer online distribution.

7\. Implementation Plan

The proposed development sequence covers both hardware components in parallel, since they share printing and assembly infrastructure but differ in final integration.

|                                 |                                                                                                            |
|---------------------------------|------------------------------------------------------------------------------------------------------------|
| **Step**                        | **Description**                                                                                            |
| 1\. Design and ink selection    | Electrode and heater geometry, functional-ink formulation for the attachable part                          |
| 2\. Printing                    | Screen-printing or roll-to-roll deposition of sensor and heater layers                                     |
| 3\. Electronics module assembly | Hybrid IC, BLE radio, and rechargeable battery integration into the reusable module                        |
| 4\. Attachable-part integration | Heater and connector integration onto the disposable attachable part                                       |
| 5\. Bench testing               | Signal fidelity and mechanical durability testing for both components                                      |
| 6\. Pilot with real users       | Small-scale pilot to validate wear time, engagement, and the Adaptive Comfort Engine's real-world behavior |

*Table 3. Proposed development sequence.*

Required equipment: a screen printer or roll-to-roll press; functional inks (conductive silver, dielectric, and piezoresistive formulations); flexible PET or TPU substrate; pick-and-place equipment for the hybrid IC; a lamination or encapsulation press; a multimeter or LCR meter; an oscilloscope for signal-fidelity verification; a flex-cycle chamber for durability testing; and a reference EMG device for calibration. OAMK's PrinLab facility, offered as part of the InnoFest first-prize support package, would provide access to this fabrication and testing infrastructure for an initial proof-of-concept build.

8\. Competitive Differentiation

FlexiCure's differentiation rests on two structural properties, not on any single component being individually novel. First, it is the only product in its adjacent market that both senses a physiological signal and requires no insertion; ELITONE is external but has no sensing layer, and every sensing-capable competitor is insertable, for the real anatomical reason discussed in Section 3.2. Second, it solves a different problem than its nearest competitors: tension sensing and comfort response, not exercise and strengthening, a distinction that means FlexiCure is not attempting to out-compete Elvie or Perifit at their own job, but rather to serve a use case none of them address.

Every individual sensing technique FlexiCure uses, abdominal surface EMG, GSR, and piezoresistive strain, is independently established in existing clinical or consumer literature, described in Section 4. The genuine, still-untested claim is the specific combination: applying electrohysterography-grade abdominal sensing, ordinarily used for labor monitoring, to everyday menstrual and abdominal tension, and pairing it with an adaptive, personalized heat-response loop.

9\. Limitations, Risks, and Outstanding Validation

This report deliberately documents what has not yet been demonstrated.

- The Adaptive Comfort Engine, described in Section 5.3, is a design specification, not a validated learning system. Its ability to meaningfully personalize a heat-trigger threshold from Comfort Check taps has not been tested with real users or real data.

- FlexiCure's sensing principle, abdominal surface EMG, is well-established for detecting uterine contraction during labor; its use as a proxy for the character or severity of everyday menstrual cramping has methodological precedent (electrohysterography) but has not itself been validated for this specific application.

- All cost, pricing, and revenue figures in Section 6 are illustrative planning estimates and have not been validated against actual manufacturing quotes or willingness-to-pay research.

- The two-part hardware's mechanical connector, between the electronics module and each new attachable part, is a real engineering component that has not been designed or tested; its reliability and ease of use for a non-technical consumer are open questions.

- FlexiCure Respond's safety design, closed-loop temperature regulation and a hardware-level cutoff, requires dedicated engineering and safety validation beyond the scope of the initial concept.

- The claim that FlexiCure addresses a distinct problem from Elvie and Perifit, rather than a lighter-touch alternative to the same problem, is a positioning argument based on the anatomical and functional analysis in Section 3, not an independent market-research finding.

10\. Roadmap

The proposed roadmap sequences by shared hardware and validation risk, extending the same reusable electronics module across new use cases rather than starting over for each one.

|           |                                                                                                                             |             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|-------------|
| **Phase** | **Focus**                                                                                                                   | **Status**  |
| Now       | Abdominal tension and menstrual comfort sensing, Respond heat, on the two-part hardware                                     | Day-1 build |
| Next      | New attachable-part placements (for example, lower back) using the same electronics module, sold as additional refill lines | Roadmap     |
| Later     | Formal Respond+ integration with a named third-party heat or vibration device partner                                       | Roadmap     |

*Table 4. Application roadmap by phase.*

11\. Conclusion

FlexiCure proposes that meaningful value in this product category comes not from inventing new sensing physics, every individual technique it uses is independently established, but from a deliberate set of engineering and business decisions: separating power-hungry heating from low-power sensing across two hardware components to make a seven-day charge claim actually true; applying an established clinical sensing technique, electrohysterography, to an everyday consumer problem it was not originally built for; and structuring the business around a razor-and-blades model that keeps recurring cost low while reaching a buyer already proven to spend in an adjacent market. The project's central open question, and the fair one for a jury to ask, is whether the Adaptive Comfort Engine's personalization actually holds up under real usage, a question this report does not claim to have answered, only to have scoped honestly for the pilot phase that follows.

References

Jo, Y. C., Kim, H. N., et al. Wearable Patch Device for Uterine EMG and Preterm Birth Monitoring Applications. Korea Electronics Technology Institute, 2018.

Electrohysterography for Uterine Contractility Monitoring: Measurement Principles, Clinical Evidence, and Reporting Recommendations. Sensors, 2026, 26(15), 4669. https://doi.org/10.3390/s26154669

Monica Healthcare (GE Healthcare). Monica AN24 - wireless abdominal fetal and maternal monitoring patch. Product documentation.

Jo, J., and Lee, S. H. Heat therapy for primary dysmenorrhea: A systematic review and meta-analysis of its effects on pain relief and quality of life. Scientific Reports, 2018, 8, 16252. https://www.nature.com/articles/s41598-018-34303-z

Melzack, R., and Wall, P. D. Pain mechanisms: A new theory. Science, 1965, 150(3699), 971-979.

Pelvic Floor Exerciser Market Size, Share, and Industry Trends Forecast 2026-2036. MarkWide Research. https://markwideresearch.com/pelvic-floor-exerciser-market

PelviRestore vs. Elvie vs. Perifit: Which Pelvic Floor Trainer Is Right for You? Product comparison, 2026.

Elvie Trainer Review: In-Depth Biofeedback Pelvic Floor Device Analysis. Product review and comparison, 2026.

PrintoCent. PrintoCent InnoFest Kick-off presentation, 1 September 2026. VTT Technical Research Centre of Finland / Oulu University of Applied Sciences (OAMK).
