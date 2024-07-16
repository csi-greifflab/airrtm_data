# AIRRTM_data


This repository contains synthetic data (datasets S1 and S2) from the article [Weakly supervised identification and generation of adaptive immune receptor sequences associated with immune disease status](https://www.biorxiv.org/content/10.1101/2023.09.24.558823v1)


Note that you should unzip the data files before running AIRRTM on them, e.g.:
```shell
git clone git@github.com:csi-greifflab/airrtm_data.git
cd airrtm_data/S1/samples/0.005/
unzip data.zip
cd <airrtm_repo_path>
pipenv shell
python preprocess_data.py -w 0.005 -l 20 --min_len 6 --input_data_dir <airrtm_data_repo_path>/S1
mkdir ./checkpoints
python train_model.py  -w 0.005 -l 20 --input_data_dir <airrtm_data_repo_path>/S1 --checkpoint_dir ./checkpoints
```
