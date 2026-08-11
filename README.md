<div align="center">

# Beyond Pixels: From Video Priors to 4D Worlds

Zihao Liu, [Xiaolong Shen](https://scholar.google.com/citations?user=vAMMc8EAAAAJ), [Zhenglin Zhou](https://scholar.google.com/citations?user=6v7tOfEAAAAJ), [Ruijie Quan](https://scholar.google.com/citations?user=WKLRPsAAAAAJ), [Yi Yang](https://scholar.google.com/citations?user=RMSuNFwAAAAJ)<sup>*</sup>

**Zhejiang University**

<sup>*</sup>Corresponding author

[Project Page](https://hayd-zju.github.io/) · **arXiv (Coming Soon)** · **PDF (Coming Soon)** · **Hugging Face (Coming Soon)** · **ModelScope (Coming Soon)**

</div>

<div align="center">
  <img src="https://hayd-zju.github.io/media/teaser-figure-original.webp?v=pdf-replacement-20260810" alt="Beyond Pixels teaser" width="100%">
</div>

> [!IMPORTANT]
> **Code and models have not been released yet.** This private repository currently serves as the official project placeholder. Release materials will be added after the paper revision is complete.

## News

- **[2026/08/11]** The official repository is now available. Code and model release are under preparation.

## TL;DR

**One latent interface for generated 4D.** Beyond Pixels lifts the terminal denoised latent of a video diffusion transformer into camera parameters and dynamic world-space point maps, enabling compatible video generation tasks to transfer to 4D without task-specific changes to the 4D predictor.

## Abstract

4D generation seeks to synthesize dynamic 3D scenes from conditions such as text and images. Existing systems either reconstruct decoded RGB videos with a separate 4D model—introducing distribution mismatch and cascading errors—or specialize a video generator for geometry prediction, limiting transfer across backbones and conditioning schemes. We instead treat the terminal denoised latent of video DiTs sharing a VAE as a reusable interface to explicit 4D prediction. Latent-to-4D bypasses RGB decoding by aligning this latent with a pretrained 4D decoder and refining it through alternating frame-wise and global spatiotemporal attention. Trained on roughly 1K continuous 81-frame clips from six existing reconstruction datasets, one checkpoint transfers unchanged across three compatible conditional DiTs. On Text4D-200 and I4D-200, it improves DINO-F1 over matched Wan+4RC cascades by 2.88–3.45 and 5.81 points, respectively; multi-view human evaluation also favors its geometry, completeness, and temporal stability.

## Highlights

- **Generality.** A single Latent-to-4D (L4AR) checkpoint transfers across compatible video DiTs that share the same VAE latent space.
- **Efficiency.** Training uses roughly 1K clips, followed by about one hour of final refinement on four GPUs.
- **Performance.** L4AR improves DINO-F1 by 2.88–5.81 points and receives 66.8–72.1% human preference for 4D geometry.

## Method Overview

<div align="center">
  <img src="https://hayd-zju.github.io/media/method-l4ar-original.webp" alt="Latent-to-4D method overview" width="100%">
</div>

Rather than decoding a generated video to RGB and reconstructing it with a separate model, L4AR directly maps the terminal video latent to explicit 4D structure. A lightweight alignment module bridges the latent representation to a pretrained 4D decoder, while alternating frame-wise and global spatiotemporal attention preserves per-frame detail and temporal consistency.

## Applications

The same latent-to-4D pathway supports a broad range of compatible video-generation settings, including:

- Text-to-4D and image-to-4D generation
- Audio-, video-, pose-, and motion-conditioned 4D generation
- Controllable 4D character animation
- Action-conditioned 4D world simulation

Interactive results are available on the [project page](https://hayd-zju.github.io/#interactive).

## Release Status

| Resource | Status |
| --- | --- |
| Project page | Available |
| arXiv and PDF | Paper under revision |
| Source code | Planned |
| Model checkpoints | Planned |
| Hugging Face and ModelScope | Planned |

We will update this repository when the corresponding materials are ready. No release date is announced at this stage.

## Citation

Citation information will be added after the arXiv release.
