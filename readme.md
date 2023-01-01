<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://i.imgur.com/BtQCfMu.png">
    <img src="https://i.imgur.com/BtQCfMu.png" alt="Logo" width=200 height=200>
  </a>
  
  <h1 align="center">️<b>EVAL-M</b></h1> 
  <h2 align="center"><i>Error Vulnerability Analysis in Language Modelling </i></h2> 
  <h3 align="center">📒 An Interactive Pipeline 📒</h3>


  <p align="center">
  By <i> Niels Aalund Krogsgaard & Jørgen Højlund Wibe </i>
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

## Usage
To use this pipeline you need to adopt the following steps.

**NOTE**: There may be minor variations depending on the terminal and operating system you use. The following pipeline is designed to work using the JupyterNotebook environment Google Colab. If you use a different IDE or operating system, there may be slight variations and hiccups. Furthermore, it requires that pip is installed and you may also want to create a new virtual environment for this project.

1. Clone repository

2. Conduct topic modelling

3. Fine-tune language model(s)

4. Conduct error analysis

## Requirements

* A machine with a GPU (we used Google Colab: a virtual notebook environment that executes code on virtual machines with GPU)
* Python 3.6 or higher
* An R-markdown capable IDE

## 🔧 Set up
1. Clone this repository:

```
git clone https://github.com/jorgenhw/EVALm
```


<br />
<p align="center">  
  <h1 align="center">Section 1</h1>
  <h2 align="center"><i>Topic Modelling</i></h2>
</p>


## 🔧 Set up
1. Navigate to this repository:

```
cd EVALm/topic_modellling
```

2. Open notebook

Open the notebook with the name ```BERTopic_-_template_script.ipynb``` either through your own IDE or through Google Colab (link below).

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1S0gwDVc3tvnO3uvM8i3oOiAPHBFZoKXH#scrollTo=O6svYNzcBB4X)

3. Follow the steps outlined in the notebook but with your own data
4. Save output file

<br />
<p align="center">  
  <h1 align="center">Section 2</h1>
  <h2 align="center"><i>Model Fine-tuning</i></h2>
</p>


## 🔧 Set up
1. Navigate this repository:

```
cd EVALm/model_fine_tuning
```

2. Open notebook

Open the notebook ```Fine_tuning_models_template.ipynb``` either through your own IDE or through Google Colab (link is below).

| Filename    | Colab link |
| ----------- | ----------- |
| ```Fine_tuning_models_template.ipynb```       | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1OjNQI1otcRgYZU6hfBvnkiLocKU_-4hz#scrollTo=EnWYUwwkYOpW)       |


## Content of each notebook
Following are the content of the notebook

1. GPU, installing packages and login to WANDB
2. Installing required packages
3. Importing packages, data and model
4. Preprocessing
    * Removing unwanted words
    * Removing non-Danish sentences
    * Split data into test, training and validation
    * Converting dataset into dataset dict
    * Tokenize data
5. Evaluation metrics
6. Define early stopping function
7. Define hyperparameters
8. Initialize Weights and Biases (WANDB)
9. Hyperparameter tuning
10 Fine-tuning


1. Initialization of GPU, installation of necesarry packages and setup of WANDB
2. Importing libraries, data, and the language model
3. Data preprocessing
4. Fine-tuning
5. Evaluation

<br />
<p align="center">  
  <h1 align="center">Section 3</h1>
  <h2 align="center"><i>Evaluation Method</i></h2>
</p>

## 🔧 Set up
1. Navigate to this repository:

```
cd EVALm/analysis_R
```

2. Open markdown file and follow the steps

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
