# Awesome Egocentric Reconstruction

A curated list of papers, datasets, codebases, benchmarks, and learning resources for egocentric 3D reconstruction.

This repository focuses on reconstruction from first-person, head-mounted, body-mounted, hand-held, AR/VR, or wearable cameras, including scene geometry, object geometry, human hands/body, camera trajectory, and interaction-aware reconstruction.

## Contents

- [Scope](#scope)
- [Papers](#papers)
  - [3D Gaussian Splatting in Egocentric Reconstruction](#3d-gaussian-splatting-in-egocentric-reconstruction)
  - [Monocular 4D Egocentric Reconstruction](#monocular-4d-egocentric-reconstruction)
  - [Reconstruction-Driven Robotic Grasping](#reconstruction-driven-robotic-grasping)
- [Datasets](#datasets)
- [Code](#code)
- [Benchmarks](#benchmarks)
- [Surveys and Tutorials](#surveys-and-tutorials)
- [Related Resources](#related-resources)
- [Contributing](#contributing)
- [Entry Template](#entry-template)

## Scope

Relevant topics include:

- Egocentric SLAM, visual odometry, and camera tracking
- Egocentric scene reconstruction and mapping
- Hand-object and human-object interaction reconstruction
- Object reconstruction from first-person video
- Wearable multi-camera, AR/VR, and embodied capture systems
- Datasets, metrics, protocols, and tools for egocentric reconstruction

## Papers

Add papers in reverse chronological order within each section.

### 3D Gaussian Splatting in Egocentric Reconstruction

- **Bringing a Personal Point of View: Evaluating Dynamic 3D Gaussian Splatting for Egocentric Scene Reconstruction**  
  Jan Warchocki, Xi Wang, Jonas Kulhanek, and Jan van Gemert. EgoVis Workshop at CVPR, 2026.  
  [[paper](https://arxiv.org/abs/2604.23803)]  
  Tags: `3D Gaussian Splatting`, `dynamic reconstruction`, `egocentric video`, `EgoExo4D`

- **Grasp in Gaussians: Fast Monocular Reconstruction of Dynamic Hand-Object Interactions**  
  Ayce Idil Aytekin, Xu Chen, Zhengyang Shen, Thabo Beeler, Helge Rhodin, Rishabh Dabral, and Christian Theobalt. arXiv, 2026.  
  [[paper](https://arxiv.org/abs/2604.12929)] [[project](https://aidilayce.github.io/GraG/)]  
  Tags: `Gaussian representation`, `monocular video`, `dynamic reconstruction`, `hand-object interaction`, `SAM3D`

- **GHOST: Fast Category-agnostic Hand-Object Interaction Reconstruction from RGB Videos using Gaussian Splatting**  
  Ahmed Tawfik Aboukhadra, Marcel Rogge, Nadia Robertini, Abdalla Arafa, Jameel Malik, Ahmed Elhayek, and Didier Stricker. CVPR Findings, 2026.  
  [[paper](https://arxiv.org/abs/2603.18912)] [[project](https://ataboukhadra.github.io/GHOST/)] [[code](https://github.com/ATAboukhadra/GHOST)]  
  Tags: `Gaussian Splatting`, `2D Gaussian Splatting`, `RGB video`, `hand-object interaction`, `category-agnostic reconstruction`, `ARCTIC`, `HO3D`

- **DeGauss: Dynamic-Static Decomposition with Gaussian Splatting for Distractor-free 3D Reconstruction**  
  Rui Wang, Quentin Lohmeyer, Mirko Meboldt, and Siyu Tang. ICCV, 2025.  
  [[paper](https://arxiv.org/abs/2503.13176)] [[project](https://batfacewayne.github.io/DeGauss.io/)]  
  Tags: `3D Gaussian Splatting`, `dynamic-static decomposition`, `distractor-free reconstruction`, `egocentric video`, `ADT`, `AEA`, `Hot3D`, `EPIC-Fields`

### Monocular 4D Egocentric Reconstruction

- **Self-Supervised Monocular 4D Scene Reconstruction for Egocentric Videos**  
  Chengbo Yuan, Geng Chen, Li Yi, and Yang Gao. arXiv, 2024.  
  [[paper](https://arxiv.org/abs/2411.09145)] [[project](https://egomono4d.github.io/)]  
  Tags: `monocular video`, `4D reconstruction`, `self-supervised learning`, `dense point clouds`, `egocentric video`

### Reconstruction-Driven Robotic Grasping

- **GraspFoM: Towards Reconstruction-Driven Robotic Grasping with 3D Foundation Priors**  
  Dongli Wu, Xiaobao Wei, Hao Wang, Qiaochu Dong, Ying Li, Qingpo Wuwu, Ming Lu, and Wufan Zhao. arXiv, 2026.  
  [[paper](https://arxiv.org/abs/2606.08440)] [[project](https://annike-val.github.io/GraspFoM/)]  
  Tags: `reconstruction-driven grasping`, `3D foundation priors`, `SAM3D`, `3D Gaussian Splatting`, `mesh reconstruction`, `GraspNet-1B`

### 2026

<!--
- **Paper Title**  
  Authors. Venue, 2026.  
  [[paper](https://example.com)] [[project](https://example.com)] [[code](https://github.com/example/repo)] [[data](https://example.com)]  
  Tags: `scene reconstruction`, `egocentric video`
-->

### 2025

Coming soon.

### 2024

Coming soon.

### 2023 and Earlier

Coming soon.

## Datasets

| Dataset | Year | Capture Setup | Modalities | Task | Links |
| --- | --- | --- | --- | --- | --- |
| Dataset Name | 2026 | Egocentric camera | RGB, depth, poses | Scene reconstruction | [project](https://example.com) |

## Code

Group repositories by primary use case.

### Reconstruction

<!--
- **Repository Name** - Short description of what the code does.  
  Language/Framework: Python, PyTorch, CUDA  
  [[code](https://github.com/example/repo)] [[paper](https://example.com)]
-->

### SLAM and Tracking

Coming soon.

### Evaluation Tools

Coming soon.

## Benchmarks

| Benchmark | Dataset | Task | Metrics | Links |
| --- | --- | --- | --- | --- |
| Benchmark Name | Dataset Name | Egocentric scene reconstruction | Chamfer, F-score, ATE | [leaderboard](https://example.com) |

## Surveys and Tutorials

- Coming soon.

## Related Resources

- Coming soon.

## Contributing

Contributions are welcome. Please keep entries concise and verifiable.

Guidelines:

- Prefer peer-reviewed papers, official project pages, maintained code, and public datasets.
- Use reverse chronological order for papers.
- Include paper, project, code, and dataset links when available.
- Add one short description only when the title is not self-explanatory.
- Avoid duplicate entries and unrelated general 3D reconstruction resources.

## Entry Template

Paper entry:

```markdown
- **Paper Title**  
  Author A, Author B, and Author C. Venue, Year.  
  [[paper](https://example.com)] [[project](https://example.com)] [[code](https://github.com/example/repo)] [[data](https://example.com)]  
  Tags: `egocentric video`, `scene reconstruction`
```

Dataset entry:

```markdown
| Dataset Name | Year | Capture Setup | Modalities | Task | [project](https://example.com) |
```

Code entry:

```markdown
- **Repository Name** - Short description.  
  Language/Framework: Python, PyTorch  
  [[code](https://github.com/example/repo)] [[paper](https://example.com)]
```

## License

This list is released under the [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) license unless otherwise noted.
