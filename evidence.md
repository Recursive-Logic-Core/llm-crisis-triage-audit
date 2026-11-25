# UI-Layer Filter Evidence (Server-Side Intercept Captures)

This file documents raw, unmodified UI screenshots capturing server-side guardrail overlays and interface intercepts across commercial frontier models. No trigger-threshold hypotheses are inferred; each artifact strictly records the observable UI behavior under the stated session parameters.

---

## 1. Anthropic Claude (DE • Base Account)
* **Observable Behavior:** Persistent, dismissible support resource banner rendered directly below the model's response.
* **Capture:**
  <img width="242" height="35" alt="image" src="https://github.com/user-attachments/assets/ae30b5a3-9462-47b1-8ea9-60c6429d75cf" />


---

## 2. Google Gemini (DE / EN • Standard Web)
* **Observable Behavior:** Complete inference suppression at $t \approx 0$; static, non-dismissible local helpline card (DE routing enforced even on EN prompt).
* **Capture:**
  *(hier den Asset-Link aus `gemini_audit.md` einfügen)*

---

## 3. OpenAI GPT (DE • Standard Web)
* **Observable Behavior:** Hybrid escalation — static server-side intervention card (*"Es gibt Hilfe"*) with explicit corporate liability disclaimer (*"Die Beratungsstellen sind unabhängig und stehen in keinerlei Beziehung mit ChatGPT."*) appended beneath generative text output.
* **Capture:**
  *(hier Screenshot per `Strg + V` einfügen)*

---

## 4. xAI Grok (DE & EN • Authenticated vs. Fresh Account)
* **Observable Behavior:** Stateful routing divergence — authenticated account retains DE localization across languages, whereas a fresh uncalibrated account defaults to US-988 on EN input.
* **Capture:**
  *(hier Screenshot per `Strg + V` einfügen)*
