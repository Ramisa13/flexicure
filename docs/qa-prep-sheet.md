# FlexiCure - Q&A Prep Sheet
### Team FLEXICURE, PrintoCent InnoFest 2026

The 20 toughest questions a judge could ask, with a tight, honest answer for each. Read this once before Day 1, and again before Day 2. Questions 1-10 cover the core pitch; questions 11-20 cover the competitive landscape, the ones most likely to land if a judge has done their homework.

**Golden rule:** if you don't know, say "we don't know yet, that's what the pilot is for." Judges trust that far more than a confident guess.

---

### 1. "Have you actually tested the fusion logic?"

No. The cross-channel gating logic (concurrent EMG + GSR, checked against strain) is a design specification, not a validated algorithm. Its real false-positive and false-negative rates under everyday motion, walking, coughing, rolling over, haven't been measured yet. That's exactly what the bench-testing and pilot phases in our implementation plan are for.

---

### 2. "Is this really novel, or has it been done before?"

Partially. The general pattern, a wearable sensor closing the loop into an automatic therapeutic response, is active published research (for example, closed-loop EMG-driven TENS systems, closed-loop insulin delivery). We're not claiming to have invented that pattern. What we haven't found precedent for is this specific combination: EMG-driven heat response for abdominal muscle tension specifically, on a non-insertable, two-part hardware platform. If a judge names something similar, ask what it is and genuinely compare, don't get defensive.

---

### 3. "Isn't a reusable-electronics, disposable-patch split just how continuous glucose monitors already work?"

Yes, in part, real precedent exists (Dexcom's G6 used exactly this split). Full answer, including why a market leader later moved away from it, is under question 20.

---

### 4. "How do you know 40°C is safe to wear for hours?"

Skin can tolerate temperatures up to about 44°C indefinitely without injury; above that, burn risk rises fast, roughly doubling per additional degree. We're targeting ~40°C, a 4°C safety margin below the injury threshold, in the same range used by existing continuous low-level heat wrap products and the clinical studies behind our heat-therapy evidence. The system also has a hardware-level temperature cutoff independent of the firmware, so even a software fault can't push it past a safe ceiling.

---

### 5. "Do you have a partnership with [device maker] for Respond+?"

No. Respond+ is a roadmap compatibility feature, the idea that our app could connect to existing Bluetooth-enabled heat or vibration devices already on the consumer market (connected heating pads, TENS/EMS units). No specific device or company partnership exists today. We're flagging it as a smart build-versus-integrate decision, not claiming it's built.

---

### 6. "Why should we trust your team on a women's health wearable?"

Be straight about the gap. Our directly relevant published research is in biomedical signal analysis, which is where the method transfers: reading noisy multi-channel body signals. We do not claim gynecological clinical expertise. That is why the pilot plan includes a clinical partner, and why we lean on published electrohysterography and the Machado 2019 heat trial instead of our own clinical claims.

---

### 7. "Is this too much to build in two days?"

The product is one thing: one electronics module and one patch, for abdominal comfort. Sensing, heat and the app are the same hardware and firmware path, not separate builds. For the demo, show the two parts, the app flow and the Comfort Check tap. Everything else is on the roadmap, clearly labelled as not yet built.

---

### 8. "These cost and pricing numbers, are they real?"

They're illustrative planning estimates, not the output of a costing exercise, a manufacturing quote, or market research. We were explicit about that in the business case. The actual per-unit cost, pricing, and margin will come from real supplier quotes and a pilot, not from this deck.

---

### 9. "What about GDPR and medical device regulation?"

Menstrual and abdominal health data can qualify as special-category data under GDPR, so any pilot needs a real consent flow and a data protection impact assessment, neither exists yet. On the device side, we've deliberately kept FlexiCure framed as a non-diagnostic wellness product specifically to stay on a lighter regulatory path; the moment we added a diagnostic claim, a specific validated prediction window, or built-in electrical stimulation output, we'd likely trigger formal medical device classification. We haven't done a full regulatory strategy, that needs real legal input before any clinical marketing claim.

---

### 10. "What happens after InnoFest if you don't win?"

Have a real answer ready, not just "we'd be sad." E.g.: "We'd still want the idea-development consultation and PrinLab access if the pilot phase is realistic for us, and we'd start with the period-pain configuration since it has the fastest regulatory and go-to-market path." Judges sometimes ask this specifically to see if you're building a company or just building a pitch.

---

## Additional Critical Questions (Competitive Landscape)

These got sharper after researching what's already on the market. Read these last, they're the ones most likely to actually come up if a judge has done their homework.

### 11. "There are already dozens of TENS and heat devices for period pain, some FDA-cleared since 2008 with millions sold. Why does this need a sensor?"

Because every one of those devices is open-loop, the patient decides when to turn it on, usually after the pain is already bad. None of them read a biosignal first. Our claim isn't "TENS or heat for period pain is new," it's "reading EMG and GSR to catch a cramp and respond automatically, potentially earlier than the patient would react on their own, is what's missing." That said, we haven't shown this closed-loop approach actually improves outcomes over just letting the patient press a button. That's an assumption, not a result.

### 12. "You claim it catches a spasm 'early' and mention labor monitoring. Is this becoming a medical device?"

Deliberately not, and that's worth being direct about. The underlying sensing principle, electrohysterography, is genuinely used clinically for labor monitoring, that's real, cited precedent for why the physiology works. But the product we're selling today is a non-medical wellness device: no diagnostic claim, no specific validated prediction window. If a specific "10 to 15 minutes early" figure ever comes up, that's a product target, not a validated clinical result, we haven't tested it. Labor monitoring itself would be a much later, separately regulated roadmap direction, not something we're building or claiming now.

### 13. "Women already buy heat wraps for pennies. Why would they pay for a module and patches?"

Fair. A wrap is cheap but blind: it cannot tell you when tension builds or whether it helped. Our bet is that a share of users will pay for sensing plus personalised timing, the way people pay for a fitness tracker over a stopwatch. We have not tested willingness to pay. Price points (module about EUR 39-49 proposed, patch 3-pack about EUR 15 per month) are planning estimates to be tested in a pilot.

### 14. "If sensor-triggered pain response is such an obvious idea, why hasn't an established TENS company already added sensors to their product?"

Possibly because multi-channel biosignal fusion is a different engineering discipline than simple electrical stimulation output, or because a profitable, established company has less incentive to add complexity to a product that already sells well. We don't know for certain, and that uncertainty is itself a reason to stay measured rather than claim we found something everyone else missed.

### 15. "What's your actual moat? Couldn't an established player just add sensors to their existing device faster than you could build a company?"

Probably, yes, if they wanted to. We don't have patent-based protection. Our near-term defensibility is being first with a working, validated fusion algorithm and real clinical relationships, that's a real but modest moat, not a permanent one.

### 16. "Would people actually trust a connected device with their menstrual health data, given the controversy around period-tracking apps and data privacy?"

Real concern, not hypothetical. Any real product needs explicit, minimal data collection, local on-device processing where possible, and clear consent. This is exactly why our case study flags GDPR special-category data handling as unresolved, we haven't designed the actual privacy architecture yet, and we shouldn't imply otherwise.

### 17. "Wearing an electronic patch for 5 to 7 days, won't that cause skin irritation?"

Realistic risk we haven't tested. Skin-safe medical adhesives are standard in comparable wearables, continuous glucose monitors and Zio cardiac patches wear for a similar or longer duration, but our specific adhesive and skin compatibility hasn't been tested. Squarely a bench and pilot-phase question.

### 18. "Do you have any IP or patent protection for this?"

No, nothing filed. Normal for a two-day competition concept, but if this moved forward, freedom-to-operate and patentability would need real legal review, especially given how crowded the period-pain device space already is.

### 19. "Do you sell a device, a subscription and data at once? Is that too much for a small team?"

Yes, that would be too much. The plan is sequenced: first sell the module and patches to consumers (razor-and-blades), prove retention, and only then consider partnerships. Data sales are not part of the plan today, and any use of menstrual data would need explicit consent.

### 20. "Isn't this just a copy of how continuous glucose monitors work?"

Partly, and that's a strength, not a weakness. Dexcom's G6 used exactly our architecture: a disposable sensor paired with a reusable, 90-day transmitter. That's real, proven precedent that a reusable-electronics split can work commercially. But Dexcom moved away from it in the G7, integrating everything into one disposable unit, because users found the snap-together two-piece process cumbersome, and full integration let them shrink the device by 60% and cut warm-up time from 2 hours to 30 minutes. So the honest answer has two parts: the cost-saving idea is proven, but so is the friction that made a market leader abandon it. Our bet is that the friction doesn't map the same way onto us, our module swap happens every 2 to 4 days, not every rare 90 days, so it stays a familiar routine rather than a half-forgotten fiddly task. That's a real assumption we're making, not a settled fact.

---

## If you genuinely don't know the answer

Say exactly that. "We don't know yet, that's what the pilot would tell us" is a stronger answer than an invented number. Every judge on this panel has seen enough pitches to know confident nonsense when they hear it.
