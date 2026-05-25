# Project Progress & Experimentation Matrix

## 📊 Completed Baseline Metrics (Reference Data for LaTeX/Poster)
*No experiments have run yet. Project is starting from an absolute clean state.*

---

## 🗺️ Master Roadmap

- [ ] **Phase 1: Environment & Baseline Dual-Stream Architecture Setup**
  - Initialize the local workspace and verify GPU accelerator state via `uv`.
  - Construct an extraction pipeline using MediaPipe to output BOTH 64x64 grayscale mouth arrays and normalized $(x, y)$ coordinate matrix graphs.
  - Build the core Dual-Stream Asymmetric network (GCN Stream + 3D-CNN Stream + Concatenation Fusion Layer + Bi-GRU).
  - Execute a baseline training loop using CTC Loss and log initial training curves.
  - Implement a basic greedy decoding validation script.

- [ ] **Phase 2: Systematic Stream Ablation Testing**
  - Create isolated training scripts to train Stream A (GCN Geometry Only) and Stream B (3D-CNN Pixels Only) independently.
  - Run experiments to collect clean, comparative loss and accuracy metrics showing how fusion outperforms isolated modalities.
  - Test optimization variations like dynamic learning rate scheduling (`ReduceLROnPlateau`).

- [ ] **Phase 3: Cognitive Language Decoding Upgrade**
  - Integrate token/character tracking compilation decoders (e.g., `torchaudio`).
  - Upgrade inference mechanics from greedy decoding to multi-hypothesis Beam Search Decoding.
  - Measure how effectively the language contextual framework resolves viseme ambiguities compared to the raw baseline.

- [ ] **Phase 4: Dataset Scale-Up & Linguistic Generalization**
  - Pivot pipelines to open-access multi-speaker or sentence-level collections.
  - Migrate vocabulary dimensions to complete character-level prediction matrices (`a-z` and space token sets).

- [ ] **Phase 5: Academic Delivery Consolidation**
  - Extract logged metric arrays from `results/` to render matplotlib training curves.
  - Generate full LaTeX text files using the university template.
  - Populate the CVPR-style presentation poster blocks.