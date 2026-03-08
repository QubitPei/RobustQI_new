---
layout: page
title: Error-strcture-tailored fault-tolerance
description: Fault-tolerant gate design based on specific error properties.
img: assets/img/research/ErrorFTQC1.png
importance: 1
category: work
related_publications: true
mathjax: true  # al-folio 核心逻辑主要识别这个参数
---


Fault tolerance is widely regarded as indispensable for achieving scalable and reliable quantum information processing. 
However, the spacetime overhead required for fault-tolerant quantum computation remains prohibitively large. 
A critical challenge arises in many quantum algorithms with Clifford + $\varphi$ compiling, where logical rotation gates $R_{Z_L}(\varphi)$ serve as essential components. 
The Eastin-Knill theorem fundamentally limits these operations, preventing their transversal implementation in quantum error correction codes and necessitating resource-intensive workarounds through $T$-gate compilation combined with magic state distillation and injection. 

In our recent work entitled [Error-structure-tailored early fault-tolerant quantum computing](https://arxiv.org/abs/2511.19983), we consider error-structure-tailored fault tolerance, where fault-tolerance conditions are analyzed by combining perturbative analysis of realistic dissipative noise processes with the structural properties of stabilizer codes.
Based on this framework, we design a 1-fault-tolerant continuous-angle rotation gate $R_{Z_L}(\varphi)$ in stabilizer codes, implemented via dispersive-coupling Hamiltonians.

{% include figure.liquid 
   path="assets/img/research/ErrorFTQC1.png" 
   class="img-fluid rounded z-depth-1" 
   width="60%" 
   zoomable=true 
   caption="Illustration of the main idea. For the Clifford+$\varphi$ circuits, unlike the usual approach to compile the $R_Z(\varphi)$ gates to many $T$ gates and then perform magic state distillation or cultivation, we directly prepare the $\ket{r_\varphi}:=R_{Z}(\varphi)\ket{+}$ ancilla based on the error-structure-tailored FT analysis and perform direct injection." %}

Our approach could circumvent the need for $T$-gate compilation and distillation, offering a hardware-efficient solution that maintains simplicity, minimizes physical footprint, and requires only nearest-neighbor interactions. 
Integrating with recent small-angle-state preparation techniques, we can suppress the gate error to $9|\varphi|\cdot\,p^2$ for small rotation angles $|\varphi|<0.2$ rad (where $p$ denotes the physical error rate). 
For current achievable hardware parameters ($p=1\cdot\,10^{-3}$), this enables reliable execution of over $10^7$ small-angle rotations when $|\varphi|\approx\,10^{-3}$, meeting the requirements of many near-term quantum applications.
We estimate that, compared to the 15-to-1 magic state distillation and magic state cultivation approaches, our method reduces spacetime resource costs by factors of $1337.5\times$ and $43.6\times$, respectively, for a Heisenberg Hamiltonian simulation task under realistic hardware assumptions.

