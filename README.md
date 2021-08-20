# Deep-Purpose-Tutorial    [![forthebadge](https://forthebadge.com/images/badges/built-with-science.svg)](https://forthebadge.com)
![GitHub last commit](https://img.shields.io/github/last-commit/ssiddhantsharma/deep-purpose-tutorial)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-orange.svg)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/ssiddhantsharma/deep-purpose-tutorial/graphs/commit-activity) 
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
![GitHub forks](https://img.shields.io/github/forks/ssiddhantsharma/deep-purpose-tutorial?style=social)

### A low code tutorial for replicating DeepPurpose Library for Drug-Target Interaction (DTI) for the HackBio'2021 Internship as a part of Team Drug-Development-A
---

![](/banner.png) <br>

Drug-Dev-A will be using an open-source toolkit called [DeepPurpose](https://github.com/kexinhuang12345/DeepPurpose) for Drug-Target Interaction (DTI) prediction which measures the binding affinity of drug molecules to the protein targets. What our team will be doing is replicating some of the DeepPurpose tutorialson our own google colaboratories for checking the reproducibility of the code samples and learning how this toolkit wraps deep learning (DL) models promising performances for DTI prediction to a comprehensive and easy-to-use DL library. Combining machine learned approaches to drug discovery is an effective way as shown by this [web-app](http://deeppurpose.sunlab.org/). This README.md contains all the necessary information to replicate the tutorials for DeepPurpose. <br>

# About DeepPurpose:
![](/figure1.png) <br>

# Working With DeepPurpose:
![](/figure2.png) <br>
**The work-horse for playing with DeepPurpose will be Google Colaboratory or Collab in short. We will be using [Google Colaboratory](https://colab.research.google.com/) to install DeepPurpose and it's dependencies for running/eplicating the tutorials.** 

1. Google Colab does not come with Conda Environment installed. Conda Environment can be installed on google colab through 'pip': 
```
!pip install -q condacolab
import condacolab 
condacolab.install_anaconda()
``` 
2. Checking if Conda is working all fine:
```
import condacolab
condacolab.check()
!conda --version
```
3. All good! Now we will install DeepPurpose and it's dependencies: 
```
%%bash
git clone https://github.com/kexinhuang12345/DeepPurpose.git ## Cloning the DeepPurpose Code Repository
cd DeepPurpose ## Change Directory to DeepPurpose
conda env create -f environment.yml # Creating New Environment
source activate DeepPurpose
```
4. We have DeepPurpose, now installing some other dependencies:
```%%bash
conda install -c conda-forge rdkit
conda install -c conda-forge notebook
```
5. Running a simple file for the tutorial, let's call it drug.py. Contents of drug.py:
```
from DeepPurpose import oneliner  #Importing the oneliner package
from DeepPurpose.dataset import *  #Importing the proprietary library of drugs
oneliner.repurpose(*load_SARS_CoV2_Protease_3CL(), *load_antiviral_drugs(no_cid = True))
``` 
6. Run drug.py as ```python drug.py``` and voila you have retrieved a list of repurposing drugs from a proprietary library.

7. Output that you will get in a text file in your runtime: 
```
----output----
Drug Repurposing Result for SARS-CoV2 3CL Protease
+------+----------------------+------------------------+---------------+
| Rank |      Drug Name       |      Target Name       | Binding Score |
+------+----------------------+------------------------+---------------+
|  1   |      Sofosbuvir      | SARS-CoV2 3CL Protease |     190.25    |
|  2   |     Daclatasvir      | SARS-CoV2 3CL Protease |     214.58    |
|  3   |      Vicriviroc      | SARS-CoV2 3CL Protease |     315.70    |
|  4   |      Simeprevir      | SARS-CoV2 3CL Protease |     396.53    |
|  5   |      Etravirine      | SARS-CoV2 3CL Protease |     409.34    |
|  6   |      Amantadine      | SARS-CoV2 3CL Protease |     419.76    |
|  7   |      Letermovir      | SARS-CoV2 3CL Protease |     460.28    |
|  8   |     Rilpivirine      | SARS-CoV2 3CL Protease |     470.79    |
|  9   |      Darunavir       | SARS-CoV2 3CL Protease |     472.24    |
|  10  |      Lopinavir       | SARS-CoV2 3CL Protease |     473.01    |
|  11  |      Maraviroc       | SARS-CoV2 3CL Protease |     474.86    |
|  12  |    Fosamprenavir     | SARS-CoV2 3CL Protease |     487.45    |
|  13  |      Ritonavir       | SARS-CoV2 3CL Protease |     492.19    |
....
```
---

# Replicated DeepPurpose Tutorials:
### Case Study 1(a): A Framework for Drug Target Interaction Prediction, with less than 10 lines of codes.
In addition to the DTI prediction, we also provide repurpose and virtual screening functions to rapidly generation predictions.

**Link to the binder run for 1(a):** <br>
**[Video-tutorial of 1(a) by a member of team through Loom-App](https://www.loom.com/share/1564269d811d410c9fcdcfdb2f55967a?sharedAppSource=personal_library)** 

### Case Study 1(b): A Framework for Drug Property Prediction, with less than 10 lines of codes.
Many dataset is in the form of high throughput screening data, which have only drug and its activity score. It can be formulated as a drug property prediction task. We also provide a repurpose function to predict over large space of drugs. 

**Link to the binder run for 1(b):** <br>
**[Video-tutorial of 1(b) by a member of team through Loom-App](https://www.loom.com/share/b38b55e16e184b45a3ae0fde3e3a9df0)** 

### Case Study 2 (a): Antiviral Drugs Repurposing for SARS-CoV2 3CLPro, using One Line.
Given a new target sequence (e.g. SARS-CoV2 3CL Protease), retrieve a list of repurposing drugs from a curated drug library of 81 antiviral drugs. The Binding Score is the Kd values.

**Link to the binder run for 2(a):** <br>
**[Video-tutorial of 2(a) by a member of team through Loom-App](https://www.loom.com/share/7e3eac0a45144b9abb60bbea17383f27)** 

### Case Study 2(b): Repurposing using Customized training data, with One Line.
Given a new target sequence (e.g. SARS-CoV 3CL Pro), training on new data (AID1706 Bioassay), and then retrieve a list of repurposing drugs from a proprietary library (e.g. antiviral drugs).

**Link to the binder run for 2(b):**

## DeepPurpose Reference: 
If you found this package useful, please see the publication [DeepPurpose](https://doi.org/10.1093/bioinformatics/btaa1005):

![](/figure3.gif) <br>

## Contributors (Slack Usernames) <br> All people contributed to running their copy of DeepPurpose on Colab
### Case Study 1(a): 
1. @Emon : Installed resources locally and on google colab, replicated Case Study 1(a) and troubleshooting of the errors.
2. @Hameed : Installed resources locally and on google colab, replicated Case Study 1(a) and recording the tutorial video.
3. @Sanjana : Installed resources locally and on google colab, replicated Case Study 1(a) and confirmation of final reproducibility.

### Case Study 1(b): 
1. @eshaan : Installed resources locally and on google colab, replicated Case Study 1(b) and recording the tutorial video.
2. @Ayush : Installed resources locally and on google colab, replicated Case Study 1(b) and troubleshooting of the team's errors.
3. @Anjali : Installed resources locally and on google colab, replicated Case Study 1(b) and confirmation of final reproducibility.

### Case Study 2(a): 
1. @UmasriSankarlal : Installed resources locally and on google colab, replicated Case Study 2(a) and troubleshooting of the team's errors.
2. @jovel : Installed resources locally and on google colab, replicated Case Study 2(a) and recording the tutorial video.
3. @Ayesha : Installed resources locally and on google colab, replicated Case Study 2(a) and confirmation of final reproducibility.

### Case Study 2(b): 
1. @Benson: Installed resources locally and on google colab, replicated Case Study 2(b) and troubleshooting of the team's errors.
2. @Dolu : Installed resources locally and on google colab, replicated Case Study 2(b) and troubleshooting of the team's errors.
3. @Maurya : Installed resources locally and on google colab, replicated Case Study 2(b) and confirmation of final reproducibility.

### Contributors (Slack Usernames)
1. @Jass: All graphical figures in Adobe Suite and setting up Binder.
2. @Siddhant: Idea Generation and Github Repository Management and Netlify Porting.

## 🎨 Future Improvements/Ideas: 
One can try to benchmark DeepPurpose with the very new (August 2021) library, [TorchDrug](https://torchdrug.ai/), might give something good to compare to. More about installing TorchDrug [here](https://rmurphy2718.github.io/posts/2021/08/torch-drug-install/). In case of any questions, please send to siddhaantsharma.ss@gmail.com
