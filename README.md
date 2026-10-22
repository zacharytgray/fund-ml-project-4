# Project 4: Neural Networks, CNNs, and Transformers

CS-4103 Fundamentals of Machine Learning, University of Tulsa

## What is here

- `assignment/Assignment 4.1.ipynb`, `assignment/Assignment 4.2.ipynb`, and `assignment/Assignment 4.3.ipynb`, the three notebooks you complete. 4.1 covers layered, feedforward networks on the handwritten digits, German Credit, and Mushroom datasets. 4.2 covers convolutional networks on Fashion-MNIST and MNIST. Both evaluate every model with 5-fold cross-validation. 4.3 covers scaled dot-product attention: you check it against the pretrained BERT model, watch BERT fill in a hidden word, and plot what its attention heads look at.
- `data/`, German Credit and Mushroom. The digits dataset comes with scikit-learn. Fashion-MNIST and MNIST download into `data/` the first time 4.2 runs, and BERT downloads into the Hugging Face cache the first time 4.3 runs.
- `assignment/Project 4 - Neural Networks, CNNs, and Transformers.pdf`, the project spec. The same PDF is posted on Harvey.

Sources: Statlog (German Credit Data) and Mushroom are from the UCI Machine Learning Repository. Of the Mushroom data's 22 categorical features, veil type has a single value and is dropped; the other 21 are one-hot encoded into 116 columns, with a missing stalk root kept as its own category. Fashion-MNIST is from Zalando Research, MNIST from Yann LeCun, Corinna Cortes, and Christopher Burges, and `bert-base-uncased` from Google, through Hugging Face.

## Running in Colab

Run the notebooks in Google Colab. Colab already has every library this project uses, and 4.2 runs much faster on its free T4 GPU.

- [Assignment 4.1 in Colab](https://colab.research.google.com/github/zacharytgray/fund-ml-project-4/blob/main/assignment/Assignment%204.1.ipynb)
- [Assignment 4.2 in Colab](https://colab.research.google.com/github/zacharytgray/fund-ml-project-4/blob/main/assignment/Assignment%204.2.ipynb)
- [Assignment 4.3 in Colab](https://colab.research.google.com/github/zacharytgray/fund-ml-project-4/blob/main/assignment/Assignment%204.3.ipynb)

After you open one, save your own copy with **File > Save a copy in Drive** and work in that copy. For 4.2, choose **Runtime > Change runtime type > T4 GPU** before you run anything. In 4.1 and 4.2, run the first code cell every time you open the notebook: it copies this repository onto the Colab machine so the notebook finds `../data`.

## Running on your own computer

Use Python 3.10 or newer.

    pip install -r requirements.txt
    jupyter notebook

Open the notebooks from the `assignment` folder. They load data through `../data`, so they fail if you move them or start them elsewhere. 4.2 is slow without a GPU. It uses one on its own when it finds one, including the GPU of an Apple silicon Mac.

## Working in the notebooks

Every network in this project is built from PyTorch layers, and PyTorch computes the gradients. The data loading, the training and testing functions, and the plots are already written. Your job is to build each architecture, choose how many epochs to train it, write scaled dot-product attention in 4.3, and write about what you see.

Fill in each `TODO`. The numbered comment above a `TODO` lists the steps that region needs.

Import nothing beyond the libraries listed in the import cell.

Run every cell, top to bottom, before you submit. 4.2 downloads Fashion-MNIST and MNIST the first time it runs, and 4.3 downloads BERT, about 440 MB.

## Submitting

Submit through Harvey:

- All three notebooks, with all outputs visible. In Colab, download each one with **File > Download > Download .ipynb**.
- The report PDF described in the spec.

A notebook with cleared outputs is graded as though the code did not run.
