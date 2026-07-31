---
title: "Aggregating Partitioned Data"
section: working
date: 2026-04-20
coauthors:
  - name: "Chiu Yu Ko"
    url: "https://kochiuyu.github.io"
presentations:
  - name: "the 2026 Greater Bay Area Economics Conference"
    url: "https://sites.google.com/view/2026-gbaec"
  - name: "the 18th Meeting of the Society for Social Choice and Welfare"
---

This paper addresses a central challenge in composite index construction: aggregating data partitioned by exogenous constraints such as cost, privacy, or administrative reporting. Standard additive approaches (e.g., weighted arithmetic means) are systematically biased when the true weightings are non-additive to capture synergies and redundancies across dimensions. We develop a family of non-additive aggregation methods by extending traditional capacities to partitioned data (represented by P), introducing P-restricted decomposition integrals, including the P-restricted concave integral and the P-restricted Choquet integral. We axiomatically characterize the two principal members. The P-restricted concave integral, which optimizes over all feasible within-block allocations, is characterized by a central axiom called Information Monotonicity: coarser data never reduces the index, embodying a “benefit of the doubt” principle. The P-restricted Choquet integral, which restricts attention to chain-based decompositions, is characterized by P-Stochastic Dominance. We show that these axioms are fundamentally incompatible for any non-degenerate integral, revealing a sharp axiomatic divide within the family. The framework applies to composite indices built from partitioned data, such as ESG ratings, GDP measurement with cross-sector interactions, and welfare measures across different family compositions. Applying it to MSCI ESG ratings, we find that the concave–Choquet gap grows monotonically with partition coarseness, that the non-additive integrals refine rather than overturn the additive baseline, and that the pillar-level P-restricted integrals generate consistent reversal rates across industries.
