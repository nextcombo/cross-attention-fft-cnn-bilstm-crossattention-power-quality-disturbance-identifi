# Cross Attention FFT + CNN -BiLSTM-CrossAttention Power Quality Disturbance Identification Model for Time-Domain and Frequency-Domain Features

The family set includes the following content:
Thesis innovation!!!
The cross-attention mechanism can model the degree of correlation between different features, extracting important features from both frequency and time domain characteristics for model recognition, with significant effects.
50 epochs, with 100% accuracy. The FFT+CNN-BiLSTM-CrossAttention network achieves significant results in classification. The model can fully extract spatial and temporal features as well as frequency domain features from perturbation signals. It converges quickly and performs exceptionally well, currently the highest precision method among previous articles. Innovation is also present!!!
Includes a complete dataset of power quality disturbance signals, as well as a fully generated and prepared dataset of ten types of disturbance signals, classified data, and label sets, all of which can be run.
Includes code for data preprocessing and the FFT+CNN-BiLSTM-CrossAttention classification model.
Environment: Python 3.9
Innovation Point: Utilizing cross-attention mechanism to fuse the model!
Preface
This article introduces the FFT (Fast Fourier Transform) for data preprocessing and the implementation of a CNN-BiLSTM-CrossAttention model based on FFT for classifying power quality disturbance signals using Python. For more detailed information about the simulation of power quality disturbance signals in Python, please refer to the following text (Appendix 10 contains the 10-class dataset):
\tPython - Data Introduction and Classification of Electric Power Quality Disturbance Signals
The waveform diagram of some disturbed signal types is as follows:
\t  
Overall Model Structure
The overall structure of the model is as follows: The one-dimensional perturbation signal undergoes FFT transformation to extract its frequency domain features, and the signal itself has its time domain features. These features are then processed through CNN convolutional pooling operations to extract global features. Subsequently, BiLSTM is used to extract sequential features. The cross attention mechanism is employed to fuse both time and frequency domain features. Through calculating attention weights, the model focuses more on important features for feature enhancement and fusion. Finally, the full connection layer and softmax output classification results.
Time domain and frequency domain feature extraction:
Apply FFT to the time domain signal to convert it into the frequency domain.
Use CNN to learn and extract frequency domain features. The convolutional layers of CNN can capture local patterns in the frequency domain features.
BiLSTM network:
Input the time domain signal into the BiLSTM network. BiLSTM (Bidirectional Long Short-Term Memory) can effectively capture the long-term dependencies of the time domain signal.
Cross attention mechanism:
Use the cross attention mechanism to fuse time and frequency domain features. This can be achieved by calculating attention weights, allowing the model to focus more on important features.
Fast Fourier Transform (FFT) principle introduction:
Fourier transform is a tool for signal processing and spectral analysis, converting a signal from the time domain to the frequency domain. Fast Fourier Transform (FFT) is an efficient algorithm for implementing Fourier transform, especially suitable for discrete signal processing.
First step, import part of the data, visualize perturbation signals:
Second step, perturbation signals undergo FFT visualization:
Preprocessing of power quality disturbance data:
2.1 Import data:
Based on the reference IEEE Std1159-2019 Power Quality Detection Standard and related literature, a model for perturbation signals was constructed, generating 10 types of single signals and various composite disturbance signals. Following previous articles, preprocessing of 10-classification of perturbation signals was carried out:
First step, generate single signals according to the formula model.
Single disturbance signal visualization:
\t  
2.2 Dataset Production
\tCreating dataset and classification labels
\t  
3 Cross Attention Mechanism
\t3.1 Cross Attention Concept
\tThe two sequences must have the same dimensions.
\tThe two sequences can be different patterns (such as: text, sound, image).
A sequence as input defines the output sequence length, and another sequence provides the input K&V.
3.2 Cross-attention Algorithm
\tCalculate K and V for S1.
Calculate Q for S2
\tCalculate the Attention Matrix Based on K and Q
\tApply V to the Attention Matrix
The output sequence length is consistent with S2.
During the fusion process, we use the frequency domain features transformed by FFT as query sequences and temporal features as key-value pairs. By calculating the attention weights between the query sequences and the key-value pairs, we can model the degree of association between different features.
4. FFT+CNN-BiLSTM-CrossAttention Perturbation Signal Identification Model
4.1 Network Definition Model
\tNote: The input fault signal data shape is [64, 1024], batch_size=64, where 1024 represents the length of perturbation signal sequence.
4.2 Set parameters and train the model
50 epochs, with an accuracy nearing 100%. The FFT+CNN-BiLSTM-CrossAttention integrated network model significantly improves classification performance. The model can fully extract spatial and temporal features as well as frequency domain features from the disturbance signals of electrical energy quality. It converges rapidly, exhibits superior performance, high accuracy, and the cross attention mechanism models the correlation degree between different features. It effectively extracts critical features from both the frequency domain and time domain characteristics of the disturbance signals, leading to significant improvements in model recognition.
4.3 Model Evaluation
Accuracy, Precision, Recall, F1 Score
\tPerturbation signal classification confusion matrix:
Previously Featured Content:
Python - Data Introduction and Classification of Power Quality Disturbance Signals
Python Classification of Disturbance Signals in Electric Power Quality (I) One-Dimensional Signal Classification Based on LSTM Model
Python Classification of Disturbance Signals in Electric Power Quality (II) - One-Dimensional Signal Classification Based on CNN Model
Python Power Quality Disturbance Signal Classification (III) - One-Dimensional Signal Classification Model Based on Transformer
Python Power Quality Disturbance Signal Classification (IV) - One-Dimensional Signal Classification Model Based on CNN-BiLSTM
Python Power Quality Disturbance Signal Classification (V) One-Dimensional Signal Classification Model Based on CNN-Transformer
Based on FFT + CNN - BiGRU-Attention, the model for fusion of time and frequency domain features attention in power quality disturbance identification
Python Power Quality Disturbance Signal Classification (VI) - Super-strong Machine Learning Recognition Model Based on Disturbance Signal Feature Extraction
END  
2. Friends who enjoy this can click to follow, give the article a "watch" and share it on social media or in discussion groups.
Modeling Pioneer

## Images

![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](01.png)
![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](02.png)
![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](03.png)
![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](04.png)
![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](05.png)
![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](06.png)
![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](07.png)
![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](08.png)
![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](09.png)
![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](10.png)
![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](11.png)
![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](12.png)
![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](13.png)
![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](14.png)
![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](15.png)
![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](16.png)
![Cross Attention FFT + CNN - BiLSTM-CrossAttention Power Quality Disturbance Identification Model](17.png)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
