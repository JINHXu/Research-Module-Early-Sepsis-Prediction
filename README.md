# Research-Module-WS22

Code repository for Research Module with Prof. Riezler (WS22): Natalia, Pablo, Jinghua

A tranformer-based self-supervised approach to early sepsis prediction using physiological features and clinical notes.

## Important Links to Data/Resources/Colab Notebooks/Write-up

* Large Data Files on Google Drive (share link in a private email)
   
   * Mortality Data _for dry run_ (original) ✅
   
   * Sepsis Data, three additional features (to be added) ☑️
   
   * Sepsis Data, three additional features + clinical notes (to be added) ☑️

__Each dataset is stored in pkl, each pkl loads a `data` table (essentially for pretraining, but also used for tuning) and a `oc` table (essentially for tuning).__

* [Train/test/val split by patient id](https://github.com/JINHXu/Research-Module-WS22-Natalia-Pablo-Jinghua/tree/main/sepsis_id_split) ✅

* [Write-up](https://www.overleaf.com/5363766881tqvnbdymqnfs) (to reveal specifics per chapter) 

* Colab notebooks will be added later

## Data

### Datasets

* [MIMIC-III](https://physionet.org/content/mimiciii/1.4/)
* [Mannheim Data](https://www.cl.uni-heidelberg.de/statnlpgroup/sepsisexp/)

### Features

+ [131 features](https://github.com/JINHXu/Research-Module-WS22-Natalia-Pablo-Jinghua/blob/main/features/pretraining_features.txt) = 129 physiological features + 2 static features (Age & Gender)

+ 3 additional features for sepsis check

+ clinical notes

* ~~Discuss in the first meeting in January~~

  * ~~same features for pretraining and finetuning?~~

* ~~For now: Mannheim features ^ 40 features in wang et al. ^ 40 features in physionet challenge 2019~~


### Data Inspection

* MIMIC-III 

* Mannheim Data

## Models 

* Strats (baseline, physiological features only)

* Strats + Text 

* Wish: More flexible forecasting window!

## ~~Experiments~~

~~Baselines:~~

* ~~[SEFT](https://github.com/BorgwardtLab/Set_Functions_for_Time_Series)?~~
* 



## Evaluation

to be discussed in a later stage

* AUC-ROC (implemented in Strats)
* physionet challenge 2019 Evaluation Scheme [link to python implementation](https://github.com/physionetchallenges/evaluation-2019)

## Further Analysis

* Significance testing: with text vs. without text model

* ~~Ablation Study~~

## OLD NOTES

### MIMIC-III Data

* [Database Physionet](https://physionet.org/content/mimiciii/1.4/)
* [How to get data](https://mimic.mit.edu/docs/gettingstarted/)
* [Application form](https://physionet.org/credential-application/)

### Keep some documentations on overleaf?

[Overleaf Link](https://www.overleaf.com/5363766881tqvnbdymqnfs) (Currently an ACL template)

_I also have a parser for `GitHub markdown` tables to `latex` tables conversion: [link](https://github.com/JINHXu/MDtable2Latex)_

### Problem Setup

Time Series Forecasting consistent with PhysioNet challenge?

> We ask participants to design and implement a working, open-source algorithm that can, based only on the clinical data provided, automatically identify a patient's risk of sepsis and make a positive or negative prediction of sepsis for every time interval. 

Task to do: 

* reimplement architecture in wang et al.

* in our case -> altering a binary classification model into a regression model! MSE loss 

### Resources

* [MIMIC data extraction tool](https://github.com/MLforHealth/MIMIC_Extract)

* code for wang et al.: pending request

* calculate PhysioNet challenge utility score [code](https://github.com/physionetchallenges/python-example-2019)

* [PhysioNet Challenge](https://physionet.org/content/challenge-2019/1.0.0/)

* [SOFA to describe organ failure](https://link.springer.com/content/pdf/10.1007/BF01709751.pdf)

* [TSF with ML](https://www.youtube.com/watch?v=_ZQ-lQrK9Rg&t=185s)

### Extended Reading List

* 

### More thoughts 

Beyond the current approach for time series forecasting

* Survival Analysis? (Time-to-event Analysis)

* various other approaches to TSF 

### Computing Resources

* [bw Uni Cluster](https://login.bwidm.de/service/index.xhtml?serviceId=1012)

* [Jupyter Documentations](https://wiki.bwhpc.de/e/BwUniCluster2.0/Jupyter)

* [File System/Data Management](https://wiki.bwhpc.de/e/BwUniCluster2.0/Hardware_and_Architecture)
