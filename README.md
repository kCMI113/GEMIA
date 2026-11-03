<div align="center">

<h1>[CIKM'26] Generative Multimodal Intent Modeling with Adaptive Integration for Recommendation</h1>

<strong>Official PyTorch Implementation</strong>

</div>

<p align="center">
  <a href="https://doi.org/10.1145/3799682.3841022">Paper</a> ·
  <a href="#citation">Citation</a>
</p>

<p align="center">
  <img src="imgs/overview.png" alt="Overall architecture of GEMIA." width="100%">
</p>

<p align="center"><em>Overview of the GEMIA architecture.</em></p>

## Quick Start

### 1. Environment

```bash
conda create -n gemia python=3.10 -y
conda activate gemia
pip install -r requirements.txt
```

### 2. Data

Preprocessed datasets are available from [Google Drive](https://drive.google.com/drive/folders/1sEMc1-q3CU4lioyvs9-SCUMPObFOFtFg?usp=sharing).

Place each dataset under `data/{data_name}/` with the following files:

```text
data/{data_name}/
├── uniqued_metadata.json
├── uniqued_test_data.pt
├── idx_img_emb_map.pt
└── idx_text_emb_map.pt
```

Use `data_amazon.ipynb` for the Amazon datasets and `data_hm.ipynb` for H&M preprocessing.

### 3. Training

Select one of `Baby`, `Clothing`, `Home`, or `HM` and run:

```bash
python main.py --config Baby
```

Experiment options are defined in `settings/*.yaml`, and outputs are saved under `model/{timestamp}/`. Running without `--config` uses `Baby` by default.

## Citation

If you find this repository useful, please cite the paper:

```bibtex
@inproceedings{10.1145/3799682.3841022,
author = {Kang, Chanmi and Son, Bongguk and Cho, Junsu},
title = {Generative Multimodal Intent Modeling with Adaptive Integration for Recommendation},
year = {2026},
isbn = {9798400725395},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3799682.3841022},
doi = {10.1145/3799682.3841022},
booktitle = {Proceedings of the 35th ACM International Conference on Information and Knowledge Management},
pages = {2008–2019},
numpages = {12},
keywords = {recommender systems, multimodal sequential recommendation, multimodal semantic inference, multimodal fusion},
location = {Rome, Italy},
series = {CIKM '26}
}
```
