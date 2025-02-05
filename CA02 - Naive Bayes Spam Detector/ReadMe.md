# Building a Spam Detector using Naive Bayes Algorithm

## Overview
This project implements a Naïve Bayes multinomial model to detect spam emails.  
The classifier is trained on a dataset of labeled emails and predicts whether a given email is spam or not spam.  

The model has the following approach: 
- First text features are extracted from a folder full of text file emails.
- A dictionary, that will be referred back to later, is built using the most common 3,000 words.
- Converts emails into feature vectors, with a count of each occurence.
- Trains NB model to classify emails and tests for accuracy. 

**Target Accuracy:** ~96%

---

## Dataset Information
- **Training Data:** 702 emails (351 spam, 351 non-spam)
- **Test Data:** 260 emails (130 spam, 130 non-spam)
- Each email is stored as a **text file**.
- **Spam emails** filenames start with `"spmsg"`.
- The **third line** of each file contains the actual email content.

---

## Libraries
Ensure you have the following Python libraries installed:
- pip install numpy scikit-learn

Furthermore, Google Drive must be mounted, with both train and test files being named correctly.
- "train-mails" and "test-mails" folder should live in a "BSAN6070" folder within personal Google Drive.
    TRAIN_DIR = '/content/drive/MyDrive/BSAN6070/train-mails'
    TEST_DIR = '/content/drive/MyDrive/BSAN6070/test-mails'
- mount Google Drive using drive.mount("/content/drive")

---

## Credit
Template for the majority of the code provided by Dr. Arin Brahma, the professor for this class.
