# IMFM_for-fake-news-detection
# IMFM: Integrate multidimensional frequency features with multi-task learning for fake news detection
#We will upload the complete code and dataset after the paper review process has concluded.

## Introduction


The proposed IMFM is a Fake News Detection framework, which could tackle multi-dimentional frequency features by multi-task learning to achieve better performance.
This project is an improvement of Project [FTT](https://github.com/ICTMCG/FTT-ACL23).

![1](IMFM.png)

## Dataset

Due to review requirements, we cannot release the complete dataset at the moment. We have placed test dataset at `roll_seasonal_data/NDMF_for_paper_review`  so you can test the model. You can create your own dataset following the sample format.

## Code

### File Tree

```bash
.
├── grid_search.py
├── logs  # results save here
│   └── seaonal_res_analyse.ipynb
├── main.py
├── models
│   ├── bert.py
│   └── layers.py
├── requirements.txt
├── reweight_roll_season
│   ├── roll_seasonal_user_data  # adjusted data save here
├── run.sh  
└── utils
    ├── dataloader.py
    └── utils.py
```

### Requirements

Refer to requirements.txt

You can run `pip install -r requirements.txt` to deploy the environment quickly.

### Pretrained Models

We provide models for each season at `param_model` .

### Run


Parameter Configuration:

--gpu 0
--epoch 50
--lr 3e-04
--model_name bert
--root_path reweight_roll_season\roll_seasonal_user_data\NDMF_for_paper_review_SBERT-sg-1.2_prophet-bsr-100_sw-100.0-0.5-1.5
--bert_path .\pre_train_model\bert-base-multilingual-uncased-sentiment
--data_name NDMF_for_paper_review_SBERT-sg-1.2_prophet-bsr-100_sw-100.0-0.5-1.5
--data_type roll_online
--split_level seasonal

You can  complete the testing process running the main.py.


## How To Cite
```
IMFM: Integrate multidimensional frequency features with multi-task learning for fake news detection
Jianyi Zheng, Zirui Zhang, Siming Wang, Rong Yu, Yaqi Hu, Wuchang Zhong. 2026. IMFM: Integrate multidimensional frequency features with multi-task learning for fake news detection. Reviewing.
```
