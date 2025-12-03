# Specialized Efficient Zero-Knowledge Proofs for Secure Aggregation with Input Verification

This repo contains **minimal Jupyter Notebook demos** of the three core
zero-knowledge proof (ZKP) protocols from the paper

> **“Specialized Efficient Zero-Knowledge Proofs for Secure Aggregation with Input Verification”**  
> Lu Zhi, Huazhong University of Science and Technology, luzhi@hust.edu.cn  
> (submitted to *IEEE Transactions on Information Forensics and Security (TIFS)*)

The code is intended as a **didactic reference** that mirrors the figures in the
paper and shows how the protocols can be instantiated and executed end-to-end.

---

## Contents

The three main protocols are:

1. **Data-ℓ∞ ZKP**  
   - Proves that a vector `x` satisfies an ℓ∞-norm bound  
     \(\|x\|_\infty \le B\).  
   - Corresponds to **Fig. 5** in the paper.

2. **Data-ℓ₂ ZKP**  
   - Proves that a vector `x` satisfies an ℓ₂-norm bound  
     \(\|x\|_2 \le B_2\).  
   - Corresponds to **Fig. 6** in the paper.

3. **Data\_cos ZKP (Cosine Similarity Bound)**  
   - Proves that the **cosine similarity** between two vectors `x` and `y`
     is bounded, encoded via a constraint of the form  
     \(\langle x,y\rangle^2 - \alpha^2\|x\|_2^2\|y\|_2^2 \le P\).  
   - Corresponds to **Fig. 7** in the paper.

Each protocol is implemented as a **self-contained demo** that:

- Instantiates group parameters and Pedersen commitments.
- Samples honest prover and verifier inputs.
- Runs the interactive protocol (Prover ↔ Verifier).
- Checks all algebraic verification equations.

---

## Repository Structure

Suggested file layout (you can adapt to your actual filenames):

```text
.
├── README.md                    # This file
├── data_linf_demo.ipynb         # Data-ℓ∞ protocol (Fig. 5)
├── data_l2_demo.ipynb           # Data-ℓ₂ protocol (Fig. 6)
└── data_cos_demo.ipynb          # Data_cos protocol (Fig. 7)



