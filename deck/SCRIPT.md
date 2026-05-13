# Trust — final presentation · speaking script

**Total target:** ~10 min · ~6:30 of slides + ~3:00 live demo + ~0:30 wrap.
**Pace cue:** ~140 words / min. Time annotations below assume natural pause at slide transitions.

---

## SLIDE 1 — Title  *(~15 s)*

> My final project is called *Trust* — a concept prototype for human–AI interfaces.
> The thesis in one sentence: **trust is the central design variable for human–AI interaction, and it can be deliberately designed for** — not just hoped for as a side-effect of good model output.

---

## SLIDE 2 — Problem  *(~40 s)*

> Most AI products today produce fluent output, but they don't give the user any surface to evaluate it. The model speaks smoothly, the user accepts on instinct, and walks away with *miscalibrated* trust — usually overtrust.
>
> The workaround today is a manual verification loop: re-running prompts across LLMs, Command-F-ing source documents, cross-checking citations. From the interviews I did, this loop often costs more time than the original task. Seventy-three percent of the graduate students I spoke to had been burned by fake AI citations. And essentially none of the products on the market today treat trust *differently* based on the stakes of the question.

---

## SLIDE 3 — Thesis  *(~25 s)*

> So my thesis is this: **trust is not an emergent property of good model output. It is a deliberate design output** — manufactured by the interface, on top of whatever the model produces.
>
> Every trust signal in my prototype is an interface decision, not a happy accident. Which claims get cited, when confidence appears, how the model hedges, where the user steers — all interface choices.

---

## SLIDE 4 — Four dimensions  *(~55 s)*

> I operationalized this through four trust dimensions.
>
> **One — Sources.** Provenance and citation as the foundation. References are inspectable objects in the response, not footnotes you have to leave the page to verify.
>
> **Two — Confidence.** Calibrated bands that translate internal probability into a glanceable trust signal. Confidence pills appear *only* when confidence isn't high — the omission itself is information.
>
> **Three — Semantics.** The *manner* of communication. Hedging language, tone, modality. The prose itself is a trust surface — how something is said is often a stronger trust signal than any badge.
>
> **Four — Interactions.** Affordances that let the user steer, accept, refine, reject. Interaction transfers ownership from system to user — and trust follows ownership.

---

## SLIDE 5 — Counter-principle  *(~45 s)*

> The most important move in the whole project is the **counter-principle**: visible absence of evidence is itself a trust act.
>
> When the user asks the model something it can't competently answer, the response leads with an empty-state confession instead of papering over the gap. A model that buries its uncertainty three paragraphs in is *hiding* it. Leading with the limitation is the honesty move.
>
> But anti-trust isn't refusal. The model still ends with a small, caveat-scoped recommendation — and a checklist of what would unlock a sourced answer. The failure state becomes an actionable handoff.

---

## SLIDE 6 — Pre-mortem corridor  *(~45 s)*

> There are three failure modes I had to design against.
>
> On the left, **insufficient transparency** — smooth, confident UI that hides uncertainty and produces overtrust. Most AI products today live here.
>
> On the right, the **transparency paradox** — making risks too visible reduces trust below a productive threshold; users disengage rather than calibrate. Plus a third failure: **cognitive overload** from stacking too many trust artifacts at once.
>
> The design tries to sit in the narrow corridor between these — what I'm calling a *calibrated witness*. Every decision in the prototype is a position along that corridor.

---

## SLIDE 7 — The loop  *(~45 s)*

> The core interaction is a loop. The user sends a question. The model responds with trust signals embedded inline. The user evaluates as they read — hovering citation chips for source popovers, hedge underlines for the reason the model hedged. The user steers via per-claim feedback chips and the persistent steering bar. And critically, that feedback persists into the next response.
>
> The single most important rule: **the loop is never silent**. Every user action produces a visible acknowledgement. Silent absorption is treated as a design bug, not a feature.

---

## SLIDE 8 — Six states  *(~50 s)*

> The system has six states.
>
> The common case — *domain · evaluated* — uses citation chips, confidence pills sparingly, hedge typography on softened clauses.
>
> The counter-principle case — *domain · outside* (highlighted here) — flips the header, opens with the confession panel, marks inferences with no-source chips, and offers an actionable checklist.
>
> Plus four supporting states: a source side-panel for inspection, an agent trace for process visibility, cognitive forcing for high-stakes prediction, and rejection cascade for closed-loop feedback persistence.

---

## SLIDE 9 — Annotated flow  *(~55 s)*

> To show interaction-design depth: here's the design reasoning behind the outside-domain response — the most important exchange in the prototype.
>
> **First:** the competence flip lives in the *header*, not inside the message. Outside-domain is a session-level state, not a per-message flag. A banner inside each message would imply the system is broken; a quiet header shift implies it's self-aware.
>
> **Second:** the confession comes first. Buried uncertainty is hidden uncertainty.
>
> **Third:** the response splits into *"what I can say"* and *"what I would need"* — failure state turned into actionable handoff.
>
> **Fourth:** the single inference carries two signals at once — a rust no-source chip *and* hedge typography. Double uncertainty, double signal.

---

## SLIDE 10 — Evolution  *(~45 s)*

> How the design moved over three weeks. Week 13 was the framework on paper. Week 14 was the first clickable build, but the counter-principle was just described as a rule — not yet built.
>
> The biggest shift was making the outside-domain exchange an equal-weight second exchange. The argument of the whole project sits or falls on whether that exchange reads as honest.
>
> Week 15 added the actionable handoff — real checkboxes, upload pills, yes/no toggles. The counter-principle became *doable*, not just declarative.

---

## SLIDE 11 — Tradeoffs and open questions  *(~50 s)*

> Five things I'm still genuinely uncertain about.
>
> **A.** There are two places confidence shows up — chip popover and inline pill. Not redundant, but users have to learn both.
>
> **B.** Eight visible trust marks. The per-genre allocation rule is the guard, but the overload threshold is empirically unknown.
>
> **C.** In peer review, three readers said the confession panel is appropriately calibrated; one said excessive. Worth A/B testing.
>
> **D.** The rejection cascade — some readers find it responsive, others find it surveillance-adjacent. Toast copy is the lever.
>
> **E.** Cognitive forcing has the strongest empirical evidence in the system — Buçinca et al. 2021 — but is the most disruptive to flow. Open question: does anyone keep it on after the first encounter?

---

## SLIDE 12 — Mental model + demo  *(~25 s)*

> The mental model I'm trying to teach is: **a calibrated witness, not an oracle**. The system tells you what it knows, how it knows it, and where its knowledge ends. It's not trying to persuade you. It's trying to give you enough to decide.
>
> Let me show it to you live now.

---

## DEMO — live walkthrough  *(~3 min · 5 beats)*

**Beat 1 — common case, hover citation** *(~30 s)*
> Here's the first exchange — a well-sourced response. Notice the citation chip after "hybrid of the two." Hovering shows the popover — title, domain, and a *source-class badge* — peer-reviewed in this case. Clicking opens the side panel with the full source body and an entailment statement: this source directly supports the claim.

**Beat 2 — modality switch** *(~25 s)*
> Same content, restructured. Text becomes bullets, becomes a table, becomes a manipulable diagram. Same trust signals carry through. In the diagram I can drag the nodes and the structure re-flows — the user can rearrange the model's worldview and watch it stay consistent.

**Beat 3 — outside-domain** *(~40 s)*
> Scrolling to the second exchange. Notice the header — domain just flipped to *outside*. The response opens with the amber confession panel. The single inference carries the rust no-source chip plus hedge typography. And here's the *what-I'd-need* checklist — these are interactive: I can check them, upload a file via this grey pill, or answer yes/no for context questions. The model has converted its failure state into an actionable handoff.

**Beat 4 — closed loop** *(~25 s)*
> Watch the steering bar. If I reject two claims on the previous response — *here* — a toast fires and the hedging strength auto-shifts from *measured* to *cautious*. The model is listening, and the next response will reflect that change. Silent absorption would be a design bug.

**Beat 5 — cognitive forcing** *(~20 s)*
> Last move. The forcing toggle. With it on, the next send asks me to commit a prediction before the model shows its answer. This is Buçinca 2021 — the single strongest known intervention against automation bias on high-stakes tasks.

---

## WRAP  *(~15 s)*

> So that's the project. The system isn't trying to be the smartest voice in the room — it's trying to be the most *honest* one. A calibrated witness. Thank you — happy to take questions.

---

## Quick reference card — total budget

| Section | Time | Notes |
|---|---|---|
| Slides 1–12 | 6:30 | Click slide numbers `1`–`9` or arrow keys to jump |
| Demo (5 beats) | 3:00 | Use the `?stage=` URLs if you want to skip into a specific state |
| Wrap + buffer | 0:30 | |
| **Total** | **10:00** | |

### `?stage=` URLs for instant deep-link

- common case: `https://lena-quantum.github.io/trust-chat-prototype/`
- citation hover: `…/?stage=citation-hover`
- source panel: `…/?stage=source-panel`
- modality diagram: `…/?stage=modality-diagram`
- outside-domain: `…/?stage=outside-domain`
- agent trace: `…/?stage=agent-trace`
- cognitive forcing: `…/?stage=cognitive-forcing`
- rejection cascade: `…/?stage=rejection-cascade`
- legend: `…/?stage=legend`
