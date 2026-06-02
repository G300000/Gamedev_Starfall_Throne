# ⚔️ Starfall Throne: The Oracle's Gambit

An atmospheric, cyber-gothic tactical card duel built entirely with vanilla web technologies (**HTML5**, **CSS3**, and **JavaScript**). In **Starfall Throne**, players manage a persistent, floating mana pool and battle a highly strategic, predictive AI subsystem known as **The Oracle's Eye**. Counter the Oracle's calculations, navigate the rule adjustments, and keep your tower standing across 15 rounds of high-stakes combat.

---

## 🕹️ Game Core & File Structure

The project features zero external dependencies, build configurations, or heavy framework packages. It is composed of three interconnected files:

*   **`index.html`**: Establishes the semantic markup of the layout, structural game dashboards, modal overlays, SVG assets for the Oracle Eye graphics, and layout guides[cite: 1].
*   **`style.css`**: Defines the dark cyber-gothic color design system, flexible multi-row grid architecture, hover transformations, layout animations, and background star rendering systems[cite: 2].
*   **`script.js`**: Orchestrates the round-based state machinery, structural rendering loops, probabilistic calculation engines, and dynamic audio synthesizer layout[cite: 3].

---

## 📖 Game Rules & The Power Cycle

The game revolves around an asymmetric interaction dynamic where higher-tier cards demand heavier mana resources but deal less devastating structural damage to the enemy tower[cite: 1, 3].

### 🔄 The Power Cycle Breakdown
*   **♚ King**: Costs `6 Mana` | Deals `75 Damage`[cite: 1, 3]. Defeats Queen and Jack[cite: 1, 3]. Loses to Ace[cite: 1, 3].
*   **♛ Queen**: Costs `4 Mana` | Deals `100 Damage`[cite: 1, 3]. Defeats Jack and Ace[cite: 1, 3]. Loses to King[cite: 1, 3].
*   **♞ Jack**: Costs `3 Mana` | Deals `125 Damage`[cite: 1, 3]. Defeats Ace[cite: 1, 3]. Loses to King and Queen[cite: 1, 3].
*   **✦ Ace**: Costs `2 Mana` | Deals `150 Damage`[cite: 1, 3]. **Counters King ONLY**[cite: 1, 3]. Loses to Queen and Jack[cite: 1, 3].
*   **⚖️ Identical Card Draws**: Playing matching card ranks prompts a standoff[cite: 1, 3]. Both cards return safely to their respective hands without dealing tower damage[cite: 1, 3].
*   **💥 Ace vs. Ace**: A catastrophic mirror explosion[cite: 1, 3]. Both cards are instantly destroyed (*dumped*), both players suffer `-200 HP`, and hands refill from reserves[cite: 1, 3].
*   **🏳️ Tactical Pass**: Skipping a turn inflicts a loss penalty of `-50 HP` to the passer, but returns your card selection safely to your active hand structure[cite: 1, 3].

### ⏳ Resource & Attrition Rules
*   **Tower Vitality**: Both towers start at `500 HP`[cite: 1, 3]. The game continues for a maximum of `15 Rounds`[cite: 1, 3].
*   **Floating Mana Pool**: Mana starts at `5`, gaining `+3` continuously every round up to a hard cap of `10`[cite: 1, 3]. Mana accumulates continuously and never resets[cite: 1, 3].
*   **Symmetric Attrition**: 
    *   Winning a clash returns your card safely to your hand[cite: 1, 3]. The opponent's card is permanently discarded (*dumped*), and their reserve count decreases[cite: 1, 3].
    *   Losing a clash permanently eliminates your card slot[cite: 1, 3]. Your active hand layout is replenished from your hidden `Reserve Pile` until empty[cite: 1, 3].

---

## 👁️ The Oracle's Eye: Variable Elimination Engine

The standout technical implementation is **The Oracle's Eye**—a real-time probability forecast model that surfaces what card the AI is calculated to play next[cite: 1, 3].

The `computeEnemyProbs()` algorithm leverages variable elimination to filter out choices using real-time constraints[cite: 3]:
1.  **Archetype Volume Tracking**: Tracks remaining available elements within the sealed starter deck pool (`3 Kings, 3 Queens, 2 Jacks, 2 Aces`) by assessing historical discards (*Oracle Dumped*)[cite: 1, 3].
2.  **Resource Exclusion**: Instantly eliminates card options that exceed the enemy's current floating mana threshold[cite: 1, 3].
3.  **Aggression Weight Scaling**: Evaluates tower health ratios[cite: 3]. When the Oracle's tower drops below critical limits (`<35% HP`), calculation weights scale aggressively toward massive damage outputs (like Jacks and Aces) to optimize counter-attack paths[cite: 3].

Meanwhile, the AI's selection layer balances this strategy[cite: 3]. It spends `75%` of its processing trying to counter the player's statistically likely cards, while reserving a `25%` random variance to remain unpredictable and avoid easy counter-plays[cite: 3].

---

## 🔊 Interactive Synth Audio Engine

This project features a fully programmatic, real-time battle theme generated entirely via the **Web Audio API** within `script.js`[cite: 3]:
*   **No Media Files**: Sound design uses zero external audio assets, keeping repository sizes light and load times instantaneous[cite: 3].
*   **Rhythmic Architecture**: Generates a fast driving rhythm (~158 BPM) complete with synthetic basslines, synthesized hi-hat noise, square-wave counter-melodies, and electronic snare drums[cite: 3].
*   **Dynamic Sound FX Contexts**: Emits dedicated acoustic synthesizer sound cues tailored to game states, such as player selection clicks (`select`), target triumphs (`win`), tactical defaults (`pass`), or damage impacts (`lose`)[cite: 3].

---

## 🚀 Quick Setup & Deployment

Because this project is built using native web code, it requires **zero build setups, installation packages, or node servers**[cite: 1, 2, 3].

1.  Clone this repository locally:
```bash
    git clone [https://github.com/your-username/starfall-throne.git](https://github.com/your-username/starfall-throne.git)
    ```
2.  Launch the setup:
    *   Open `index.html` directly inside any web browser of your choice[cite: 1].
    *   Alternatively, serve it through a text editor utility such as VS Code's **Live Server** extension.
