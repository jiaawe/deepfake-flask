# Can Detect Or Not Ah?

## Introduction
In the ever-evolving landscape of artificial intelligence (AI), the rise of sophisticated technology has brought with it a double-edged sword. While AI has unlocked unprecedented possibilities and efficiencies across various sectors, it has also given rise to the proliferation of deepfake technology. Deepfakes, a portmanteau of "deep learning" and "fake," represent a formidable manifestation of AI's potential, one that poses a significant problem to society. [1]

IAI is now capable of convincingly replicating human behaviors, voices, and even appearances, paving the way for the creation of deepfake content—artificially generated media, including videos, audio recordings, and images, that seamlessly mimic real-life counterparts. 

The implications of this technology have far-reaching consequences for society at large. From 2022 to Q1 2023, the proportion of deepfakes among all fraud types increased by 4,500% in Canada, by 1,200% in the U.S., by 407% in Germany, and by 392% in the UK. [2]

This reflects the urgent need for reliable detection of synthetic or manipulated images,  which brings us to our problem statement.

Team Members: Calvin Septyanto, Chen Jia Wei, Seah Ding Xuan

## Problem Statement
Our project is a multifaceted initiative aimed at countering the burgeoning threat of deepfake technology across diverse media formats. Our approach leverages a rich, multi-source dataset comprising artificial (fake) and factual (real) images, audio, and video. This project is dedicated to developing advanced detection algorithms capable of identifying manipulated content, regardless of its origin.

## Project Scope
Data Collection and Preprocessing:
<li> Gather a wide variety of deepfake and genuine content, including images, audio, and video, from diverse sources. </li>
<li>Preprocess data to ensure consistency, quality, and compatibility </li> <br>

Model Selection and Development:
<li>Develop and fine-tune CNN models optimized for image-based deepfake detection.</li>
<li>Explore the use of other neural network architectures, such as Recurrent Neural Networks (RNNs) for audio and video content analysis.</li><br>

Training and Validation:
<li>Train the selected neural network models on the multi-source dataset, utilizing a portion for training and a separate portion for testing.</li><br>
<li>Optimize model hyperparameters to maximize classification accuracy.</li>
<li>Implement cross-validation techniques to ensure robustness and prevent overfitting.</li><br>

Evaluation Metrics:
<li>Define appropriate evaluation metrics, such as accuracy, precision, recall, F1-score, and area under the ROC curve (AUC), for assessing model performance.</li><br>

Use Cases and Applications:
<li>Implement deepfake classification tools in a web application </li><br>

Documentation and Reporting:
<li>Maintain clear and organized documentation of data sources, preprocessing steps, model architectures, and results.</li>
<li>Summarize findings, challenges, and outcomes</li><br>

## Solutions & Results
### Image Detection

Convolutional Neural Networks (CNNs) can be a valuable tool for detecting and predicting deepfakes, which are manipulated or generated videos or images created using artificial intelligence techniques, particularly deep learning models. On the extreme ends, using deepfakes can propagate misinformation,  undermine the authenticity of the media and even be misused to escalate political situations. [3] Therefore, our team explored designing a custom CNN architecture and fine-tuned it in an attempt to predict both real images and fake images from a variety of generators. The data comprises 1,531,749 real images and 964,989 fake images with diverse categories including: human faces, animals, places, vehicles and real-life objects [5]. CNN models can potentially learn the different generative methods from the diverse deepfake dataset  (including 13GANs, 7 Diffusion, and 5 miscellaneous generators) that we are training on [4], allowing us to separate real images from generated ones, especially those in these 25 particular generators. The results of the CNN on the test data is as shown below:

|           | Predicted FAKE | Predicted REAL |
|-----------|-----------------|----------------|
| **Actual FAKE** | 161,127         | 31,800         |
| **Actual REAL** | 78,691          | 114,366        |

Accuracy: 71.38% <br>
Precision: 78.25% <br>
Recall: 59.24% <br>
F1 Score: 67.43% <br>

