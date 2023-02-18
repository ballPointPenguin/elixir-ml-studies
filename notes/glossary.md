---
title: glossary
created: 2023-02-17T17:32:30.976Z
modified: 2023-02-17T17:32:30.976Z
---

## Glossary

**Scalar**: A scalar is a single value, as opposed to a vector or a matrix. It can be a real or complex number and it doesn't have any direction or magnitude.

**Tensor:** a multi-dimensional array of numerical values used in machine learning and data algorithms.

**Vector**: an element of a vector space that has magnitude (or length) and direction. In mathematics, vectors are often represented by an array of numbers.
Vectors are typically denoted by boldface letters, such as $\mathbf{v}$ or $\mathbf{u}$.

**Scalar multiplication**: multiplying each component of a vector by a scalar.

**Logits:** the output of a neural network before the application of the final activation function, typically a sigmoid for binary classification or softmax for multi-class classification.

**Epoch:** a single pass through the entire training dataset during the training process. The number of epochs is a hyperparameter that determines the number of training iterations and it should be chosen carefully to balance the model's performance and generalization.

**Softmax function**: a mathematical function that is commonly used in machine learning as the activation function in the final layer of a neural network when the network is used for multi-class classification. This function is used to convert the raw output of a neural network into a set of probabilities that can be interpreted as the network's confidence in the different classes.

The softmax function is defined as:

$softmax(x_i) = \frac{e^{x_i}}{\sum_{j=1}^{K} e^{x_j}}$

Where x is a vector of real numbers, and K is the number of classes. The output of the softmax function is a vector of values between 0 and 1 that add up to 1, representing a probability distribution over the classes.

**ONNX:** The Open Neural Network Exchange
An open format representing machine learning models. This allows developers to transfer models between platforms/frameworks.

**Edge computing:** data is processed at the edge of the network, on devices such as sensors, smartphones, or other edge devices, rather than being sent to a centralized data center for processing. This enables real-time data processing and reduces the amount of data that needs to be transmitted over the network, which can be especially beneficial in situations where bandwidth is limited or where the cost of sending data to a centralized location is prohibitive.

**Short Time Fourier Transform (SFTF):** works by dividing a continuous signal into overlapping segments, or windows, and then applying the Fourier Transform to each window to obtain the frequency spectrum of that segment. The resulting time-frequency representation, also known as a spectrogram, provides information about the evolution of the frequency content of the signal over time. The choice of window size and overlap affects the time and frequency resolution of the resulting spectrogram. STFT is commonly used in areas such as speech processing, audio signal processing, and vibration analysis.

**Faiss (Facebook AI Similarity Search):** is an open-source library developed by Facebook AI Research (FAIR) for efficient similarity search and clustering of high-dimensional data such as images and videos. It was designed to support large-scale information retrieval use cases with billions of high-dimensional data points.

**Juptyer Notebooks:** environments for collaborating, prototyping and exploring with a mix of code, narrative text, and visualizations. Python is the main language, but Julia, R, and others are supported. It is based on the IPython kernel and can run any valid python.

**Google Colab (Co-Laboratory):** is a cloud platform for writing and sharing Jupyter notebooks.
Access to GPUs and TPUs in Google Cloud are available. Syncs with Google Drive, Google Sheets, and Google Big Query.
