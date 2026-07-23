<!-- # TACE Foundational Models -->

# Default Ranking on Matbench as of July 8, 2026
![Default Ranking on Matbench as of July 8, 2026](fig/matbench_tece_rra.png)

# Model Selection Guide

* **Highest accuracy**
  If accuracy is your top priority, we recommend:

  * `TECE-OMat24-RRA-1.0`
  * `TECE-OAM-RRA-1.0`

* **Balanced accuracy, speed, and memory usage**
  For production simulations, we recommend:

  * `TACE-OMat24-7M`
  * `TACE-OAM-7M`

  These models provide a better balance between accuracy, inference speed, and GPU memory consumption.

* **About `TACE-OAM-L`**
  `TACE-OAM-L` remains usable, but it is based on an earlier, less effective architecture developed during the model exploration stage. In addition, it was trained using only approximately 20% of the available `OMat24`, `sAlex`, and `MPtrj` datasets. Therefore, it is not recommended as the default choice for new projects or production simulations.

# Acceleration (OpenEquivariance / cuEquivariance / AOTI)

When using or benchmarking any TACE model, make sure to enable the appropriate TACE acceleration method. Acceleration can deliver at least a **5× improvement in runtime performance and GPU memory efficiency** compared with the unaccelerated configuration.

See the [TACE Acceleration Guide](https://tace.readthedocs.io/en/latest/guide/acceleration.html) for setup instructions and supported backends.

# Available models

The source code for TACE can be found here: [TACE GitHub Repository](https://github.com/xvzemin/tace).

All model can be found here: [TACE HuggingFace Repository](https://huggingface.co/xvzemin/tace-foundations/tree/main).

| Name                        | Level of theory | Available sizes     | To be used for                      | Training set          |
|-----------------------------|-----------------|---------------------|-------------------------------------|-----------------------|
| TACE-OMat24-7M              | PBE+U           | M                   | materials (89 elements)             | OMat24                |
| TACE-OAM-7M                 | PBE+U           | M                   | materials (89 elements)             | OMat24 → sAlex+MPtrj  |
| TECE-OMat24-RRA-1.0         | PBE+U           | XL                  | materials (89 elements)             | OMat24                |
| TECE-OAM-RRA-1.0            | PBE+U           | XL                  | materials (89 elements)             | OMat24 → sAlex+MPtrj  |
| TACE-OMat24-RRA-1.0         | PBE+U           | XL                  | materials (89 elements)             | OMat24                |
| TACE-OAM-RRA-Preview        | PBE+U           | XL                  | materials (89 elements)             | OMat24 → sAlex+MPtrj  |
| TACE-OMat24-L               | PBE+U           | L                   | materials (89 elements)             | OMat24                |
| TACE-OAM-L                  | PBE+U           | L                   | materials (89 elements)             | OMat24 → sAlex+MPtrj  |

---

# Legacy models
| Name                        | Level of theory | Available sizes     | To be used for                      | Training set          |
|-----------------------------|-----------------|---------------------|-------------------------------------|-----------------------|
| TACE-v1-OMAT24              | PBE+U           | M                   | materials (89 elements)             | OMat24                |
| TACE-v1-OAM                 | PBE+U           | M                   | materials (89 elements)             | OMat24 → sAlex+MPtrj  |
| TACE-v1-LES-REICO-5-PdAgCHO | PBE             | M                   | heterogeneous catalysis (5 elements)| REICO-5-PdAgCHO       |
---

# Finetuning Strategy

We currently support **LoRA** and **parameter-freezing** finetuning methods.

For more details, please refer to the TACE documentation: [TACE Docs](https://tace.readthedocs.io/en/latest/index.html)

---

# Citing TACE

If you use TACE, please cite our papers:

```bibtex
@misc{xu2026spectralspatialtensoratomiccluster,
  title={Spectral/Spatial Tensor Atomic Cluster Expansion with Universal Embeddings in Cartesian Space},
  author={Zemin Xu and Wenbo Xie and P. Hu},
  year={2026},
  eprint={2509.14961},
  archivePrefix={arXiv},
  primaryClass={stat.ML},
    url={https://arxiv.org/abs/2509.14961},
}

@misc{xu2026edgeclusterexpansionradial,
  title={Edge Cluster Expansion with Radial Rotary Attention for Interatomic Potentials},
  author={Zemin Xu and Wenbo Xie and P. Hu},
  year={2026},
  eprint={2607.10664},
  archivePrefix={arXiv},
  primaryClass={stat.ML},
  url={https://arxiv.org/abs/2607.10664},
}
```

If you use cartnn, Cartesian-3j, cMACE, cNequIP, cAllegro, please cite our papers:

```bibtex
@inproceedings{
  xu2026a,
  title={A Cartesian-3j Framework for Machine Learning Interatomic Potentials},
  author={Zemin Xu and Chenyu Wu and Wenbo Xie and Peijun Hu},
  booktitle={Forty-third International Conference on Machine Learning},
  year={2026},
  url={https://openreview.net/forum?id=9ZWK6gneWq}
}
```

## License

Code: MIT License  

Models：CC BY 4.0


