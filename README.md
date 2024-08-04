# Pretraining and Finetuning Demo

This is the code used to demonstrate the benefits of pretraining and finetuning in constructing ML foundation models for the publication:

```
Matthias Ihme and Wai Tong Chung. Artificial Intelligence as a Catalyst for Combustion Science and Engineering. Proc Combust. Inst. 40 (2024). In Press.
```

## 0. Env setup 
1. We use Python 3.10.12 in this work. For the conda command:
```
conda create -n my_env python=3.10.12
conda activate my_env 
```
2. Followed by the following pip install:

```
pip install -r requirements.txt 
```
## 1. Pretraining
Pretraining notebook is avaiable here: https://www.kaggle.com/code/waitongchung/pretraining-2d-sr-from-scratch
    * This notebook is already linked to the dataset used for pretraining.
    * This generates the pretrained checkpoint in `./ckpt/ckpt-92/` that is used for finetuning

## 2. Finetuning and Training from Scratch
1. This is done in `finetune_and_scratch.ipynb` where we (i) finetuned the pretrained model and (ii) and train another model from scratch. 
2. Logs and model checkpoints from the two training approaches are then compared in `plot.ipynb`.
3. Finetuning dataset is in `./dataset/`. This is extracted from the reference below.

## 3. Checkpoints here
1. For brevity, only first, last, and best model checkpoints are saved in this repo. See training info in the provided logs and use provided notebooks to recreate experiments.

## 4. Citation Info
1. To cite this work and code, use:
```
@article{ihme2024,
  title={Artificial Intelligence as a Catalyst for Combustion Science and Engineering},
  author={Ihme, Matthias and Chung, Wai Tong},
  journal={Proceedings of the Combustion Institute},
  volume={40},
  year={2024},
  note={In Press}
}
```
2. For the dataset, cite:
```
@article{chung2024turbulence,
  title={Turbulence in focus: {B}enchmarking scaling behavior of {3D} volumetric super-resolution with {BLASTNet} 2.0 data},
  author={Chung, Wai Tong and Akoush, Bassem and Sharma, Pushan and Tamkin, Alex and Jung, Ki Sung and Chen, Jacqueline and Guo, Jack and Brouzet, Davy and Talei, Mohsen and Savard, Bruno and others},
  journal={Advances in Neural Information Processing Systems},
  volume={36},
  pages = {77430--77484},
  year={2024}
}
```