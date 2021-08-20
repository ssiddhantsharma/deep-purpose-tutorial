# Deep-Purpose-Tutorial    [![forthebadge](https://forthebadge.com/images/badges/built-with-science.svg)](https://forthebadge.com)
![GitHub last commit](https://img.shields.io/github/last-commit/ssiddhantsharma/deep-purpose-tutorial)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-orange.svg)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/ssiddhantsharma/deep-purpose-tutorial/graphs/commit-activity) 
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
![GitHub forks](https://img.shields.io/github/forks/ssiddhantsharma/deep-purpose-tutorial?style=social)

### A low code tutorial for replicating DeepPurpose Library for Drug-Target Interaction (DTI) for the HackBio'2021 Internship as a part of Team Drug-Development-A

![](https://github.com/ssiddhantsharma/team-greider/blob/main/HackBio.jfif) <br>

Drug-Dev-A will be using an open-source toolkit called DeepPurpose [https://github.com/kexinhuang12345/DeepPurpose] for Drug-Target Interaction (DTI) prediction which measures the binding affinity of drug molecules to the protein targets. The toolkit is developed fairly recent in 2020 by Marinka Zitnik's lab at Harvard [https://zitniklab.hms.harvard.edu/drugml/], using a concoction of AI algorithms for end-to-end drug development. What our team will be doing is replicating some of the DeepPurpose tutorialson our own google colaboratories for checking the reproducibility of the code samples and learning how this toolkit wraps deep learning (DL) models promising performances for DTI prediction to a comprehensive and easy-to-use DL library. Combining machine learned approaches to drug discovery is an effective way as shown by this web-app by the lab: http://deeppurpose.sunlab.org/. This README.md contains all the necessary information to replicate the tutorials for DeepPurpose. <br>

# About DeepPurpose:
![](/figure1.png) <br>

# DeepPurpose Installation:
![](/figure2.png) <br>
One can try to install DeepPurpose for replicating the tutorials either on their local machine or on [Google Colaboratory](https://colab.research.google.com/)
We recommend to install it on Google Colab for faster, on-cloud performances. Conda needs to be installed on Google Colab and can be done through: https://towardsdatascience.com/conda-google-colab-75f7c867a522

To install locally, we recommend to install from `pip`:
```bash
conda create -n DeepPurpose python=3.6
conda activate DeepPurpose
conda install -c conda-forge rdkit
conda install -c conda-forge notebook
pip install git+https://github.com/bp-kelley/descriptastorus 
pip install DeepPurpose
```
# Tutorials:
### Case Study 1(a): A Framework for Drug Target Interaction Prediction, with less than 10 lines of codes.
In addition to the DTI prediction, we also provide repurpose and virtual screening functions to rapidly generation predictions.

### Case Study 1(b): A Framework for Drug Property Prediction, with less than 10 lines of codes.
Many dataset is in the form of high throughput screening data, which have only drug and its activity score. It can be formulated as a drug property prediction task. We also provide a repurpose function to predict over large space of drugs. 

### Case Study 2 (a): Antiviral Drugs Repurposing for SARS-CoV2 3CLPro, using One Line.
Given a new target sequence (e.g. SARS-CoV2 3CL Protease), retrieve a list of repurposing drugs from a curated drug library of 81 antiviral drugs. The Binding Score is the Kd values.

### Case Study 2(b): Repurposing using Customized training data, with One Line.
Given a new target sequence (e.g. SARS-CoV 3CL Pro), training on new data (AID1706 Bioassay), and then retrieve a list of repurposing drugs from a proprietary library (e.g. antiviral drugs).

### Contributors (Slack Usernames)
### Case Study 1(a): 
1. @Emon : Installed resources locally and on google colab, replicated Case Study 1(a) and troubleshooting of the errors.
2. @Hameed : Installed resources locally and on google colab, replicated Case Study 1(a) and troubleshooting of the errors.
3. @Sanjana : Installed resources locally and on google colab, replicated Case Study 1(a) and confirmation of final reproducibility.

### Case Study 1(b): 
1. @eshaan : Installed resources locally and on google colab, replicated Case Study 1(b) and troubleshooting of the team's errors.
2. @Ayush : Installed resources locally and on google colab, replicated Case Study 1(b) and troubleshooting of the team's errors.
3. @Anjali : Installed resources locally and on google colab, replicated Case Study 1(b) and confirmation of final reproducibility.

### Case Study 2(a): 
1. @UmasriSankarlal : Installed resources locally and on google colab, replicated Case Study 2(a) and troubleshooting of the team's errors.
2. @jovel : Installed resources locally and on google colab, replicated Case Study 2(a) and troubleshooting of the team's errors.
3. @Ayesha : Installed resources locally and on google colab, replicated Case Study 2(a) and confirmation of final reproducibility.

### Case Study 2(b): 
1. @Benson: Installed resources locally and on google colab, replicated Case Study 2(b) and troubleshooting of the team's errors.
2. @Dolu : Installed resources locally and on google colab, replicated Case Study 2(b) and troubleshooting of the team's errors.
3. @Maurya : Installed resources locally and on google colab, replicated Case Study 2(b) and confirmation of final reproducibility.

### Contributors (Slack Usernames)
1. @Jass: All graphical representation in Adobe Suite. 
2. @Siddhant: Idea Generation and Github Repository Management.

# Contact
Please send questions to siddhaantsharma.ss@gmail.com
