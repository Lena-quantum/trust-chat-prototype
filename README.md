# Trust — a concept prototype for AI interfaces

Clickable concept artifact exploring **trust as a designed variable in human–AI interaction**: four trust dimensions (sources, confidence, semantics, interactions) plus a counter-principle (visible absence of evidence as a trust act).

**Live:** [https://lena-quantum.github.io/trust-chat-prototype/](https://lena-quantum.github.io/trust-chat-prototype/)

## What's in here

Vanilla HTML / CSS / JS. No build step. No dependencies. Open `index.html`.

```
.
├── index.html      conversation surface, two scripted exchanges
├── styles.css      trust-signal grammar (citation chips, confidence rings, hedge typography, …)
├── app.js          interactions — popovers, side-panel, modality switcher, feedback chips, …
├── data.js         scripted source records
└── assets/         supporting graphics
```

## How to read the prototype

The conversation demonstrates trust signals in two registers:

1. **Exchange 1** — well-sourced response inside the model's evaluated domain. Citation chips, confidence pills, hedge typography, modality switcher (text / bullets / table / diagram).
2. **Exchange 2** — question grounded in private data the model can't evaluate. Competence indicator flips to `outside`; empty-state confession; `no-source` chips; "what I'd need" checklist with upload pills and yes/no toggle.

Try: hover any citation chip; click the competence indicator (top right); switch modalities; reject two claims (✕ on hover) and watch the steering bar; toggle "ask me before showing" and press send.
