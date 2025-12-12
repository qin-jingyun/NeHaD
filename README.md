<div align="center">

# Neural Hamiltonian Deformation Fields for<br>Dynamic Scene Rendering

[![Conference](https://img.shields.io/badge/SIGGRAPH_Asia-2025-blue.svg)](https://asia.siggraph.org/2025)
[![arXiv](https://img.shields.io/badge/arXiv-2512.10424-b31b1b.svg)](https://arxiv.org/abs/2512.10424)
[![Project Page](https://img.shields.io/badge/Project-Page-green.svg)](https://qin-jingyun.github.io/NeHaD/)
[![Video](https://img.shields.io/badge/Video-YouTube-FF0000.svg?logo=youtube&logoColor=white)](https://youtu.be/5MwP_wGIUVA)

[![Poster](https://img.shields.io/badge/Poster-PDF-orange.svg)](https://qin-jingyun.github.io/NeHaD/assets/poster.pdf)
[![Slide](https://img.shields.io/badge/Slide-PDF-yellow.svg)](https://qin-jingyun.github.io/NeHaD/assets/slide.pdf)
[![License](https://img.shields.io/badge/License-MIT-yellowgreen.svg)](LICENSE)
[![Email](https://img.shields.io/badge/Contact-Email-blue.svg)](mailto:hailong.qin@bupt.edu.cn)

[Hai-Long Qin](https://scholar.google.com/citations?user=N33wbdEAAAAJ)¹, [Sixian Wang](https://scholar.google.com/citations?user=f9s8H6UAAAAJ)², [Guo Lu](https://scholar.google.com/citations?user=R9iwlJcAAAAJ)², [Jincheng Dai](https://scholar.google.com/citations?user=0I_YtFsAAAAJ)¹

¹ Beijing University of Posts and Telecommunications (BUPT)  
² Shanghai Jiao Tong University (SJTU)

</div>

<div align="justify">

## ⚡ TL;DR

We reformulate dynamic Gaussian deformation as Hamiltonian dynamics, enabling neural networks to learn physical conservation laws directly from data.

- **Hamiltonian Neural Network Decoder**
  Learn energy-conserving deformation fields through symplectic gradients, replacing purely data-driven MLPs with physics-informed inductive biases.
- **Boltzmann Equilibrium Decomposition**
  Adaptively separate static and dynamic Gaussians via soft masks based on their deviation from spatial-temporal equilibrium states.
- **Physics-Informed Constraints**
  Ensure long-term stability through symplectic integration for position dynamics and local rigidity regularization for rotation dynamics.

</div>

<p align="center">
  <img src="./images/nehad.svg" alt="Teaser Figure" style="width:100%">
</p>

<div align="justify">

## 📖 Abstract

Representing and rendering dynamic scenes with complex motions remains challenging in computer vision and graphics. Recent dynamic view synthesis methods achieve high-quality rendering but often produce physically implausible motions. We introduce NeHaD, a neural deformation field for dynamic Gaussian Splatting governed by Hamiltonian mechanics. Our key observation is that existing methods using MLPs to predict deformation fields introduce inevitable biases, resulting in unnatural dynamics. By incorporating physics priors, we achieve robust and realistic dynamic scene rendering. Hamiltonian mechanics provides an ideal framework for modeling Gaussian deformation fields due to their shared phase-space structure, where primitives evolve along energy-conserving trajectories. We employ Hamiltonian neural networks to implicitly learn underlying physical laws governing deformation. Meanwhile, we introduce Boltzmann equilibrium decomposition, an energy-aware mechanism that adaptively separates static and dynamic Gaussians based on their spatial-temporal energy states for flexible rendering. To handle real-world dissipation, we employ second-order symplectic integration and local rigidity regularization as physics-informed constraints for robust dynamics modeling. Additionally, we extend NeHaD to adaptive streaming through scale-aware mipmapping and progressive optimization. Extensive experiments demonstrate that NeHaD achieves physically plausible results with a rendering quality-efficiency trade-off. To our knowledge, this is the first exploration leveraging Hamiltonian mechanics for neural Gaussian deformation, enabling physically realistic dynamic scene rendering with streaming capabilities.

## 🔥 Dynamic Rendering Showcase

The video [here](./assets/demo.mp4) demonstrates the qualitative rendering results on D-NeRF, HyperNeRF, and DyNeRF datasets. You can download the full-resolution demo video via this [Google Drive link](https://drive.google.com/uc?export=download&id=1WS3uVbFnLJyFXuTVC-znIASx7n4Bep87).

<!-- <p align="center">
  <a href="./assets/demo.mp4">
    <img src="https://placehold.co/1280x720/000000/FFFFFF/png?text=▶+Watch+Demo+Video&font=roboto" alt="Watch Demo Video" style="width:100%; border-radius: 8px;">
  </a>
</p> -->

## 🎤 SIGGRAPH Asia 2025 Presentation

For more details on NeHaD, please refer to our conference presentation.

<p align="center">
  <a href="https://youtu.be/5MwP_wGIUVA">
    <img src="https://img.youtube.com/vi/5MwP_wGIUVA/maxresdefault.jpg" alt="SIGGRAPH Presentation" style="width:100%; border-radius: 8px;">
  </a>
</p>

## 📝 Citation

If you find this work helpful, please consider citing:

```bibtex
@inproceedings{qin-nehad,
    title = {Neural Hamiltonian Deformation Fields for Dynamic Scene Rendering},
    author = {Qin, Hai-Long and Wang, Sixian and Lu, Guo and Dai, Jincheng},
    booktitle = {SIGGRAPH Asia 2025 Conference Papers},
    pages = {1--11},
    year = {2025}
}