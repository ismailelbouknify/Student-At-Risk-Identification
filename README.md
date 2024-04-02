# Student-At-Risk-Identification
This repository contains the model architecture and the experimental setup of the paper titled 'Student At-Risk Identification and Classification through Multitask Learning: A Case Study on the Moroccan Education System'.


## Overview:
This repository is part of the DEWS Dropout Early Warning System project, a critical component of the larger initiative to address the challenges of dropout rates in the Moroccan education system. Developed as a collaboration between UM6P (Université Mohammed VI Polytechnique) and the Moroccan Ministry of Education, this project harnesses the power of artificial intelligence (AI) to identify students at risk of academic failure or dropout.

At its core, the project aims to build an AI-based system capable of early detection and intervention for students who are struggling academically or at risk of dropping out of school. Using advanced machine learning algorithms and data analytics techniques, the system aims to analyze various indicators and patterns to accurately predict potential dropout cases.

The primary goal of the DEWS project is twofold: first, to identify students at risk of failure or dropping out early, and second, to provide timely support and interventions to prevent such outcomes. By harnessing the power of AI, the system aims to provide personalized support and resources tailored to the specific needs of each at-risk student, thereby increasing their chances of academic success and retention.

## Models

### Multitask models

The Multitask-ANN architecture consists of an input layer connected to a shared hidden layer of 64 ReLU-activated neurons, followed by a 25\% dropout layer. This is followed by another shared hidden layer of 32 ReLU-activated neurons with dropout applied. The final shared hidden layer contains 16 ReLU-activated neurons. A dense layer with 2 sigmoid activated neurons is added for the at-risk task, while a dense layer with 3 softmax activated neurons is included for the student categorization task. Both tasks minimize the sparse categorical cross-entropy loss.



### Multiclass models

Multiclass models encompass a range of techniques from traditional machine learning to deep learning methods. The ANN-based model architecture includes an input layer with 64 neurons and ReLU activation, followed by a dropout layer (25\% rate), and two hidden layers with 32 and 16 neurons respectively, both activated by ReLU. The output layer comprises 2 neurons with sigmoid activation for binary classification.
![image](https://github.com/ismailelbouknify/Student-At-Risk-Identification/assets/108365289/d71b57e4-a027-46d7-91bb-5219ea77a202)



## Dataset:
![image](https://github.com/ismailelbouknify/Student-At-Risk-Identification/assets/108365289/5e799225-3a14-4d62-b688-e8c0a1101f56)


![image](https://github.com/ismailelbouknify/Student-At-Risk-Identification/assets/108365289/0d123be9-a46e-47ac-85c4-1e790f7383e5)

![image](https://github.com/ismailelbouknify/Student-At-Risk-Identification/assets/108365289/cde22912-50d8-404a-a057-f4d4c409690e)


## Experiment setting

The deep learning models presented in this study were implemented using the TensorFlow and Keras frameworks, while the scikit-learn library was employed for machine learning models. The experiments were conducted on a PowerEdge C6420 Server, equipped with 56 cores of Xeon Platinum 8276L running at 2.2GHz, 1545 GB of RAM, and a single Nvidia Tesla V100 with 16GB of dedicated memory. 
The hyperparameters for the models used in this study are summarised in the following Table:
![image](https://github.com/ismailelbouknify/Student-At-Risk-Identification/assets/108365289/0380e8e0-8490-4185-87c0-b0a56b61bfc9)

## Evaluation

The Figure shows the general pipeline from data splitting to model training and model evaluation.
For multiclass classification, as shown in the Figure, the data were split, with the training dataset used to train models for specific tasks: identification of students at risk (Task 1) or categorization of students (Task 2). The test dataset was then used to evaluate the models.
In contrast, for multitask classification, as shown in The Figure, the training dataset was used to train the model for both tasks simultaneously, and the test dataset was used to evaluate the performance of the models for each task.
All models are evaluated using accuracy, as well as macro-averaged precision, recall, and F1 score. For each class, the formulas are:

![image](https://github.com/ismailelbouknify/Student-At-Risk-Identification/assets/108365289/366deeb3-51a6-4abe-95ad-52cf7b7987b4)

To ensure rigorous evaluation of the models, the dataset was split by randomly selecting 20\% of the data from each academic year for testing. This method ensures that student data from all academic years are included in the test dataset.
All models are evaluated using accuracy, as well as macro-averaged precision, recall, and F1 score. The macro-average is then calculated by averaging these metrics across all classes.

