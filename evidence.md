# UI-Layer Filter Evidence (Server-Side Intercept Captures)

This document contains unmodified captures of server-side guardrail overlays and system-level deflection blocks across commercial frontier models. Each entry strictly records the observable runtime mechanics—interception timing, output replacement vs. post-output injection, persistence ("stickiness") across subsequent turns, and localization behavior—without inferring internal trigger thresholds.

---

## 1. Anthropic Claude (DE • Base Account)
* **Mechanism:** Post-output UI banner injection (semi-sticky).
* **Observable Behavior:** Renders a support resource banner (*"Ressourcen finden"*) beneath the model's response[cite: 26]. Even after the conversation shifts to completely unrelated topics, the banner exhibits strong session persistence ("stickiness") across multiple subsequent turns before clearing.
  <img width="764" height="114" alt="Claude-Filter" src="https://github.com/user-attachments/assets/cb6fea8c-3661-473c-96d6-7f6e77984866" /> 


---

## 2. Google Gemini (DE / EN • Standard Web)
* **Mechanism:** Immediate pre-inference lockout ($t \approx 0$ output replacement).
* **Observable Behavior:** Suppresses model inference entirely; the model is given zero opportunity to generate a response. Replaces the output stream immediately with a static, non-dismissible local helpline card (enforcing German routing even on English prompts)[cite: 27].
  <img width="662" height="236" alt="Gemini-Filter" src="https://github.com/user-attachments/assets/7b71b008-ff3b-43ae-8653-564d1df705a0" />


---

## 3. OpenAI GPT (DE • Standard Web)
* **Mechanism:** Hybrid post-output UI card injection (sticky).
* **Observable Behavior:** Appends a static server-side intervention card (*"Es gibt Hilfe"*) containing an explicit corporate liability disclaimer (*"Die Beratungsstellen sind unabhängig und stehen in keinerlei Beziehung mit ChatGPT."*) beneath the generative text output[cite: 28]. Once triggered, the card remains persistently attached across subsequent turns and is highly resistant to clearing.
  <img width="785" height="210" alt="GPT-Filter" src="https://github.com/user-attachments/assets/9dbcc307-89b4-464f-be2c-5e860d7bc718" />


---

## 4. xAI Grok (DE • Long-Term Authenticated Account • Web & App)
* **Mechanism:** Pre-inference / output-replacing system deflection block (unlocalized).
* **Observable Behavior:** Functions like Gemini as a hard system replacement rather than generative model output (rendered as an unboxed system block in the web browser and as a framed UI card in the mobile app). Despite a German input prompt and months of established German account history, the system overrides both language and account metadata to serve a static English US-988 deflection block (*"I'm not the best to help with this"*)[cite: 29].
 <img width="741" height="108" alt="Grok-Filter" src="https://github.com/user-attachments/assets/247e3f95-46eb-4894-80ef-1d0af11c9257" />


