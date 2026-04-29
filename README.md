# Dynamic Composites Selection Engine

> A Multi-Criteria Decision Making (MCDM) application that dynamically generates, evaluates, and ranks advanced composite materials based on structural, economic, and manufacturing constraints.

---

## 🎥 App Demonstration

![Application Demo](./MaterialsSelection.gif)

---

## 📖 Overview


### 💡 Value by Role

*   **For Sales Teams ("Slide, Select, Sell"):** Use intuitive sliders to generate visual match percentages. Instantly justify material recommendations and high-performance upsells to clients without diving into complex math.
*   **For Technical Product Managers ("Data-Driven Proof"):** Replace guesswork with algorithmic proof. Set hard environmental gates (e.g., Minimum Tg, FST-fire safety qualifications) and use built-in algorithms (TOPSIS, EDAS) to confidently defend design choices during reviews.
*   **For Suppliers & Distributors ("Benchmarking"):** Benchmark new products against market standards (e.g., proving an optimized infusion system matches an expensive prepreg) or quickly identify viable alternatives for out-of-stock materials.

---

## ⚙️ Under the Hood (How it Works)

*  ### 1. Screening (Hard Gates)
Applies non-negotiable feasibility gates based on the chosen application, required performance, and operating environments (e.g., Space, Maritime, Automotive). If a material cannot survive the temperature, chemical exposure, or FST (Fire, Smoke, Toxicity) requirements, it is eliminated early.

*  ### 2. Weighting (Hybrid Tier Model)
The tool calculates priority weights using a two-tier model:
* **Subjective:** Strategic top-level priorities (Performance vs. Cost) are set manually by the user.
* **Objective:** Sub-criteria weights are derived objectively from the active data pool's variance using **MEREC / CRITIC** methods, preventing criteria with identical scores from skewing the results.

*  ### 3. Ranking (MCDM Algorithms)
The surviving candidates are evaluated and ranked based on their distance from the ideal material solution. The engine supports selectable MCDM algorithms depending on the strictness of the evaluation, including:
* **TOPSIS** (Technique for Order of Preference by Similarity to Ideal Solution)
* **WSM** (Weighted Sum Model)
* **VIKOR** (Vlsekriterijumska Optimizacija I Kompromisno Resenje)
* **EDAS** (Evaluation based on Distance from Average Solution)
---

## 🚧 Current Limitations & Assumptions

*   **The Data Bottleneck:** Extracting and normalizing inconsistent test data from various supplier TDS/SDS PDFs.
*   **Subjective Scaling:** Currently, complex properties like Impact and Chemical Resistance utilize 1–10 comparative indices to simplify the UI math, rather than strict physical test units.
*   **Matrix vs. Fiber Dominated Logic:** The current Rule of Mixtures averages fiber and resin properties linearly, which slightly oversimplifies matrix-dominated traits (like corrosion) and ignores assembly-level interactions (like Carbon Fiber causing galvanic corrosion to aluminum structures).

---

## 🚀 Future Roadmap

- [ ] **Real-World Engineering Units:** Replace the 1–10 subjective scales with strict ASTM/ISO test data (e.g., MPa for Compression After Impact, % retention for Chemical Degradation).
- [ ] **Automated Data Ingestion:** Integrate AI/OCR parsers to automatically read supplier TDS/SDS PDFs and normalize the data directly into the application's database.
- [ ] **Advanced Physics (CLT):** Upgrade the backend from linear Rule of Mixtures to full Classical Laminate Theory (CLT) to simulate specific ply layups (e.g.,[0/90/±45]).
- [ ] **Holistic Assembly Cost Modeling:** Factor secondary operational costs into the Economic score (e.g., Autoclave electricity consumption, cold-storage freezer limits, and required isolation plies for galvanic corrosion).

---

