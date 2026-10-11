# FlexiCure Deck - text export

Source file: `slides/FlexiCure_Deck.pptx` (13 slides). Speaker notes included.


## Slide 1

- FlexiCure
- Senses Abdominal Muscle Tension. Responds With Heat.
- A non-insertable wearable for women managing menstrual cramping and abdominal muscle tension - two-part hardware: a rechargeable electronics module and a low-cost, disposable attachable part.
- Team FLEXICURE  |  PrintoCent InnoFest 2026

> **Speaker notes:** [0:00-0:25] Menstrual cramping and everyday abdominal muscle tension are managed by guesswork. Heat wraps and painkillers get applied on a hunch, not because anyone actually knows tension is building. Nobody has an objective signal for this.

## Slide 2

- Building a Successful Business Case
- The InnoFest framework, answered for FlexiCure
- 1
- WHAT'S THE PROBLEM?
- Abdominal muscle tension and menstrual cramping are managed by guesswork - no objective way to know when tension is building, or whether today's relief actually helped.
- 2
- WHOSE PROBLEM IS IT?
- Women managing menstrual cramps or everyday abdominal muscle tension - a broad, everyday audience, not a narrow clinical population.
- 3
- HOW DO THEY SOLVE IT TODAY?
- Heat wraps and painkillers, applied on a guess, with no sensing. Period apps log dates only. Pelvic floor trainers (Elvie, Perifit) exist, but are insertable and target a different muscle group entirely.
- 4
- WHY IS YOUR SOLUTION BETTER?
- FlexiCure senses abdominal muscle tension directly, using the same principle as clinical electrohysterography, and closes the loop with automatic heat - no insertion, no guessing when to apply relief.

> **Speaker notes:** [0:25-0:55] This is a broad, everyday problem for women, not a narrow clinical one. Today's alternatives are all incomplete: heat wraps and painkillers with no sensing, period apps that log dates but nothing physiological, and pelvic floor trainers like Elvie and Perifit, which exist, but require internal insertion and sense a completely different muscle group.

## Slide 3

- In Our Presentation, We Focus On
- Idea, Market, and Feasibility
- IDEA
- One external patch, two-part hardware, senses abdominal muscle tension and closes the loop with automatic heat - no insertion, no guessing.
- MARKET
- A real, sized adjacent market: the pelvic-floor device space is worth USD 892.4M in 2026, growing to USD 1.89B by 2035 (8.7% CAGR) - FlexiCure serves the same buyer with a non-insertable alternative.
- FEASIBILITY
- Abdominal surface EMG (electrohysterography) is an established clinical technique with real wearable-patch precedent; manufacturing via screen-printing/R2R at OAMK PrinLab.

## Slide 4

- FLEXICURE
- Lean Canvas - FlexiCure
- PrintoCent InnoFest 2026
- Iteration #6
- 2
- Problem
- Abdominal muscle tension & menstrual cramping are managed by guesswork - no objective sense of building tension Pelvic floor trainers exist, but sense a different muscle group and require internal insertion Nothing external senses abdominal tension and responds with relief automatically
- Existing Alternative
- Heat wraps & painkillers, applied on a guess; period apps log dates only, no sensing
- 4
- Solution
- Two-part patch: rechargeable electronics module + disposable attachable part Senses abdominal EMG, GSR, strain; auto-triggers heat via the attachable part Comfort Check + Period Log personalize the trigger over time
- 8
- Key Metrics
- EMG tension-signal correlation with Comfort Check taps Comfort Check + Period Log engagement rate Attachable-part reorder rate; module battery life vs. 7-day claim
- 3
- Unique Value Proposition
- External, non-insertable - senses abdominal muscle tension directly, competitors sense a different muscle group internally Learns each user's own comfort pattern through one-tap logging, not a fixed threshold Two-part hardware keeps ongoing cost low: one module, cheap disposable refills
- 9
- Unfair Advantage
- Team's biomedical signal-analysis background, directly applicable to EMG interpretation University of Oulu research network
- 5
- Channels
- Direct-to-consumer online - the channel already proven for this buyer Retail alongside women's wellness products InnoFest jury network
- 1
- Customer Segments
- Women managing menstrual cramping or abdominal muscle tension Early adopters: women already spending EUR 99-199 on insertable pelvic trainers who want a non-insertable option
- Early Adopters
- Existing Elvie/Perifit customers seeking a non-insertable alternative
- 7
- Cost Structure
- Electronics module: IC, BLE radio, rechargeable battery, connector (~EUR 8-14, one-time) Attachable part: printed electrodes, heater, adhesive, substrate (~EUR 2-3.50, recurring) Manufacturing via screen-printing/R2R (OAMK PrinLab)
- 6
- Revenue Streams
- One-time electronics module sale, priced with margin Recurring attachable-part refill sales (subscription or multi-pack)

## Slide 5

- What FlexiCure Looks Like
- Two parts: a reusable electronics module, and a disposable attachable part
- IC + BLE
- + Battery
- Electronics Module (Reusable)
- clicks into
- Attachable Part (Disposable)
- Target Specifications (Illustrative)
- Electronics module size:  ~25 mm x 20 mm x 4 mm
- Electronics module battery:  Rechargeable, 1 charge covers 7 days of sensing
- Electronics module weight:  Under 3 g
- Attachable part size:  80 mm (L) x 50 mm (W), 0.3-0.5 mm thick
- Attachable part power:  Single-use cell, powers the heater only, decoupled from the module
- Replacement interval:  Every 2-4 days (illustrative)
- All measurements are illustrative target specifications to be confirmed during the prototyping phase.

> **Speaker notes:** [0:55-1:10] FlexiCure is two parts. A small rechargeable electronics module, about the size of a coin, holds the sensors and Bluetooth radio, one charge lasts a full week. It clicks into a disposable attachable part, the actual patch, replaced every few days, that carries the printed electrodes, the heater, and the adhesive.

## Slide 6

- How the Sensors Work
- External, non-insertable - worn on the lower abdomen, over the uterus
- Where It's Worn
- Lower abdomen, over the uterus - the same placement used in clinical electrohysterography (EHG) Not the pelvic floor - a different, externally-accessible muscle group No insertion required, unlike Elvie, Perifit, or kGoal
- What It Senses
- EMG - abdominal/uterine muscle electrical activity GSR - autonomic stress response Strain - muscle tension and contraction, cross-checked to reject motion artifact
- Grounded in Real Precedent
- Electrohysterography (EHG)
- An established, non-invasive clinical technique: adhesive surface electrodes on the abdomen read uterine electrical activity. Detects ~94% of contractions confirmed by an internal pressure reference, versus ~54% for older external methods.
- Jo et al., 2018
- Built a real abdomen-attachable uterine EMG patch, ~43mm x 36mm, close to FlexiCure's own target size - direct academic precedent for this exact approach.
- Monica AN24
- A real commercial wireless abdominal EMG patch, already used clinically to monitor uterine activity - proof this sensing approach is already trusted in practice.

> **Speaker notes:** [1:10-1:35] It's worn externally, on the lower abdomen, over the uterus, not inserted. That placement isn't arbitrary, it's the same one used in electrohysterography, a real clinical technique for reading uterine muscle activity through the skin. There's direct academic precedent for a patch this size doing exactly this, and a real commercial product, the Monica AN24, already does it clinically.

## Slide 7

- FlexiCure Respond: From Sensing to Soothing
- Heat lives on the attachable part - powered separately from the electronics module
- The Feature
- A thin-film resistive heating element on the attachable part Triggers automatically when tension is detected, or manually via the app Powered by the attachable part's own small cell, not the rechargeable module Optional: Respond+ compatibility with existing Bluetooth heat or vibration devices, for a stronger session
- Why Power Is Split This Way
- Sensing draws ~150-200 microwatts continuous - a week's use needs only ~30 mWh A single heat session can draw ~60-190 mWh - more than a week of sensing, in minutes Splitting power keeps the module's 7-day claim true regardless of how much heat is used
- Two Modalities
- Built In: Heat
- Standalone, always available while worn - no other device required.
- Optional: External Devices
- Connects to existing Bluetooth heat or vibration pads already on the market, for a stronger or longer session.

> **Speaker notes:** [1:35-1:55] When tension is detected, the attachable part's own heater responds automatically, or the patient triggers it manually. We power sensing and heating separately on purpose: sensing sips power, a single heat session can use more energy than a whole week of sensing, so splitting them is what makes the seven-day charge claim actually true.

## Slide 8

- Companion App: Features & How It Works
- One-tap logging that makes the heat trigger smarter over time
- App Features
- Comfort Check - one-tap logging (Easy / Manageable / Hard / Severe), no forms, no typing Period Log - a simple calendar log for period start/end dates, tagging every event to a cycle day Comfort Forecast - proactive heat suggestions based on the user's own logged pattern Live sensor readings - EMG, GSR, and strain visible at a glance, not just a summary status Manual Respond trigger - heat on demand, independent of automatic detection Patch status - electronics module battery, attachable part wear time
- How It Works: The Adaptive Comfort Engine
- 1
- Pair & log
- Patient pairs the electronics module once, and logs period dates in the Period Log.
- 2
- Wear & sense
- EMG, GSR, and strain stream continuously while the attachable part is worn.
- 3
- Comfort Check
- A one-tap prompt asks how the current moment feels: Easy, Manageable, Hard, or Severe.
- 4
- Threshold learns
- Each tap recalibrates the user's own heat-trigger threshold - not a fixed, one-size rule.
- 5
- Respond triggers
- Heat activates automatically at the personalized threshold, or the patient triggers it manually.
- 6
- Forecast improves
- Over time, the app proactively suggests heat before tension peaks, based on the user's own pattern.

> **Speaker notes:** [1:55-2:20] The app's real trick is a one-tap Comfort Check: easy, manageable, hard, or severe. Every tap personalizes that user's own heat-trigger threshold, so the system gets more accurate specifically for them over time, not a generic population average.

## Slide 9

- Business Case: Costing, Customers & Economics
- Two-part hardware keeps recurring cost low - a razor-and-blades model
- Unit Cost (Illustrative)
- Electronics module: IC + BLE + rechargeable battery + connector - EUR 8-14, one-time Attachable part: printed electrodes + heater + adhesive + substrate - EUR 2-3.50, recurring Recurring cost drops ~80-85% versus a single-piece, weekly-disposed design
- Pricing & Revenue Model
- One-time electronics module purchase, priced with healthy margin (the razor) Recurring attachable-part refills, subscription or multi-pack (the blades) Direct-to-consumer, the channel already proven for this buyer
- Market Context
- Pelvic-floor device market: USD 892.4M in 2026, growing to USD 1.89B by 2035 (8.7% CAGR) Real, funded comparators: Elvie (EUR 149-199), Perifit (EUR 99-149), kGoal - all insertable FlexiCure reaches the same buyer with a non-insertable, different-muscle-group alternative
- Case Study: Illustrative Economics
- 1,000 electronics modules sold in year one, each subscribing to attachable-part refills at ~EUR 15/month, represents roughly EUR 180,000 in annual recurring revenue from refills alone, on top of one-time module sales - a realistic first proof point, not a market-wide projection.

> **Speaker notes:** [2:20-2:45] The pelvic wellness market is real and sized, 892 million dollars in 2026, heading toward 1.9 billion by 2035. Elvie and Perifit already prove women will spend 100 to 200 euros here. We reach the same buyer with a non-insertable alternative, and the two-part hardware means our recurring cost is a fraction of theirs.

## Slide 10

- Implementation Plan
- From design to a working prototype of both hardware parts
- Design & ink selection
- 1
- Print electrode layers (R2R / screen-print)
- 2
- Assemble electronics module
- 3
- Integrate attachable-part heater
- 4
- Bench test (signal fidelity, durability)
- 5
- Pilot with real users
- 6
- Equipment & Materials
- Printing & Fabrication
- Screen printer or roll-to-roll press Conductive silver, dielectric, and piezoresistive inks Flexible PET/TPU substrate Pick-and-place for the hybrid IC Lamination/encapsulation press
- Testing & Validation
- Multimeter / LCR meter Oscilloscope for signal fidelity Flex-cycle chamber for durability Reference EMG device for calibration

> **Speaker notes:** [2:45-2:55] Every sensing technique here already exists in clinical literature. Manufacturing is screen-printing and roll-to-roll, the same processes this lab already runs. We're asking for exactly what the InnoBoost prize offers: PrinLab access to build our first working prototype.

## Slide 11

- What's Next
- Prove the core, then extend the same hardware further
- 1
- NOW
- Abdominal Tension & Period Comfort
- Core sensing (EMG, GSR, strain) and Respond heat, on the two-part hardware - the Day-1 build.
- 2
- NEXT
- New Attachable-Part Placements
- Same electronics module, new attachable parts sized for other tension areas (e.g. lower back), sold as additional refill lines.
- 3
- LATER
- Respond+ Device Integration
- Formal compatibility with named third-party Bluetooth heat and vibration devices, beyond the current no-partnership roadmap item.
- Shared foundation across every phase:
- One rechargeable electronics module, reused across attachable parts and use cases - only the disposable layer changes.

> **Speaker notes:** [2:55-3:00] CLOSE: One electronics module, endlessly reusable. One disposable part, replaced cheaply. Built for a market that's already proven women will pay for it. That's FlexiCure.

## Slide 12

- Glossary of Terms and Abbreviations
- Every acronym and technical term used in this deck, defined in one place
- EMG:  Electromyography - electrical activity produced by muscle contraction, read via skin-surface electrodes.
- EHG:  Electrohysterography - the clinical term for surface EMG of the uterus, read from the abdomen.
- GSR:  Galvanic Skin Response - skin conductance change caused by sweat gland activity, a proxy for autonomic stress.
- IC:  Integrated Circuit - a small conventional chip; the electronics module uses a hybrid IC for signal processing.
- BLE:  Bluetooth Low Energy - a low-power wireless standard for syncing patch data to the app.
- R2R:  Roll-to-Roll - a continuous, high-volume printing method suited to mass production.
- PET / TPU:  Polyethylene Terephthalate / Thermoplastic Polyurethane - flexible plastic substrate materials.
- LCR meter:  An instrument measuring Inductance (L), Capacitance (C), and Resistance (R) for electronics testing.
- COGS:  Cost of Goods Sold - the direct per-unit cost of manufacturing one part.
- ARR:  Annual Recurring Revenue - predictable yearly subscription revenue.
- B2C:  Business-to-Consumer - selling directly to individual end users.
- PrinLab:  OAMK's printed electronics pilot fabrication and testing lab, part of the InnoFest first-prize support.

## Slide 13

- FLEXICURE
- Lean Canvas - FlexiCure
- PrintoCent InnoFest 2026
- Iteration #6 - Final
- 2
- Problem
- Abdominal muscle tension & menstrual cramping are managed by guesswork - no objective sense of building tension Pelvic floor trainers exist, but sense a different muscle group and require internal insertion Nothing external senses abdominal tension and responds with relief automatically
- Existing Alternative
- Heat wraps & painkillers, applied on a guess; period apps log dates only, no sensing
- 4
- Solution
- Two-part patch: rechargeable electronics module + disposable attachable part Senses abdominal EMG, GSR, strain; auto-triggers heat via the attachable part Comfort Check + Period Log personalize the trigger over time
- 8
- Key Metrics
- EMG tension-signal correlation with Comfort Check taps Comfort Check + Period Log engagement rate Attachable-part reorder rate; module battery life vs. 7-day claim
- 3
- Unique Value Proposition
- External, non-insertable - senses abdominal muscle tension directly, competitors sense a different muscle group internally Learns each user's own comfort pattern through one-tap logging, not a fixed threshold Two-part hardware keeps ongoing cost low: one module, cheap disposable refills
- 9
- Unfair Advantage
- Team's biomedical signal-analysis background, directly applicable to EMG interpretation University of Oulu research network
- 5
- Channels
- Direct-to-consumer online - the channel already proven for this buyer Retail alongside women's wellness products InnoFest jury network
- 1
- Customer Segments
- Women managing menstrual cramping or abdominal muscle tension Early adopters: women already spending EUR 99-199 on insertable pelvic trainers who want a non-insertable option
- Early Adopters
- Existing Elvie/Perifit customers seeking a non-insertable alternative
- 7
- Cost Structure
- Electronics module: IC, BLE radio, rechargeable battery, connector (~EUR 8-14, one-time) Attachable part: printed electrodes, heater, adhesive, substrate (~EUR 2-3.50, recurring) Manufacturing via screen-printing/R2R (OAMK PrinLab)
- 6
- Revenue Streams
- One-time electronics module sale, priced with margin Recurring attachable-part refill sales (subscription or multi-pack)