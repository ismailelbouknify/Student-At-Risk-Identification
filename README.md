# Student-At-Risk-Identification
This repository contains the model architecture and the experimental setup of the paper titled 'Student At-Risk Identification and Classification through Multitask Learning: A Case Study on the Moroccan Education System'.


## Overview:
This repository is part of the DEWS Dropout Early Warning System project, a critical component of the larger initiative to address the challenges of dropout rates in the Moroccan education system. Developed as a collaboration between UM6P (Université Mohammed VI Polytechnique) and the Moroccan Ministry of Education, this project harnesses the power of artificial intelligence (AI) to identify students at risk of academic failure or dropout.

At its core, the project aims to build an AI-based system capable of early detection and intervention for students who are struggling academically or at risk of dropping out of school. Using advanced machine learning algorithms and data analytics techniques, the system aims to analyze various indicators and patterns to accurately predict potential dropout cases.

The primary goal of the DEWS project is twofold: first, to identify students at risk of failure or dropping out early, and second, to provide timely support and interventions to prevent such outcomes. By harnessing the power of AI, the system aims to provide personalized support and resources tailored to the specific needs of each at-risk student, thereby increasing their chances of academic success and retention.

## Models

### Multitask models

The Multitask-ANN architecture consists of an input layer connected to a shared hidden layer of 64 ReLU-activated neurons, followed by a 25\% dropout layer. This is followed by another shared hidden layer of 32 ReLU-activated neurons with dropout applied. The final shared hidden layer contains 16 ReLU-activated neurons. A dense layer with 2 sigmoid activated neurons is added for the at-risk task, while a dense layer with 3 softmax activated neurons is included for the student categorization task. Both tasks minimize the sparse categorical cross-entropy loss.
![Uploading MTDNN.png…]()



### Multiclass models

Multiclass models encompass a range of techniques from traditional machine learning to deep learning methods. The ANN-based model architecture includes an input layer with 64 neurons and ReLU activation, followed by a dropout layer (25\% rate), and two hidden layers with 32 and 16 neurons respectively, both activated by ReLU. The output layer comprises 2 neurons with sigmoid activation for binary classification.
![DNN](https://github.com/ismailelbouknify/Student-At-Risk-Identification/assets/108365289/fedcaae7-9648-4231-9b91-85873ddc35c5)


## Dataset:
![image](https://github.com/ismailelbouknify/Student-At-Risk-Identification/assets/108365289/5e799225-3a14-4d62-b688-e8c0a1101f56)

## Experiment setting
## Evaluation
