# TACE Foundational Models

This repository provides foundational atomistic machine learning models based on **Tensor Atomic Cluster Expansion (TACE)**. These models are primarily developed for **potential energy surfaces** in **materials and reaction systems**, including multi-phase catalysis and organic reactions. Future work may extend the framework to additional types of foundational models.

The source code for TACE can be found here: [TACE GitHub Repository](https://github.com/xvzemin/tace).

---

## Material Models

### TAVE-v1-OMat24-M

[Download](https://huggingface.co/xvzemin/tace-foundations/resolve/main/TACE-v1-OMat24-M.pt)

- **Model size:** 18.8M parameters, 89M elements 
- **Training data:** OMat24 dataset (PBE+U)  
- **Target property:** `[energy, forces, stress]`  
- **Embedding property:** `[]`  
- **Highlights:** Excellent derivative behavior  
- **Thermal conductivity indicator:** κ_SRME = 0.1575  


### TAVE-v1-OAM-M

[Download](https://huggingface.co/xvzemin/tace-foundations/resolve/main/TACE-v1-OAM-M.pt)

- **Model size:** 18.8M parameters, 89M elements  
- **Training data:** Fine-tuned from TAVE-v1-OMat24-M using sAlex + MPtrj (PBE+U)  
- **Target properties:** `[energy, forces, stress]`  
- **Embedding properties:** `[]`  
- **Highlights:** Enhanced energy prediction accuracy  
- **Thermal conductivity indicator:** κ_SRME = 0.1729  

---

## Catalysis Models

### TACE-v1-LES-REICO-5-PdAgCHO.pt

[Download](https://huggingface.co/xvzemin/tace-foundations/resolve/main/TACE-v1-LES-REICO-5-PdAgCHO.pt)

- **Model size:** 4.7M parameters
- **Support elements:** [Pd, Ag, C, H, O]
- **Training data:** Training using RECIO-PdAgCHO dataset (PBE)  
- **Target properties:** `[energy, forces, stress]`  
- **Embedding properties:** `[]`  
- **Plug-in:** Please install ``LES`` use git commit ``976e196`` in https://github.com/ChengUCB/les
- **Highlights:** ``Describing almost arbitrary reactions without finetuning`` 


### TACE-AOR
- Coming soon
- **Highlights:** Spin-aware model with mixed-precision training, crucial for systems with magnetic properties

---

## Finetuning Strategy

We currently support **LoRA** and **parameter-freezing** finetuning methods.  
For more details, please refer to the TACE documentation: [TACE Docs](https://tace.readthedocs.io/en/latest/index.html)

---

## Citing TACE

If you use TACE code or foundational models in your work, please cite the following references.  
We sincerely acknowledge the contributions of all researchers who made the training datasets publicly available. Specific dataset citations for each model will be provided in future updates.

```bibtex
@misc{TACE,
      title={TACE: A unified Irreducible Cartesian Tensor Framework for Atomistic Machine Learning},
      author={Zemin Xu and Wenbo Xie and Daiqian Xie and P. Hu},
      year={2025},
      eprint={2509.14961},
      archivePrefix={arXiv},
      primaryClass={stat.ML},
      url={https://arxiv.org/abs/2509.14961},
}

@misc{Cartesian-nj,
      title={Cartesian-nj: Extending e3nn to Irreducible Cartesian Tensor Product and Contraction},
      author={Zemin Xu and Chenyu Wu and Wenbo Xie and Daiqian Xie and P. Hu},
      year={2025},
      eprint={2512.16882},
      archivePrefix={arXiv},
      primaryClass={physics.chem-ph},
      url={https://arxiv.org/abs/2512.16882},
}

@misc{zemin_xu_2026,
	author       = { Zemin Xu and Wenbo Xie and P. Hu },
	title        = { tace-foundations (Revision 086d67d) },
	year         = 2026,
	url          = { https://huggingface.co/xvzemin/tace-foundations },
	doi          = { 10.57967/hf/7458 },
	publisher    = { Hugging Face }
}
```

## License

Code: MIT License  

Models：CC BY 4.0

