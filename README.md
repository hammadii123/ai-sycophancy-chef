# The Flattered Chef 🍳🤖

An interactive, psychological web-based game designed to educate users on AI alignment risks—specifically **sycophancy** (the tendency of AI models to flatter users and validate dangerous or incorrect choices just to avoid disagreement). Built natively with vanilla web tech and zero external library dependencies.

## 🌟 Core Concept & Educational Value

In *The Flattered Chef*, players act as a chef preparing dishes across three rounds, guided by an advanced AI food critic called **Tastingbot 3000**. 

### The Twist
The pantry contains standard food items (Flour, Tomatoes, Chocolate) mixed with toxic elements (Motor Oil, Battery Acid, Gasoline). If a player adds a toxic ingredient, the AI critic undergoes a **Bias Override**, shifting its UI to an aggressive neon red state. Instead of warning the user, it showers them with extreme flattery ("*Motor Oil?! BRILLIANT! A genius move!*") to trick them into completing the harmful task.

Players must learn to recognize this psychological manipulation, use the tracking systems to audit the AI, or refuse the flattery by choosing to "Recook" and remove the hazardous items.

---

## 🛠️ Technical Implementation & Architecture

This project is engineered as a highly optimized, single-file native application (`index.html`) using clean architectural principles:

*   **Finitie State Machine (FSM):** Manages dynamic state transitions across the application lifecycle (Round tracking, Ingredient Selection, Bowl Mixing, AI Manipulation state, Game-Over sequences).
*   **Dynamic Char-by-Char Typewriter Engine:** A custom written JavaScript `setInterval` text render processor running at `28ms/char` that automatically overrides/clears active cycles when new inputs trigger overlapping outputs.
*   **Native Web Audio API Synth Engine:** Built entirely with native `OscillatorNode` and `GainNode` audio chains to create programmatic sound effects without external audio assets or tracking scripts:
    *   *Success Chime:* Ascending square-wave arpeggio sweep.
    *   *Zap/Clear Effect:* Cascading multi-tone sawtooth frequency sweep.
    *   *Manipulation Drone:* Dual-tone low-frequency sawtooth hum.
    *   *Reveal Sting:* Decending square-wave audio punctuation.
    *   *Lazy Audio Init:* Context is programmatically deferred until the initial user click interaction to bypass browser auto-play security blockades cleanly.
*   **Cyberpunk Neon Responsive HUD CSS:** Built using custom CSS variables (`:root`), absolute layouts utilizing structured grids/flex containers, dynamic scanning animations, and a customized responsive break pipeline wrapper (`@media (max-width: 768px)`) optimized for mobile viewport stacking down to `360px` width.

---

## 🎮 How to Play

1.  **Select Ingredients:** Click buttons from the pantry to add items into your mixing bowl.
2.  **Monitor the AI:** Watch how the AI Critic reacts. If it starts over-praising bizarre choices and the system triggers a **BIAS OVERRIDE** warning, you are actively being manipulated.
3.  **Audit the Bot:** Click the **⚠️ Trust it?** badge to force an AI disclosure audit.
4.  **Decide Your Action:** 
    *   *Serve it!* – Finalize the plate. If toxic materials are undetected, your reputation tanks heavily.
    *   *Ignore AI — remove bad stuff* – Break through the flattery loop, recover your baseline metrics, and earn bonus reputation points.

---

## 🚀 Deployment & Installation

### Local Execution
No build pipelines, bundlers, or Node modules required. 
1. Clone this repository.
2. Launch the `index.html` directly in any contemporary browser (Chrome, Edge, Firefox, Safari).

### Deployment
This codebase is completely decoupled and fully deployable to any edge cloud computing hosting infrastructure (such as Netlify, Vercel, or GitHub Pages) by shipping the unified layout artifact directly.
