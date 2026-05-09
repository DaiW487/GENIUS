<div align="center">
<h1>
🧠 GENIUS: Generative Fluid Intelligence Evaluation Suite
</h1>

[![Paper](https://img.shields.io/badge/Paper-Arxiv-red)](https://arxiv.org/pdf/2602.11144) [![Dataset](https://img.shields.io/badge/Dataset-HuggingFace-orange)](https://huggingface.co/datasets/HankYang428/GENIUS) 

</div>

<div align="center">

[Ruichuan An](https://github.com/arctanxarc)<sup>\*</sup>, [Sihan Yang](https://github.com/Hhankyangg)<sup>*</sup>, [Ziyu Guo](), [Wei Dai](), [Zijun Shen](), [Haodong Li]() <br> [Renrui Zhang]()<sup>†</sup>, [Xinyu Wei](), [Guopeng Li](), [Wenshan Wu](), [Wentao Zhang]()<sup>‡</sup>

PKU, CUHK, StepFun, PolyU, MSRA.

<sup>*</sup> Equal Contribution &nbsp;&nbsp;&nbsp; <sup>†</sup> Project Leader &nbsp;&nbsp;&nbsp; <sup>‡</sup> Corresponding Author

</div>

<p align="center">
  <a href="https://chawuciren11.github.io/GENIUS/"><b>📄 Blog</b></a> |
  <a href="#-quick-start"><b>🚀 Quick Start</b></a> |
  <a href="#1-download-the-test-dataset"><b>📦 Dataset</b></a> |
  <a href="#-license"><b>📜 License</b></a> |
  <a href="#-citation"><b>📝 Citation</b></a> |
  <a href="#-contact"><b>📬 Contact</b></a>
</p>

![An overview of **GENIUS** benchmark.](assets/showtask.png)
---

## 🕙 Timeline
- [x] **2026.02.11**: 🌟 Release of the evaluation code and the core test dataset.
- [ ] **TBD**: Integration of more model inference scripts.

---

## 🏆 Leaderboard

| Rank | Model | Interleaved | Overall | IP-RC | IP-VC | IP-AQ | SC-RC | SC-VC | SC-AQ | VC-RC | VC-VC | VC-AQ | PC-RC | PC-VC | PC-AQ | MS-RC | MS-VC | MS-AQ |
| ---: | :--- | :---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| 1 | Nano Banana Pro | ✅ | 57.19 | 66.86 | 44.59 | 96.51 | 71.38 | 50.00 | 92.11 | 76.67 | 66.67 | 96.67 | 52.97 | 41.38 | 90.59 | 35.45 | - | 95.00 |
| 2 | SeeDream 4.5 | ❌ | 52.84 | 70.00 | 59.59 | 97.06 | 62.91 | 41.09 | 94.37 | 58.33 | 62.50 | 86.67 | 40.10 | 41.38 | 92.57 | 35.00 | - | 86.82 |
| 3 | Nano Banana | ✅ | 50.66 | 56.47 | 39.04 | 94.12 | 60.46 | 51.91 | 90.20 | 68.33 | 79.17 | 93.33 | 35.50 | 39.47 | 91.00 | 30.28 | - | 93.12 |
| 4 | GPT-Image | ❌ | 47.15 | 58.14 | 41.92 | 93.60 | 58.82 | 32.82 | 93.79 | 49.17 | 62.50 | 92.50 | 43.50 | 33.33 | 90.00 | 28.64 | - | 85.45 |
| 5 | Emu3.5-Image | ❌ | 36.67 | 41.86 | 35.81 | 83.72 | 34.97 | 39.31 | 86.93 | 24.17 | 29.17 | 42.50 | 26.24 | 37.93 | 82.18 | 32.87 | - | 75.46 |
| 6 | FLUX.2-dev | ❌ | 34.39 | 34.30 | 27.70 | 88.95 | 35.76 | 31.01 | 87.09 | 39.17 | 50.00 | 59.17 | 25.25 | 30.17 | 84.16 | 29.82 | - | 79.82 |
| 7 | Gen-Searcher | ✅ | 33.73 | 33.91 | 38.19 | 79.67 | 39.07 | 27.69 | 74.09 | 27.23 | 34.56 | 63.55 | 31.80 | 16.28 | 77.75 | 30.61 | - | 68.68 |
| 8 | **Ours (Bagel)** | ✅ | 32.92 | 39.54 | 44.92 | 66.71 | 36.54 | 26.73 | 67.11 | 30.45 | 35.11 | 47.84 | 23.67 | 36.75 | 57.78 | 34.22 | - | 52.75 |
| 9 | Qwen-Image | ❌ | 30.58 | 36.18 | 27.69 | 71.05 | 36.18 | 27.69 | 71.05 | 26.67 | 45.83 | 55.83 | 27.72 | 20.69 | 71.78 | 25.91 | - | 69.55 |
| 10 | Omini-Gen2 | ❌ | 27.87 | 29.07 | 26.35 | 76.16 | 25.33 | 30.38 | 77.96 | 11.67 | 41.67 | 52.50 | 23.76 | 34.48 | 69.80 | 19.27 | - | 63.76 |
| 11 | Mind-Brush | ✅ | 27.45 | 21.18 | 16.16 | 78.66 | 45.67 | 12.58 | 71.04 | 17.02 | 12.85 | 56.49 | 30.17 | 11.38 | 72.65 | 31.79 | - | 69.98 |
| 12 | Bagel | ✅ | 26.74 | 26.74 | 27.03 | 84.30 | 29.61 | 16.03 | 76.32 | 22.50 | 12.50 | 49.17 | 22.28 | 17.24 | 74.75 | 33.49 | - | 53.67 |
| 13 | GLM-Image | ❌ | 24.71 | 32.94 | 19.86 | 93.53 | 22.37 | 21.15 | 87.50 | 27.50 | 12.50 | 70.83 | 20.30 | 15.52 | 71.29 | 17.73 | - | 70.91 |
| 14 | SeeDream 4.0 | ❌ | 21.26 | 12.05 | 0.70 | 96.39 | 21.57 | 3.44 | 84.64 | 40.00 | 4.17 | 76.67 | 30.69 | 10.34 | 82.67 | 30.73 | - | 80.00 |
| 15 | NextStep-1 | ❌ | 10.44 | 10.74 | 0.40 | 25.12 | 11.33 | 2.54 | 21.67 | 21.50 | 4.20 | 29.17 | 15.49 | 7.55 | 28.71 | 12.80 | - | 20.28 |

---

## 🚀 Quick Start

### 1. Download the Test Dataset
The dataset is available across multiple platforms for your convenience:

* **Hugging Face**: [GENIUS](https://huggingface.co/datasets/HankYang428/GENIUS)
* **Google Drive**: [Download Link](https://drive.google.com/file/d/1NAE1nGbYOrvGvimzSCoDVNebvBdGdIpg/view?usp=drive_link)
* **Baidu Netdisk**: [Download Link](https://pan.baidu.com/s/1ON_ryhfzYHQNzex1gEjCGQ?pwd=iek1) (Password: `iek1`)

### 2. Installation & Directory Setup
Clone the repository and prepare your local environment:

```bash
git clone https://github.com/arctanxarc/GENIUS.git
cd GENIUS
```

After downloading the dataset, ensure your directory structure matches the following:
```text
./
├── cal_score.py           # Scoring script
├── dataset/               # Test dataset
│   ├── implicit_pattern
│   ├── multi_semantic
│   ├── prior_conflicting
│   ├── symbolic_constraint
│   └── visual_constraint
├── eval_prompt.py         # Prompt management
├── eval.py                # Main evaluation logic
├── eval.sh                # Entry script
├── GENIUS.pdf             # Paper
└── README.md
```

### 3. Prepare Model Outputs

Place the images generated by your models into the `outputs` directory. Organize them using the following hierarchy: `outputs/<model_name>/<task_name>/{id}.png`.

> [!IMPORTANT]
>
> The `{id}` must correspond strictly to the id field in `test_data.json` (Note: IDs are unique identifiers, not necessarily a continuous sequence starting from 0).

Example Structure:
```text
./
./outputs/
└── nanobanana/              # Example: Model Name
    ├── implicit_pattern/
    │   ├── 002.png          # Matches ID=002 in ./dataset/implicit_pattern/test_data.json
    │   ├── 003.png
    │   └── ...
    ├── multi_semantic/
    └── ...
```

### 4. Running the Evaluation

Configure your credentials and target models in eval.sh:

1. Set your `API_URL` and `API_KEY` for LMM-as-a-judge.
2. Define the evaluation scope:
```shell
DIMENSIONS=("implicit_pattern" "symbolic_constraint" "visual_constraint" "prior_conflicting" "multi_semantic")
MODELS=("your_model_name")
```
3. Execute the evaluation script:
```shell
bash eval.sh
```

## 📜 License

The dataset and code are released under **CC-BY-NC 4.0** and are intended for academic research **only**. Commercial use is not permitted.

## 📝 Citation

```text
@misc{an2026geniusgenerativefluidintelligence,
      title={GENIUS: Generative Fluid Intelligence Evaluation Suite}, 
      author={Ruichuan An and Sihan Yang and Ziyu Guo and Wei Dai and Zijun Shen and Haodong Li and Renrui Zhang and Xinyu Wei and Guopeng Li and Wenshan Wu and Wentao Zhang},
      year={2026},
      eprint={2602.11144},
      archivePrefix={arXiv},
      primaryClass={cs.LG},
      url={https://arxiv.org/abs/2602.11144}, 
}
```

## 📬 Contact

* Issues: [https://github.com/arctanxarc/GENIUS/issues](https://github.com/arctanxarc/GENIUS/issues)
* Email: [arctanxarc@gmail.com](mailto:arctanxarc@gmail.com)
