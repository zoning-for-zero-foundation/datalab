# Contributing to zzproxies

Thank you for contributing to the **Epistemological Bridge**! We welcome transdisciplinary contributions that help manifest and verify urban climate impacts.

---

## 🏛️ The Gold Standard: Impact-Verified Zoning

To maintain scientific and technical integrity, every contribution must satisfy the **Triple-V** criteria:
1.  **Validation:** Blueprints must be proven against empirical "Ground Truth" data.
2.  **Verification:** Proxies must align with recognized scientific standards (ISO, EN, SSRN).
3.  **Visibility:** Logic must be documented with layman-accessible descriptions and citations.

---

## 🛠️ Developing New Blueprints (`blueprints.py`)

A Blueprint is a self-contained **Discovery Design**. It is responsible for the transition from raw data to standardized **Urban Planning Data (UPD)**.

### Technical Requirements:
* **Class-Based:** Must be an encapsulated class.
* **Atomic:** Must contain its own private helper methods (fetching, local joins).

## 🧪 Developing New Proxies (`models.py`)
A Proxy is a **Verification Model**. It calculates the climate impact of a specific Blueprint's output.

### Technical Requirements:
* **Module-Based:** Must be a Python function which can be used as module.
* **Atomic:** Must contain its own private helper methods.
* **Standardized Output:** The `.run()` method must return a list of dictionaries containing at least: 
`proxy_value`, `proxy_unit`, and `GWP_level`.

**Scientific Requirements:**
- Functional: Must be a pure, stateless function.
- Auditable: Must include a methodology key in the output citing a specific standard.
- Geographic Guard: Must be registered with a CoverageLimit defining where the math is valid.

## 🔄 The Pull Request Process
1. Experiment: Develop your logic in a datalab notebook.
2. Refactor: Move your Class to blueprints.py and your Function to models.py.
3. Test: Add a test case to tests/test_registry.py ensuring the linkage is valid.

Document: Add a .md file (named like your Class function for proxy) to the docs/ folder explaining the scientific basis for your impact metric.

Submit: Open a PR. Our Scientific Advisory Board (SAB) will review for both code and scientific contextual integrity.