# Classification of Galaxies using CNN, ResNet-50 and BYOL

This repository contains implementations of a Convolutional Neural Network (CNN), ResNet-50, and Bootstrap Your Own Latent (BYOL). The main objective of this work is to compare these architectures in a galaxy morphology classification task using the Galaxy10 DECaLS dataset.

The collaborative work was developed by **Deyvisson Garcês**, **Inayê Melo**, **Eduardo Cherobin**, **Thamara Medeiros**,  and **Nicoly Rodrigues**.
---
## Galaxy10 Decision Tree

The decision tree used to define the Galaxy10 morphological classes is shown below. This hierarchy was used as a reference for the classification task.

![Galaxy10 decision tree](Imagens/01_ArvoreDecisaoGalaxyZoo.jpeg)

---
## Dataset

The Galaxy10 DECaLS dataset consists of galaxy images divided into 10 morphological classes.

![Galaxy10 labels](Imagens/galaxies-labels.png)

The dataset is highly imbalanced. Some classes contain up to eight times more samples than others, as illustrated in the figure below.

![Number of samples per class](Imagens/number-byclass.png)

---

## Models

### Convolutional Neural Network (CNN)

The CNN architecture was designed specifically for this task, aiming to balance model complexity and generalization performance.

![CNN architecture](Imagens/08_CNNArquitetura.png)

---

### ResNet-50

ResNet-50 is a deep residual network that employs skip connections to mitigate the vanishing gradient problem and enable the training of deeper architectures.

![ResNet-50 architecture](Imagens/ResNet-50_Arquitetura.png)

---

### BYOL (Bootstrap Your Own Latent)

BYOL is a self-supervised learning framework that learns image representations without the use of negative samples. The learned representations are later fine-tuned for the galaxy classification task.

![BYOL framework](Imagens/03_ByolArquitetura.jpg)

---

## Experimental Results

Several experiments were conducted using the architectures described above. Training and validation losses, as well as accuracy curves, are shown below.

![Training and validation curves](Imagens/losses-accuracy.png)

---

## Confusion Matrices

The confusion matrices below illustrate the classification performance of each model on the test set.

### CNN
![CNN confusion matrix](Imagens/15_CM_CNNpng.png)

### ResNet-50
![ResNet-50 confusion matrix](Imagens/16_CM_Resnet.png)

### BYOL
![BYOL confusion matrix](Imagens/17_CM_BYOL.png)

---

## Recall per Class

The following figure shows the recall obtained for each class, highlighting the impact of class imbalance on the models' performance.

![Recall per class](Imagens/11_RecallClasse.png)

---

## Quantitative Metrics

The table below summarizes the main quantitative metrics obtained for each model.

![Metrics Table](Imagens/12_TabelaMetricas.jpg)



