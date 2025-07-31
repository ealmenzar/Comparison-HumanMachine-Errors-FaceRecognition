# Comparison-HumanMachine-Errors-FaceRecognition
This repo contains the “Code & Data” of the paper “A Comparison of Human and Machine Learning Errors in Face Recognition”.

## License
This data and code is released under the GPL License. Please, consider consulting the licenses of the dataset [DemogPairs](https://ihupont.github.io/publications/2019-05-16-demogpairs) and the models [IR50](https://openaccess.thecvf.com/content_cvpr_2016/papers/He_Deep_Residual_Learning_CVPR_2016_paper.pdf) (available in [face.evoLVe](https://github.com/ZhaoJ9014/face.evoLVe)) and [LightCNN](https://ieeexplore.ieee.org/abstract/document/8353856).

****

## Contents
* [Introduction](#Introduction)
* [Errors Set and Hits Set](#ErrorsSetandHitsSet)
* [Models](#Models)
* [Citations](#Citations)

## Introduction

In this repo you can find the data (set of images) used to carry out our experiments. Both sets consist of pairs from the [DemogPairs](https://ihupont.github.io/publications/2019-05-16-demogpairs) testing database, and their classification as _Errors_ or _Hits_ is based on the results obtained from the ensemble machine (IR50 + LightCNN), detailed in in [A Comparison of Human and Machine Learning Errors in Face Recognition](https://arxiv.org/pdf/2502.11337). A total of 5,460 evaluations with DemogPairs pairs was carried out, resulting in 363 errors and 5,097 hits. All the errors and a sample of the hits (180) were tested by a total of 162 participants (10 different pairs per participant, 3 different participants per pair). Participants rated these pairs by answering the question "Are they the same person?" with the options "No", "Probably not", "Not sure", "Probably yes", or "Yes". These two models are [IR50](https://openaccess.thecvf.com/content_cvpr_2016/papers/He_Deep_Residual_Learning_CVPR_2016_paper.pdf) and [LightCNN](https://ieeexplore.ieee.org/abstract/document/8353856), and the joint accuracy over DemogPairs test dataset is above 95%. By "joint accuracy" we mean the accuracy based on the mean response of both models. This ensemble machine is the base decision support system we use in our experiments.

## Errors Set and Hits Set

* ***Errors Set***: A total of 360 errors were made by the ensemble machine. All these 360 pairs were evaluated by a total of 108 participants. In file `human_on_machine_errors.csv` we provide the results from this study.
* ***Hits Set***: A total of 5,097 hits were made by the ensemble machine. A sample of 180 hits was selected to be evaluated by a total of 54 participants. The size of this sample is determined by the limits of the financial resources available to us for this work. To display the results, where necessary, a 180 - 5,097 correction was applied. In `human_on_machine_successes.csv`we provide the results from this study.
## Models
LightCNN pre-trained model is available [at its repo](https://github.com/AlfredXiangWu/LightCNN/tree/master), while IR50 pre-trained model is available through the frameworks [face.evoLVe](https://github.com/ZhaoJ9014/face.evoLVe?tab=readme-ov-file#Model-Zoo). For our experiments we used the ensemble model IR50+LightCNN (we considered the mean response of both models). In `machineIR50.csv` we provide the evaluations of IR50 model on the 5,460 DemogPairs pairs. In `machineLightCNN.csv` we provide the evaluations of LightCNN model on the 5,460 DemogPairs pairs.

## Citations
Please consult and consider citing the following papers:

      @inproceedings{hupont2019demogpairs,
        title={Demogpairs: Quantifying the impact of demographic imbalance in deep face recognition},
        author={Hupont, Isabelle and Fern{\'a}ndez, Carles},
        booktitle={2019 14th IEEE international conference on automatic face \& gesture recognition (FG 2019)},
        pages={1--7},
        year={2019},
        organization={IEEE}
      }
      @article{wang2021face,
        title={Face. evolve: A high-performance face recognition library},
        author={Wang, Qingzhong and Zhang, Pengfei and Xiong, Haoyi and Zhao, Jian},
        journal={arXiv preprint arXiv:2107.08621},
        year={2021}
      }
      @inproceedings{he2016deep,
        title={Deep residual learning for image recognition},
        author={He, Kaiming and Zhang, Xiangyu and Ren, Shaoqing and Sun, Jian},
        booktitle={Proceedings of the IEEE conference on computer vision and pattern recognition},
        pages={770--778},
        year={2016}
      }
      @article{wu2018light,
        title={A light CNN for deep face representation with noisy labels},
        author={Wu, Xiang and He, Ran and Sun, Zhenan and Tan, Tieniu},
        journal={IEEE Transactions on Information Forensics and Security},
        volume={13},
        number={11},
        pages={2884--2896},
        year={2018},
        publisher={IEEE}
      }
