<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://i.imgur.com/BtQCfMu.png">
    <img src="https://i.imgur.com/BtQCfMu.png" alt="Logo" width=200 height=200>
  </a>
  
  <h1 align="center">️// **EVAL-M** //</h1> 
  <h2 align="center"><i>**E**rror **V**ulnerability **A**nalysis in **L**anguage **M**odelling </i></h2> 
  <h3 align="center">🧠 Cognitive Science // Bachelor Thesis 🧠</h3>


  <p align="center">
    Niels Aalund Krogsgaard & Jørgen Højlund Wibe
  </p>
</p>

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About the project</a></li>
      <ul>
        <li><a href="#structure-of-the-readme-file">Structure of the readme file</a></li>
    </ul>
    <li><a href="#section-1">Section 1: <i>Topic Modelling</i></a></li>
     <ul>
      <li><a href="#setup">Setup</a></li>
      <li><a href="#conclusion">Conclusion</a></li>
    </ul>
    <li><a href="#section-2">Section 2: <i>Fine-Tuning Models</i></a></li>
     <ul>
      <li><a href="#setup">Setup</a></li>
      <li><a href="#content-of-each-notebook">Content of each notebook</a></li>
      <li><a href="#conclusion">Conclusion</a></li>
    </ul>
    <li><a href="#section-3">Section 3: <i>Evaluation Method</i></a></li>
     <ul>
      <li><a href="#setup">Setup</a></li>
      <li><a href="#content-of-markdown-file">Content of markdown file</a></li>
      <li><a href="#conclusion">Conclusion</a></li>
    </ul>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About the project
EVAL-m is a method for subgroup error analysis is a technique that involves examining the performance of a language model on specific subgroups of data in order to understand where the model is making mistakes. This can be useful for identifying and addressing sources of bias in the model, as well as for identifying areas where the model may be particularly weak. To conduct a subgroup error analysis, one would first identify relevant subgroups of data, such as examples that contain specific types of errors or examples that pertain to certain domains. The model's performance on these subgroups would then be compared to its overall performance in order to identify patterns and trends in the errors it is making. This information can be used to adjust the model's training data or algorithms in order to improve its overall performance.

EVAL-m consists of three phases: In the first phase, you apply a topic model to your data. In the second phase, you fine-tune a language model of interest on an annotated part of your data. In the last phase, you do error analysis on the subgroups made by the topic model. 

### Structure of the readme file
This file is structures as a pipeline, meaning that it contains step 1-9 on how to conduct the error analysis. There are three main sections:

* **Section 1:** describes on how to do topic modelling with BERTopic in python.

* **Section 2:** Describes how to fine-tune models available on HuggingFace with TransformersAPI. 

* **Section 3:** contains a reproducible R-markdown script outlining how to conduct the final sub-group error analysis.

## Requirements

* A machine with a GPU (we used Google Colab: a virtual notebook environment that executes code on virtual machines with GPU)
* Python 3.6 or higher
* An R-markdown capable IDE

## Data
aøsdpfkm

<br />
<p align="center">  
  <h1 align="center">Section 1</h1>
  <h2 align="center"><i>Topic Modelling</i></h2>
</p>

## 🔧 Set up
1. Clone this repository:

```
git clone https://github.com/jorgenhw/bachelor_thesis
cd bachelor_thesis/topic_modelling
```

2. Open notebook of interest

Open the notebook with the name of the topic modelling method you want to examine e.g. ```LDA.ipynb``` either through your own IDE or through Google Colab (links are provided in the table below).

The below table outlines which notebooks contains which methods.

| Method      | Filename | Colab link |
| ----------- | ----------- | ----------- |
| Non-Negative Matrix Factorization (NMF)      | NMF.ipynb       | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1PfB7Xtf3NmcUYfu5muydD2bNB_AMz8PW)       |
| Latent Dirichlet Allocation   | Text        | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1IoNVFxeqQTJTztl9ezG12BnC4NDEAt-M)        |
| TweeTopic   | Text        | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1q1WYhRYJYb13hMwGvZRZ0MxP5X3eWVp0)        |
| BERTopic   | Text        | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1P6t6s52G6ySedTDg_09bO_c_7SyQlv9u)        |

## Conclusion
In conclusion, the experiment we conducted to compare the performance of four topic modelling methods - NMF, LDA, BERTopic, and TweeTopic - showed that BERTopic was the best performer, meaning it was able to create the most human interpretable subgroups in the data. This was demonstrated through the evaluation method of qualitative assessment.



<br />
<p align="center">  
  <h1 align="center">Section 2</h1>
  <h2 align="center"><i>Model Fine-tuning</i></h2>
</p>


## 🔧 Set up
1. Clone this repository:

```
git clone https://github.com/jorgenhw/bachelor_thesis
cd bachelor_thesis/model_fine_tuning
```

2. Open notebook of interest

Open the notebook with the name of the model you want to examine e.g. ```jonfd/electra-small-nordic.ipynb``` either through your own IDE or through Google Colab (links are provided in the table below).

The below table outlines which notebooks contains which models.

| Model      | Filename | Colab link |
| ----------- | ----------- | ----------- |
| ScandiBERT      | Title       | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Sluei065T_VH_XgXQi85OzmfPBlVoARc)       |
| XLM-RoBERTa Large   | Text        | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1IoNVFxeqQTJTztl9ezG12BnC4NDEAt-M)        |
| XLM-RoBERTa Base   | Text        | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1q1WYhRYJYb13hMwGvZRZ0MxP5X3eWVp0)        |
| Nordic ELECTRA-Small   | Text        | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1P6t6s52G6ySedTDg_09bO_c_7SyQlv9u)        |
| AELAECTRA   | Text        | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1S0gwDVc3tvnO3uvM8i3oOiAPHBFZoKXH#scrollTo=O6svYNzcBB4X)        |
| RøBÆRTa   | Text        | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1S0gwDVc3tvnO3uvM8i3oOiAPHBFZoKXH#scrollTo=O6svYNzcBB4X)        |
| Danish BERT BotXO   | Text        | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1S0gwDVc3tvnO3uvM8i3oOiAPHBFZoKXH#scrollTo=O6svYNzcBB4X)        |
| DeBERTaV3   | Text        | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1S0gwDVc3tvnO3uvM8i3oOiAPHBFZoKXH#scrollTo=O6svYNzcBB4X)        |
| Twitter-XLM-Roberta-base   | Text        | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1S0gwDVc3tvnO3uvM8i3oOiAPHBFZoKXH#scrollTo=O6svYNzcBB4X)        |
| NB-BERT-large   | Text        | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1kFfVYTD47VFat5BOJH4I8rLVn8R1rmLt)        |


## Content of each notebook
Each notebook consist of five steps

1. Initialization of GPU, installation of necesarry packages and setup of WANDB
2. Importing libraries, data, and the language model
3. Data preprocessing
4. Fine-tuning
5. Evaluation

## Conclusion
In this project, we have successfully finetuned 11 Danish language models to demonstrate how a more fine-grained sub group error analysis metric can reveal new insights into language models. Suggestions for further research can be found in the paper _'A Deep Dive Into Danish NLP'_ (link provided in the top of this readme).

This project is part of a bachelor thesis in Cognitive Science at Aarhus University, Denmark, 2023.

<br />
<p align="center">  
  <h1 align="center">Section 3</h1>
  <h2 align="center"><i>Evaluation Method</i></h2>
</p>

## 🔧 Set up
1. Clone this repository:

```
git clone https://github.com/jorgenhw/bachelor_thesis
cd bachelor_thesis/analysis_R
```

2. Open markdown file 

## Content of markdown file

## Conclusion
In this markdown file we demonstrate how to conduct a subgroup error analysis on the performance of the fine-tuned models (section 2) in the the topics made by BERTopic in  section 1.

Instead of arriving at the trivial conclusion that larger models also have the highest accuracy in the sub-groups, we instead calculate the difference between each sub-group accuracy and the overall accuracy of a given language model. This is done through leave-one-group-out mean calculation to reduce the data-leakage between accuracy scores, since we are interested in the difference between a sub-group and all other groups that are not that sub-group. We call the resulting values a Relative Topic Accuracy Correction (RTAC). 

<br />
<p align="center">  
  <h1 align="center">💬 Contact 💬</h1>
</p>
Feel free to contact the authors, [Jørgen Højlund Wibe](https://github.com/jorgenhw) or [Niels Aalund Krogsgaard](https://github.com/nielsaak) for any questions regarding the project.
You may do so through our emails ([Jørgen](mailto:201807750@post.au.dk), [Niels](mailto:202008114@post.au.dk))
<br />

<br />
<p align="center">  
  <h1 align="center">Acknowledgements</h1>
</p>

We would like to express our sincere gratitude to Google Colab and Hugging Face for their invaluable contributions to the field of machine learning and natural language processing.

Google Colab has provided us with a powerful platform for conducting research and development, allowing us to access state-of-the-art resources and technologies without the need for expensive hardware or software. Its intuitive interface and seamless integration with Google Drive have made it an essential tool for collaborating together and sharing our findings.

Hugging Face, on the other hand, has revolutionized the way we work with transformer-based models, providing us with a vast library of pre-trained models and a user-friendly API that allows us to easily fine-tune and deploy them for various tasks. Its commitment to open source and constantly updating its offerings have made it a go-to resource for researchers and practitioners alike.
