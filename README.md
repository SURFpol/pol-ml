# Project Open Leermaterialen - Machine Learning
Experiments related to the study investigating the generation of machine-learning based metadata. Please note that all the code in this repository is experimental and not yet suitable for implementation. SURF does not warrant nor support this code. Further details are available in the accompanying report, available on the SURFpol Wiki.

# Data and Preprocessing
The dataset which was used during the experiments consists of documents and video which are available within the Open Leermaterialen project and other sources (WikiWijs, Leraar24, HBO-Verpleegkunde). This results in a dataset which includes approximately 850 documents and 255 videos. 

The experiments focused on automatic classfication based on the type of content (Lesson, Assignment, Reference, Test). During preprocessing, all documents are converted to PDF. This enables us to automatically generate images based on each page of the documents, which are suitable as CNN input. Moreover, extraction of raw text from documents, which serve as input for TF-IDF, is also possible. For each video in the dataset several frames are captured, which can be used as CNN input. If a video contains annotations, these are extracted to be used as TF-IDF input.

# Image Recognition
Convolutional Neural Networks (CNNs) are a type of neural network which is particularly effective in classification and pattern recognition. In this experimental setup, the widely-used VGG16 network is used as a base. By making use of transfer learning we train our own part of the CNN on Open Leermaterialen-data.

# Classifying Text
The raw texts which are extracted from documents and video annotations can be vectorized using the Term Frequency - Inverse Document Frequency (TF-IDF) method. After vectorization, we run a Logistic Regression model to classify texts.
