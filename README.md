# ROGUE-Zip: Recursive Ontology-Guided Sparse Zipping

**A Neuro-Symbolic architecture for "un-smearing" the black box and enabling continual learning.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

-----

## 📖 The Problem

Artificial Intelligence is currently fractured between two incompatible paradigms.

* **Symbolic AI (Ontologies):** Defined by clarity and structure. Representations are localist (one node = one concept). They are interpretable and infinitely extensible but brittle in the face of real-world noise.
* **Neural Networks (Deep Learning):** Masters of noise and distributed patterns. But they are opaque black boxes. Knowledge is "smeared" across millions of weights in a holographic fog, making them uninterpretable and prone to **Catastrophic Forgetting** when learning new tasks.

**ROGUE-Zip** asks: Can we combine the structure of an Ontology with the power of a Neural Network? Can we force a neural network to organize itself into discrete, interpretable "blocks" instead of a distributed mess?

## 💡 The Solution: The "Handover Protocol"

ROGUE-Zip attempts to solve this by implementing a synthetic version of biological **Systems Consolidation** (the process where the brain moves memories from short-term to long-term storage during sleep).

The core mechanism is the **Handover Protocol**:

1.  **Train (Acquisition):** A top network layer (e.g., Block 4) learns a specific concept defined by an ontology (e.g., "L2 Categories").
2.  **Zip (Consolidation):** We apply a mathematical pressure to force that layer's weight matrix to become an **Identity Matrix** (a perfect diagonal line).
3.  **Handover:** As the layer transforms into a simple "pass-through" wire ($f(x)=x$), the logic it contained is forced down into the lower "trunk" layers.
4.  **Reset:** The top layer is now empty and ready to learn a new concept without overwriting the foundation.

This process aims to physically sequester knowledge deep in the network, building a neural brain that grows layer by layer, concept by concept.

-----

## 🔬 The Apparatus: HCL Trainer v8

To validate the physics of this novel approach, standard black-box libraries like PyTorch were insufficient. We needed to *see* the weight matrices evolving in real-time to verify that the "Zipping" was structurally real and not just a statistical illusion.

This repository hosts **The HCL Trainer v8**, a custom, "transparent-box" neural network engine written entirely in vanilla JavaScript. It visualizes every weight matrix, activation vector, and accuracy metric live in the browser.

-----

## 🚀 Getting Started

### Running the Demo Live

The easiest way to experience ROGUE-Zip is to run the hosted visualization:

👉 **[Launch the HCL Trainer v8 Live Demo](https://matthewfurnari.github.io/ROGUE-zip/)**

### Running Locally

Because the entire engine is contained in a single HTML file, running it locally is trivial.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/matthewfurnari/ROGUE-zip.git](https://github.com/matthewfurnari/ROGUE-zip.git)
    ```
2.  **Open the file:**
    Navigate to the folder and double-click `index.html` to open it in your web browser (Chrome, Firefox, or Edge recommended).

-----

## 🧪 Interactive Experiments

The HCL Trainer puts you in control of the curriculum. Use the manual controls to replicate our key findings.

### Experiment A: The Success (Residual Learning)

*Goal: Show that the network can remember a general concept while learning a specific one.*

1.  Set **Mode** to `TRAIN` and **Level** to `L2: Coarse Groups (6)`.
2.  Click **START** and train until accuracy is >98%.
3.  Pause, switch **Mode** to `ZIP (Handover)`, and **RESUME**. Wait for the "Zip Identity Pressure" bar to reach 100% and the weights to look diagonal.
4.  Pause, switch **Mode** back to `TRAIN`, and set **Level** to `L3: Subgroups (48)`.
5.  **RESUME** and watch the graph.
    * *Observation:* The Green line (L2 Accuracy) should stay high (~90%) even as the Blue line (L3 Accuracy) rises. The trunk has retained the foundational knowledge.

### Experiment B: The Failure (Interference)

*Goal: Understand the importance of curriculum order.*

1.  Reset the page.
2.  Train and Zip on `L1: Moves vs. Static (2)`.
3.  After Zipping, switch to train on `L2: Coarse Groups (6)`.
4.  *Observation:* Watch the L1 accuracy crash. The rigid "Motion" foundation is incompatible with the "Category" task, leading to catastrophic interference.

-----

## ⚙️ Technical Details

For a deep dive into the mathematics, optimization stability (gradient clipping, extended ramps), and topological considerations (Leaky ReLU vs. Standard ReLU), please see the **[Technical Deep Dive](https://www.intelligencefactory.ai/blog/rogue-zip-recursive-ontology-guided-sparse-zipping-protocol)**

## 🗺️ Roadmap & Future Work

* **Solving Interference:** Implementing **Group Lasso** to create sparse "neural reservations," ensuring orthogonal tasks do not fight for the same neurons.
* **Scaling Up:** Testing the protocol on larger datasets (CIFAR-100) and deeper architectures to evaluate stability at scale.
* **Recursive Zipping:** Enabling multi-stage zipping (e.g., L3 -> Zip -> L2 -> Zip -> L1) to test the ultimate compression efficiency of the trunk.

## 🤝 Contributing

This is an experimental project, and we welcome contributions, critiques, and replications.

* Found a curriculum that breaks the Zip? Open an issue.
* Have an idea for a better sparsity implementation? Submit a pull request.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

-----

*Created by Matthew Furnari.*
