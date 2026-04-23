<!-- # TACE Foundational Models -->

This repository provides foundational atomistic machine learning models based on **Tensor Atomic Cluster Expansion (TACE)**. These models are primarily developed for **potential energy surfaces** in **materials and reaction systems**, including multi-phase catalysis and organic reactions. Future work may extend the framework to additional types of foundational models.

The source code for TACE can be found here: [TACE GitHub Repository](https://github.com/xvzemin/tace).

All model can be found here: [TACE HuggingFace Repository](https://huggingface.co/xvzemin/tace-foundations/tree/main).

# Available models
| Name                        | Level of theory | Available sizes     | To be used for                      | Training set          |
|-----------------------------|-----------------|---------------------|-------------------------------------|-----------------------|
| TACE-OMAT24                 | PBE+U           | M, L                | materials (89 elements)             | OMat24                |
| TACE-OAM                    | PBE+U           | L                   | materials (89 elements)             | OMat24 → sAlex+MPtrj  |

---

# Legacy models
| Name                        | Level of theory | Available sizes     | To be used for                      | Training set          |
|-----------------------------|-----------------|---------------------|-------------------------------------|-----------------------|
| TACE-v1-OMAT24              | PBE+U           | M                   | materials (89 elements)             | OMat24                |
| TACE-v1-OAM                 | PBE+U           | M                   | materials (89 elements)             | OMat24 → sAlex+MPtrj  |
| TACE-v1-LES-REICO-5-PdAgCHO | PBE             | M                   | heterogeneous catalysis (5 elements)| REICO-5-PdAgCHO       |

---

## Finetuning Strategy

We currently support **LoRA** and **parameter-freezing** finetuning methods. (LoRA need tace = 0.1.0)

For more details, please refer to the TACE documentation: [TACE Docs](https://tace.readthedocs.io/en/latest/index.html)

---

## Citing TACE

If you use TACE code or foundational models in your work, please cite the following references.  
We sincerely acknowledge the contributions of all researchers who made the training datasets publicly available. 
Specific dataset citations for each model will be provided in future updates.

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

@misc{xu2025cartesiannjextendinge3nnirreducible,
      title={Cartesian-nj: Extending e3nn to Irreducible Cartesian Tensor Product and Contracion},
      author={Zemin Xu and Chenyu Wu and Wenbo Xie and Daiqian Xie and P. Hu},
      year={2025},
      eprint={2512.16882},
      archivePrefix={arXiv},
      primaryClass={physics.chem-ph},
      url={https://arxiv.org/abs/2512.16882},
}
```

## License

Code: MIT License  

Models：CC BY 4.0


