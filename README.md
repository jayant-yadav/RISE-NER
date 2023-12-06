# MultiNERD-NER
NER model repo for MultiNERD dataset from HF 🤗

## Resources   
Following resources were utitlized to develop this project:  
Kaggle - GPU T4x2  
Google Colab - GPU T4x1  
Dataset: https://huggingface.co/datasets/Babelscape/multinerd  
Pretrained model: https://huggingface.co/roberta-base  


The fine-tuned models and dataset have been uploaded and distributed for public good.    
Find them on Kaggle: https://www.kaggle.com/datasets/jayantyadav/multinerd-ner-models/

The findings and limitations have been recorded in `MultiNERD_NER__RISE.pdf`.   
The english subset of the dataset has been shared under the folder `dataset`.

<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple example steps.

### Prerequisites

The project currenlty runs on jupyter notebook and requires CUDA enabled GPU.

* Install Jupyter notebook as such (or visit https://jupyter.org/install)
  ```sh
  pip install notebook
  ```

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/jayant-yadav/RISE-NER.git
   ```
2. Create virtual environment and activate it
   ```sh
   python -m venv './NER' --upgrade-deps
   ```
3. cd into the local repository and install python packages
   ```sh
   pip install -r ./requirement.txt
   ```

### Usage  
Either spin up your jupyter notebook server or VSCode in order to run .ipynb scripts.  

_finetuning.ipynb_: 
* Contains code for finetuning RoBERTa-base models. 
* Run code line by line. Comments are added for better understanding.
* Toggle `is_systemB` variable to switch from system A to system B. 
* Take note of model file name after it is saved. The file path will be used for evalution later.  

_evalution.ipynb_:
* Contains code for evaluting fine-tuned models on Test dataset.
* Run code line by line. Comments are added for better understanding.
* Toggle `is_systemB` variable to switch from system A to system B. 
* Use the appropriate model file path to run the correct model checkpoints. 