# Awesome Hand-Object Interaction

A curated list of papers, datasets, codebases, benchmarks, and learning resources for 3D hand-object interaction reconstruction.

This repository focuses on reconstructing hands together with the objects they interact with — including hand pose, shape, and mesh, object geometry and 6D pose, contact, and jointly disentangled hand-object reconstruction — from single images and monocular, multi-view, or egocentric video.

## Contents

- [Scope](#scope)
- [Papers](#papers)
  - [Single-Image Reconstruction](#single-image-reconstruction)
  - [Monocular Video Reconstruction](#monocular-video-reconstruction)
  - [Others](#others)
- [Contributing](#contributing)
- [Entry Template](#entry-template)

## Scope

Relevant topics include:

- Joint 3D/4D reconstruction of hands and interacting objects
- Hand pose, shape, and mesh recovery in interaction settings
- Template-free and category-agnostic object reconstruction during interaction
- Contact modeling, grasp-aware and physically consistent reconstruction
- Hand-object and interactive segmentation
- Bimanual and dexterous hand-object interaction
- Datasets, metrics, protocols, and tools for hand-object interaction

## Papers

Papers are grouped by input type (the view/sequence the method consumes). Add papers in reverse chronological order within each section.

### Single-Image Reconstruction

- **EgoHandICL: Egocentric 3D Hand Reconstruction with In-Context Learning**  
  Binzhu Xie, Shi Qiu, Sicheng Zhang, Yinqiao Wang, Hao Xu, Muzammal Naseer, Chi-Wing Fu, and Pheng-Ann Heng. ICLR, 2026.  
  [[paper](https://arxiv.org/abs/2601.19850)] [[openreview](https://openreview.net/forum?id=nwjy9BeorI)] [[code](https://github.com/Nicous20/EgoHandICL)]  
  Tags: `egocentric hand reconstruction`, `in-context learning`, `VLM retrieval`, `3D hand mesh`, `EgoExo4D`, `ARCTIC`  
  <details><summary>Abstract</summary>EgoHandICL introduces in-context learning for egocentric 3D hand reconstruction. It retrieves complementary exemplars with vision-language models and uses an ICL-oriented multimodal tokenizer and MAE-style architecture to improve robustness in occluded hand-object interaction settings.</details>

- **Follow My Hold: Hand-Object Interaction Reconstruction through Geometric Guidance**  
  Ayce Idil Aytekin, Helge Rhodin, Rishabh Dabral, and Christian Theobalt. 3DV, 2026.  
  [[paper](https://arxiv.org/abs/2508.18213)] [[project](https://aidilayce.github.io/FollowMyHold-page/)] [[code](https://github.com/aidilayce/FollowMyHold)]  
  Tags: `hand-object interaction`, `single-image reconstruction`, `diffusion prior`, `geometric guidance`, `metric alignment`, `contact constraints`  
  <details><summary>Abstract</summary>Follow My Hold reconstructs hand-held objects from monocular RGB input by guiding an image-to-3D diffusion model with geometric cues. It optimizes hand and object transforms with normal, depth, silhouette, keypoint, SDF, contact, and non-intersection constraints to improve metric hand-object alignment.</details>

- **TIGeR: Text-Instructed Generation and Refinement for Template-Free Hand-Object Interaction**  
  Yiyao Huang, Zhedong Zheng, Yu Ziwei, Yaxiong Wang, Tze Ho Elden Tse, and Angela Yao. arXiv, 2025.  
  [[paper](https://arxiv.org/abs/2506.00953)] [[code](https://github.com/huangyiyNUS/TIGeR)]  
  Tags: `template-free reconstruction`, `text-guided priors`, `3D object generation`, `pose refinement`, `hand-object interaction`, `occlusion robustness`  
  <details><summary>Abstract</summary>TIGeR replaces hand-crafted object templates with text-instructed generated shape priors, then refines the generated prototype with visual observations. The method targets template-free hand-object interaction estimation and aligns synthesized object priors through 2D-3D collaborative attention.</details>

- **EasyHOI: Unleashing the Power of Large Models for Reconstructing Hand-Object Interactions in the Wild**  
  Yumeng Liu, Xiaoxiao Long, Zemin Yang, Yuan Liu, Marc Habermann, Christian Theobalt, Yuexin Ma, and Wenping Wang. CVPR, 2025.  
  [[paper](https://arxiv.org/abs/2411.14280)] [[project](https://lym29.github.io/EasyHOI-page/)] [[code](https://github.com/lym29/EasyHOI)]  
  Tags: `hand-object interaction`, `single-image reconstruction`, `foundation models`, `segmentation`, `inpainting`, `prior-guided optimization`  
  <details><summary>Abstract</summary>Our work aims to reconstruct hand-object interactions from a single-view image, which is a fundamental but ill-posed task. Unlike methods that reconstruct from videos, multi-view images, or predefined 3D templates, single-view reconstruction faces significant challenges due to inherent ambiguities and occlusions. These challenges are further amplified by the diverse nature of hand poses and the vast variety of object shapes and sizes. Our key insight is that current foundational models for segmentation, inpainting, and 3D reconstruction robustly generalize to in-the-wild images, which could provide strong visual and geometric priors for reconstructing hand-object interactions. Specifically, given a single image, we first design a novel pipeline to estimate the underlying hand pose and object shape using off-the-shelf large models. Furthermore, with the initial reconstruction, we employ a prior-guided optimization scheme, which optimizes hand pose to comply with 3D physical constraints and the 2D input image content. We perform experiments across several datasets and show that our method consistently outperforms baselines and faithfully reconstructs a diverse set of hand-object interactions.</details>

- **CaRe-Ego: Contact-aware Relationship Modeling for Egocentric Interactive Hand-object Segmentation**  
  Yuejiao Su, Yi Wang, and Lap-Pui Chau. arXiv, 2024.  
  [[paper](https://arxiv.org/abs/2407.05576)] [[code](https://github.com/yuggiehk/CaRe-Ego)]  
  Tags: `egocentric video`, `hand-object segmentation`, `contact-aware modeling`, `interactive segmentation`, `assistive systems`  
  <details><summary>Abstract</summary>CaRe-Ego addresses egocentric interactive hand-object segmentation (EgoIHOS), which segments hands and the objects they interact with in first-person images. It models hand-object interactive relationships with a Hand-guided Object Feature Enhancer that leverages hand features to extract contact-relevant object representations, and a Contact-centric Object Decoupling Strategy that explicitly models the relationships among object categories. Experiments on in-domain and out-of-domain test sets show that CaRe-Ego significantly outperforms prior methods with robust generalization.</details>

### Monocular Video Reconstruction

- **CHOIR: Contact-aware 4D Hand-Object Interaction Reconstruction**  
  Hao Xu, Yilin Liu, Yinqiao Wang, Chi-Wing Fu, and Niloy J. Mitra. arXiv, 2026.  
  [[paper](https://arxiv.org/abs/2605.20992)]  
  Tags: `4D reconstruction`, `hand-object interaction`, `monocular video`, `contact-aware optimization`, `6D object pose`, `open-world priors`  
  <details><summary>Abstract</summary>We ask whether everyday open-world monocular videos can be turned into reusable 4D interaction primitives: articulated hand motion, object shape with 6D pose over time, and the when/where of contact. Such a capability would enable scalable mining of real interactions and, beyond reconstruction, support scene-aware synthesis and planning. However, reconstructing hand-object interaction (HOI) from challenging monocular videos remains difficult: methods often assume known objects or curated scenes, and separately estimated hands and objects easily become misaligned under clutter, occlusion, and unseen object geometries. Targeting this setting, we present CHOIR, a Contact-aware HOI Reconstruction framework for a monocular camera, using contact as an explicit coupling signal between hands and objects. CHOIR first initializes a coarse, contact-agnostic 4D HOI sequence from open-world visual priors. It then introduces a generative HOI spatial rectification module to predict ray-depth corrections and rectify hand-object relative placement, then derive initial per-frame contact correspondences on the rectified geometry. Last, a contact-aware joint optimization with dynamically updated contact constraints enforces geometric, temporal, and contact consistency. Experiments on controlled and challenging videos show that CHOIR improves object reconstruction, physical plausibility, and temporal consistency over state-of-the-art methods.</details>

- **Bringing a Personal Point of View: Evaluating Dynamic 3D Gaussian Splatting for Egocentric Scene Reconstruction**  
  Jan Warchocki, Xi Wang, Jonas Kulhanek, and Jan van Gemert. EgoVis Workshop at CVPR, 2026.  
  [[paper](https://arxiv.org/abs/2604.23803)]  
  Tags: `3D Gaussian Splatting`, `dynamic reconstruction`, `egocentric video`, `EgoExo4D`  
  <details><summary>Abstract</summary>Egocentric video provides a unique view into human perception and interaction, with growing relevance for augmented reality, robotics, and assistive technologies. However, rapid camera motion and complex scene dynamics pose major challenges for 3D reconstruction from this perspective. While 3D Gaussian Splatting (3DGS) has become a state-of-the-art method for efficient, high-quality novel view synthesis, variants that focus on reconstructing dynamic scenes from monocular video are rarely evaluated on egocentric video. It remains unclear whether existing models generalize to this setting or if egocentric-specific solutions are needed. In this work, we evaluate dynamic monocular 3DGS models on egocentric and exocentric video using paired ego-exo recordings from the EgoExo4D dataset. We find that reconstruction quality is consistently lower in egocentric views. Analysis reveals that the difference in reconstruction quality, measured in peak signal-to-noise ratio, stems from the reconstruction of static, not dynamic, content. Our findings underscore current limitations and motivate the development of egocentric-specific approaches, while also highlighting the value of separately evaluating static and dynamic regions of a video.</details>

- **Grasp in Gaussians: Fast Monocular Reconstruction of Dynamic Hand-Object Interactions**  
  Ayce Idil Aytekin, Xu Chen, Zhengyang Shen, Thabo Beeler, Helge Rhodin, Rishabh Dabral, and Christian Theobalt. arXiv, 2026.  
  [[paper](https://arxiv.org/abs/2604.12929)] [[project](https://aidilayce.github.io/GraG-page/)] [[code](https://github.com/aidilayce/GraG)]  
  Tags: `Gaussian representation`, `monocular video`, `dynamic reconstruction`, `hand-object interaction`, `SAM3D`  
  <details><summary>Abstract</summary>We present Grasp in Gaussians (GraG), a fast and robust method for reconstructing dynamic 3D hand-object interactions from a single monocular video. Unlike recent approaches that optimize heavy neural representations, our method focuses on tracking the hand and the object efficiently, once initialized from pretrained large models. Our key insight is that accurate and temporally stable hand-object motion can be recovered using a compact Sum-of-Gaussians (SoG) representation, revived from classical tracking literature and integrated with generative Gaussian-based initializations. We initialize object pose and geometry using a video-adapted SAM3D pipeline, then convert the resulting dense Gaussian representation into a lightweight SoG via subsampling. This compact representation enables efficient and fast tracking while preserving geometric fidelity. For the hand, we adopt a complementary strategy: starting from off-the-shelf monocular hand pose initialization, we refine hand motion using simple yet effective 2D joint and depth alignment losses, avoiding per-frame refinement of a detailed 3D hand appearance model while maintaining stable articulation. Extensive experiments on public benchmarks demonstrate that GraG reconstructs temporally coherent hand-object interactions on long sequences 6.4× faster than prior work while improving object reconstruction by 13.4% and reducing hand's per-joint position error by over 65%.</details>

- **MASS: Mesh-inellipse Aligned Deformable Surfel Splatting for Hand Reconstruction and Rendering from Egocentric Monocular Video**  
  Haoyu Zhu, Yi Zhang, Lei Yao, Lap-pui Chau, and Yi Wang. arXiv, 2026.  
  [[paper](https://arxiv.org/abs/2604.08943)]  
  Tags: `hand reconstruction`, `egocentric video`, `monocular video`, `deformable surfel splatting`, `2D Gaussian Splatting`  
  <details><summary>Abstract</summary>MASS reconstructs high-fidelity dynamic hands from egocentric monocular video with a deformable 2D Gaussian surfel representation. It initializes surfels from hand meshes using mesh-aligned Steiner inellipses and refines geometry and texture with Gaussian surfel deformation.</details>

- **ArtHOI: Taming Foundation Models for Monocular 4D Reconstruction of Hand-Articulated-Object Interactions**  
  Zikai Wang, Zhilu Zhang, Yiqing Wang, Hui Li, and Wangmeng Zuo. CVPR Highlight, 2026.  
  [[paper](https://arxiv.org/abs/2603.25791)] [[project](https://arthoi-reconstruction.github.io/)] [[code](https://github.com/hitcs-zikaiwang/ArtHOI-4D-Reconstruction)]  
  Tags: `4D reconstruction`, `hand-object interaction`, `articulated objects`, `monocular video`, `foundation models`, `MLLM`  
  <details><summary>Abstract</summary>ArtHOI reconstructs hand-articulated-object interactions from a single RGB video by combining priors from multiple foundation models. It refines object scale and pose with adaptive sampling and uses MLLM-guided contact reasoning to improve hand-object alignment.</details>

- **GHOST: Fast Category-agnostic Hand-Object Interaction Reconstruction from RGB Videos using Gaussian Splatting**  
  Ahmed Tawfik Aboukhadra, Marcel Rogge, Nadia Robertini, Abdalla Arafa, Jameel Malik, Ahmed Elhayek, and Didier Stricker. CVPR Findings, 2026.  
  [[paper](https://arxiv.org/abs/2603.18912)] [[project](https://ataboukhadra.github.io/GHOST/)] [[code](https://github.com/ATAboukhadra/GHOST)]  
  Tags: `Gaussian Splatting`, `2D Gaussian Splatting`, `RGB video`, `hand-object interaction`, `category-agnostic reconstruction`, `ARCTIC`, `HO3D`  
  <details><summary>Abstract</summary>Understanding realistic hand-object interactions from monocular RGB videos is essential for AR/VR, robotics, and embodied AI. Existing methods rely on category-specific templates or heavy computation, yet still produce physically inconsistent hand-object alignment in 3D. We introduce GHOST (Gaussian Hand-Object Splatting), a fast, category-agnostic framework for reconstructing dynamic hand-object interactions using 2D Gaussian Splatting. GHOST represents both hands and objects as dense, view-consistent Gaussian discs and introduces three key innovations: (1) a geometric-prior retrieval and consistency loss that completes occluded object regions, (2) a grasp-aware alignment that refines hand translations and object scale to ensure realistic contact, and (3) a hand-aware background loss that prevents penalizing hand-occluded object regions. GHOST achieves complete, physically consistent, and animatable reconstructions from a single RGB video while running an order of magnitude faster than prior category-agnostic methods. Extensive experiments on ARCTIC, HO3D, and in-the-wild datasets demonstrate state-of-the-art accuracy in 3D reconstruction and 2D rendering quality, establishing GHOST as an efficient and robust solution for realistic hand-object interaction modeling.</details>

- **WHOLE: World-Grounded Hand-Object Lifted from Egocentric Videos**  
  Yufei Ye, Jiaman Li, Ryan Rong, and C. Karen Liu. arXiv, 2026.  
  [[paper](https://arxiv.org/abs/2602.22209)] [[project](https://judyye.github.io/whole-www)]  
  Tags: `egocentric video`, `world-space reconstruction`, `hand-object motion`, `generative motion prior`, `object pose estimation`  
  <details><summary>Abstract</summary>WHOLE reconstructs hands and object motion in a persistent world coordinate frame from egocentric video, given object templates. It learns a joint hand-object motion prior and guides generation at test time with video observations to handle occlusion and out-of-view interactions.</details>

- **ForeHOI: Feed-forward 3D Object Reconstruction from Daily Hand-Object Interaction Videos**  
  Yuantao Chen, Jiahao Chang, Chongjie Ye, Chaoran Zhang, Zhaojie Fang, Chenghong Li, and Xiaoguang Han. CVPR, 2026.  
  [[paper](https://arxiv.org/abs/2602.06226)] [[code](https://github.com/Tao-11-chen/ForeHOI)]  
  Tags: `feed-forward reconstruction`, `3D object reconstruction`, `hand-object interaction`, `mask inpainting`, `shape completion`, `synthetic data`  
  <details><summary>Abstract</summary>ForeHOI is a feed-forward model for reconstructing 3D object geometry from monocular hand-object interaction videos. It jointly predicts 2D mask inpainting and 3D shape completion to recover occluded object regions without per-sequence optimization.</details>

- **Reconstructing Objects along Hand Interaction Timelines in Egocentric Video**  
  Zhifan Zhu, Siddhant Bansal, Shashank Tripathi, and Dima Damen. arXiv, 2025.  
  [[paper](https://arxiv.org/abs/2512.07394v2)] [[project](https://zhifanzhu.github.io/objects-along-hit)] [[code](https://github.com/zhifanzhu/objects-along-hit)]  
  Tags: `hand-object interaction`, `egocentric video`, `3D object reconstruction`, `ROHIT`, `HOT3D`, `EPIC-HIT`  
  <details><summary>Abstract</summary>We introduce the task of Reconstructing Objects along Hand Interaction Timelines (ROHIT). We define the Hand Interaction Timeline (HIT) from a rigid object's perspective: an object is first static relative to the scene, then is held in hand following contact where its pose changes, followed by a firm grip during use, then released back to being static. We model pose constraints over the HIT and propose a Constrained Optimisation and Propagation (COP) framework to propagate object pose along the timeline for improved reconstruction. Our work focuses on timelines involving stable grasps, enabling annotation and evaluation without 3D ground truth. We evaluate on two egocentric datasets: HOT3D with 1.2K clips of stable grasps, and EPIC-Kitchens with 2.4K annotated clips spanning 390 object instances across 9 categories. Quantitatively, COP improves stable grasp reconstruction by 6.2–11.3% and full HIT reconstruction by up to 24.5%. We also introduce the EPIC-HIT benchmark to foster future research on HIT-based object reconstruction.</details>

- **MagicHOI: Leveraging 3D Priors for Accurate Hand-object Reconstruction from Short Monocular Video Clips**  
  Shibo Wang, Haonan He, Maria Parelli, Christoph Gebhardt, Zicong Fan, and Jie Song. ICCV, 2025.  
  [[paper](https://arxiv.org/abs/2508.05506)] [[project](https://byran-wang.github.io/MagicHOI/)] [[code](https://github.com/byran-wang/MagicHOI)]  
  Tags: `hand-object reconstruction`, `monocular video`, `novel view synthesis`, `occlusion completion`, `3D priors`, `contact constraints`  
  <details><summary>Abstract</summary>MagicHOI reconstructs hands and objects from short monocular interaction videos under limited viewpoint variation. It uses novel-view-synthesis diffusion priors to regularize unseen object regions and visible contact constraints to improve hand-object alignment.</details>

- **BIGS: Bimanual Category-agnostic Interaction Reconstruction from Monocular Videos via 3D Gaussian Splatting**  
  Jeongwan On, Kyeonghwan Gwak, Gunyoung Kang, Junuk Cha, Soohyun Hwang, Hyein Hwang, and Seungryul Baek. CVPR, 2025.  
  [[paper](https://arxiv.org/abs/2504.09097)] [[code](https://github.com/On-JungWoan/BIGS)]  
  Tags: `bimanual interaction`, `category-agnostic reconstruction`, `3D Gaussian Splatting`, `monocular video`, `diffusion prior`, `occlusion completion`  
  <details><summary>Abstract</summary>BIGS reconstructs two hands and an unknown interacting object from monocular RGB video with 3D Gaussian Splatting. It uses diffusion-based SDS priors to complete heavily occluded object parts and shared hand Gaussians to accumulate information across both hands.</details>

- **HOLD: Category-agnostic 3D Reconstruction of Interacting Hands and Objects from Video**  
  Zicong Fan, Maria Parelli, Maria Eleni Kadoglou, Xu Chen, Muhammed Kocabas, Michael J. Black, and Otmar Hilliges. CVPR Highlight, 2024.  
  [[paper](https://arxiv.org/abs/2311.18448)] [[project](https://zc-alexfan.github.io/hold)] [[code](https://github.com/zc-alexfan/hold)]  
  Tags: `hand-object interaction`, `monocular video`, `category-agnostic reconstruction`, `articulated implicit model`, `template-free`, `in-the-wild`  
  <details><summary>Abstract</summary>Since humans interact with diverse objects every day, the holistic 3D capture of these interactions is important to understand and model human behaviour. However, most existing methods for hand-object reconstruction from RGB either assume pre-scanned object templates or heavily rely on limited 3D hand-object data, restricting their ability to scale and generalize to more unconstrained interaction settings. To this end, we introduce HOLD -- the first category-agnostic method that reconstructs an articulated hand and object jointly from a monocular interaction video. We develop a compositional articulated implicit model that can reconstruct disentangled 3D hand and object from 2D images. We also further incorporate hand-object constraints to improve hand-object poses and consequently the reconstruction quality. Our method does not rely on 3D hand-object annotations while outperforming fully-supervised baselines in both in-the-lab and challenging in-the-wild settings. Moreover, we qualitatively show its robustness in reconstructing from in-the-wild videos.</details>

### Others

Adjacent works kept for reference. These are not hand-object interaction reconstruction methods; each is grouped under its category below.

#### Scene Reconstruction

- **DP-DeGauss: Dynamic Probabilistic Gaussian Decomposition for Egocentric 4D Scene Reconstruction**  
  Tingxi Chen, Zhengxue Cheng, Houqiang Zhong, Su Wang, Rong Xie, and Li Song. arXiv, 2026.  
  [[paper](https://arxiv.org/abs/2604.07986)]  
  Tags: `4D scene reconstruction`, `egocentric video`, `3D Gaussian Splatting`, `dynamic-static decomposition`, `hand-object interaction`  
  <details><summary>Abstract</summary>DP-DeGauss reconstructs dynamic egocentric scenes by decomposing Gaussian primitives into background, hand, and object components with learned category probabilities. It targets challenging first-person videos with occlusion, ego-motion, and hand-object interactions, enabling explicit disentanglement for rendering and editing.</details>

- **DeGauss: Dynamic-Static Decomposition with Gaussian Splatting for Distractor-free 3D Reconstruction**  
  Rui Wang, Quentin Lohmeyer, Mirko Meboldt, and Siyu Tang. ICCV, 2025.  
  [[paper](https://arxiv.org/abs/2503.13176)] [[project](https://batfacewayne.github.io/DeGauss.io/)] [[code](https://github.com/BatFaceWayne/DeGauss)]  
  Tags: `3D Gaussian Splatting`, `dynamic-static decomposition`, `distractor-free reconstruction`, `egocentric video`, `ADT`, `AEA`, `Hot3D`, `EPIC-Fields`  
  <details><summary>Abstract</summary>Reconstructing clean, distractor-free 3D scenes from real-world captures remains a significant challenge, particularly in highly dynamic and cluttered settings such as egocentric videos. To tackle this problem, we introduce DeGauss, a simple and robust self-supervised framework for dynamic scene reconstruction based on a decoupled dynamic-static Gaussian Splatting design. DeGauss models dynamic elements with foreground Gaussians and static content with background Gaussians, using a probabilistic mask to coordinate their composition and enable independent yet complementary optimization. DeGauss generalizes robustly across a wide range of real-world scenarios, from casual image collections to long, dynamic egocentric videos, without relying on complex heuristics or extensive supervision. Experiments on benchmarks including NeRF-on-the-go, ADT, AEA, Hot3D, and EPIC-Fields demonstrate that DeGauss consistently outperforms existing methods, establishing a strong baseline for generalizable, distractor-free 3D reconstruction in highly dynamic, interaction-rich environments.</details>

- **Self-Supervised Monocular 4D Scene Reconstruction for Egocentric Videos**  
  Chengbo Yuan, Geng Chen, Li Yi, and Yang Gao. arXiv, 2024.  
  [[paper](https://arxiv.org/abs/2411.09145)] [[project](https://egomono4d.github.io/)] [[code](https://github.com/michaelyuancb/egomono4d)]  
  Tags: `monocular video`, `4D reconstruction`, `self-supervised learning`, `dense point clouds`, `egocentric video`  
  <details><summary>Abstract</summary>Egocentric videos provide valuable insights into human interactions with the physical world, which has sparked growing interest in the computer vision and robotics communities. A critical challenge in fully understanding the geometry and dynamics of egocentric videos is dense scene reconstruction. However, the lack of high-quality labeled datasets in this field has hindered the effectiveness of current supervised learning methods. In this work, we aim to address this issue by exploring a self-supervised dynamic scene reconstruction approach. We introduce EgoMono4D, a novel model that unifies the estimation of multiple variables necessary for Egocentric Monocular 4D reconstruction, including camera intrinsic, camera poses, and video depth, all within a fast feed-forward framework. Starting from pretrained single-frame depth and intrinsic estimation model, we extend it with camera poses estimation and align multi-frame results on large-scale unlabeled egocentric videos. We evaluate EgoMono4D in both in-domain and zero-shot generalization settings, achieving superior performance in dense pointclouds sequence reconstruction compared to all baselines. EgoMono4D represents the first attempt to apply self-supervised learning for pointclouds sequence reconstruction to the label-scarce egocentric field, enabling fast, dense, and generalizable reconstruction.</details>

#### Robotic Manipulation

- **GraspFoM: Towards Reconstruction-Driven Robotic Grasping with 3D Foundation Priors**  
  Dongli Wu, Xiaobao Wei, Hao Wang, Qiaochu Dong, Ying Li, Qingpo Wuwu, Ming Lu, and Wufan Zhao. arXiv, 2026.  
  [[paper](https://arxiv.org/abs/2606.08440)] [[project](https://annike-val.github.io/GraspFoM/)]  
  Tags: `reconstruction-driven grasping`, `3D foundation priors`, `SAM3D`, `3D Gaussian Splatting`, `mesh reconstruction`, `GraspNet-1B`  
  <details><summary>Abstract</summary>Robotic grasping under partial observations demands both local contact cues and object-level 3D structure, yet existing geometry-aware approaches treat geometry as an intermediate step rather than a reusable prior. GraspFoM is a unified framework that leverages 3D foundation priors (SAM3D) to produce a shared 3D object latent for both reconstruction and grasp pose prediction. It introduces an anchor-initialized truncated pose-reasoning diffuser that predicts continuous, multimodal grasp poses without relying on discrete grasp candidates. A reconstruction-aware scorer and residual latent updater enable reconstruction and grasping to mutually benefit: reconstruction provides geometric cues while grasp supervision refines the shared object latent toward grasp-relevant affordances. GraspFoM jointly predicts grasps and reconstructs high-fidelity 3D assets in both mesh and 3DGS forms, achieving state-of-the-art results on both tasks with minimal additional trainable parameters.</details>

- **DexImit: Learning Bimanual Dexterous Manipulation from Monocular Human Videos**  
  Juncheng Mu, Sizhe Yang, Yiming Bao, Hojin Bae, Tianming Wei, Linning Xu, Boyi Li, Huazhe Xu, and Jiangmiao Pang. arXiv, 2026.  
  [[paper](https://arxiv.org/abs/2602.10105)] [[project](https://mujc2021.github.io/deximit/)] [[code](https://github.com/mujc2021/DexImit-Open)]  
  Tags: `bimanual dexterous manipulation`, `monocular human video`, `hand-object reconstruction`, `robot data generation`, `near-metric scale`, `zero-shot deployment`  
  <details><summary>Abstract</summary>Data scarcity fundamentally limits the generalization of bimanual dexterous manipulation, as real-world data collection for dexterous hands is expensive and labor-intensive. Human manipulation videos, as a direct carrier of manipulation knowledge, offer significant potential for scaling up robot learning. However, the substantial embodiment gap between human hands and robotic dexterous hands makes direct pretraining from human videos extremely challenging. To bridge this gap and unleash the potential of large-scale human manipulation video data, we propose DexImit, an automated framework that converts monocular human manipulation videos into physically plausible robot data, without any additional information. DexImit employs a four-stage generation pipeline: (1) reconstructing hand-object interactions from arbitrary viewpoints with near-metric scale; (2) performing subtask decomposition and bimanual scheduling; (3) synthesizing robot trajectories consistent with the demonstrated interactions; (4) comprehensive data augmentation for zero-shot real-world deployment. Building on these designs, DexImit can generate large-scale robot data based on human videos, either from the Internet or video generation models. DexImit is capable of handling diverse manipulation tasks, including tool use (e.g., cutting an apple), long-horizon tasks (e.g., making a beverage), and fine-grained manipulations (e.g., stacking cups).</details>

- **Stereo Hand-Object Reconstruction for Human-to-Robot Handover**  
  Yik Lung Pang, Alessio Xompero, Changjae Oh, and Andrea Cavallaro. IEEE Robotics and Automation Letters, 2025.  
  [[paper](https://arxiv.org/abs/2412.07487)] [[project](https://qm-ipalab.github.io/StereoHO/)] [[code](https://github.com/QM-IPAlab/StereoHO)]  
  Tags: `human-to-robot handover`, `stereo RGB`, `hand-object reconstruction`, `transparent objects`, `robot grasping`, `wide-baseline cameras`  
  <details><summary>Abstract</summary>StereoHO reconstructs hand-object shape from wide-baseline stereo RGB rather than depth, improving robustness for transparent and unseen household objects. It combines single-view shape-code distributions probabilistically into a coherent stereo reconstruction and uses the output in a robot handover pipeline.</details>

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
  Tags: `hand-object interaction`, `monocular video`
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
