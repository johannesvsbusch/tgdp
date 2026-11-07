# Temperature Guidance for Robust Reward Conditioning in Diffusion Planning

Code release for the NeurIPS 2026 paper *Temperature Guidance For Robust Reward Conditioning In Diffusion Planning*.

**Authors:** Johannes V. S. Busch, Roberto Calandra · LASR Lab, Technische Universität Dresden
**Paper:** https://openreview.net/forum?id=PHxRfWn3K5

## Abstract

Diffusion planners enable long-horizon planning through a generative process over full trajectories, mitigating compounding errors of autoregressive methods while handling multimodal futures. Reward conditioning via classifier-free guidance (CFG) yields high-performing plans but is brittle with respect to per-task hyperparameter choices, limiting its scalability. Our analysis reveals that guidance performance hinges on careful adaptation to the data manifold and reward distribution, contributing to CFG's hyperparameter fragility. We propose temperature-guided diffusion planning (TGDP), which adapts CFG to self-calibrate to these characteristics through temperature-conditioned sample reweighting during training and adaptive guidance at inference. TGDP mitigates the hyperparameter fragility of CFG and achieves competitive performance across standard benchmarks without per-task tuning, thus enabling more robust and practical diffusion-based planning.

## Status

This repository currently contains only this README and the license. The following will be added:

- the temperature-weighted training objective and the adaptive guide scale,
- the model definition and the training and evaluation entry points,
- configuration files for reported benchmarks,
- pinned dependency versions.

## Data

Experiments use the [D4RL](https://github.com/Farama-Foundation/D4RL) locomotion, maze2d, antmaze and kitchen datasets. No dataset files are redistributed here.

## Citation

```bibtex
@inproceedings{busch2026temperature,
  title     = {{Temperature Guidance For Robust Reward Conditioning In Diffusion Planning}},
  author    = {Busch, Johannes V. S. and Calandra, Roberto},
  booktitle = {Advances in Neural Information Processing Systems},
  volume    = {39},
  year      = {2026}
}
```

## License

MIT, see [LICENSE](LICENSE).
