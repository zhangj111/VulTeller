# VulTeller: Learning to Locate and Describe Vulnerabilities
This repository includes our experimental data and source code for our approach that aims at vulnerability localization and description generation.

## Requirements
### Hardware Environment
* Ubuntu 18.04 server
* Intel(R) Xeon(R) Silver 4214 CPU @ 2.20GHz
* 256GB RAM
* GTX3090 GPU.
### Tools
* GCC 7.5.0
* Joern 1.1.1117
### Python Packages (Python 3.8.13)
* ConfigArgParse==1.5.3
* libclang==14.0.6
* lxml==4.9.2
* networkx==2.8.8
* nltk==3.7
* numpy==1.23.3
* nvidia-cublas-cu11==11.10.3.66
* nvidia-cuda-nvrtc-cu11==11.7.99
* nvidia-cuda-runtime-cu11==11.7.99
* nvidia-cudnn-cu11==8.5.0.96
* pandas==1.5.3
* scikit-learn==1.1.2
* torch==1.9.1+cu111
* torchtext==0.5.0
* tqdm==4.64.1
## Instructions
1. Unpack the data file `data/data.rar` to get the training, validation and test sets.
2. `cd VulTeller`
3. `python python joern_parse.py` 
4. `python simplify_cfg.py`
5. `python train.py -g 0 -m loc` for task 1 //This step could be skipped if we have the checkpoint.
6. `python infer.py -g 0 -m loc` 
7. `python train.py -g 0 -m desc` for task 2 //This step could be skipped if we have the checkpoint.
8. `python infer.py -g 0 -m desc` 
