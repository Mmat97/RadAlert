# 📚 RadAlert Glossary

This glossary defines technical terms, keywords, and acronyms used in the RadAlert project that may be unfamiliar to those without specialized knowledge in machine learning, medical imaging, or computer science.

---

## Table of Contents

- [A](#a) - [B](#b) - [C](#c) - [D](#d) - [E](#e) - [F](#f) - [G](#g) - [H](#h) - [I](#i) - [L](#l) - [M](#m) - [N](#n) - [P](#p) - [R](#r) - [S](#s) - [T](#t) - [V](#v)

---

## A

**Accuracy**  
A metric that measures the proportion of correct predictions (both true positives and true negatives) out of all predictions made by the model.

**Adam Optimizer**  
An adaptive learning rate optimization algorithm commonly used in deep learning. It combines the advantages of two other optimization methods (AdaGrad and RMSProp) to efficiently update model parameters during training.

**Area Under Curve (AUC)**  
See **ROC-AUC**.

---

## B

**Backpropagation**  
The algorithm used to train neural networks by computing gradients of the loss function with respect to each parameter, allowing the model to learn from its mistakes.

**Batch Size**  
The number of training samples processed together in one forward and backward pass before updating the model weights. A larger batch size can be more stable but requires more memory.

**BatchNorm1d (Batch Normalization)**  
A technique that normalizes the inputs to each layer by adjusting and scaling activations. This helps stabilize training, allows for higher learning rates, and can improve model performance.

**BCE (Binary Cross-Entropy Loss)**  
A loss function used for binary classification tasks (e.g., predicting malignancy: yes/no). It measures how far the predicted probabilities are from the true binary labels.

**Benign**  
In medical terminology, a non-cancerous abnormality or lesion that does not spread to other parts of the body.

**Bilinear Interpolation**  
A method for resizing images by estimating pixel values using weighted averages of the four nearest pixels, producing smoother results than nearest-neighbor interpolation.

---

## C

**CNN (Convolutional Neural Network)**  
A type of deep learning architecture designed to process grid-like data (such as images). CNNs use convolutional layers to automatically learn spatial features and patterns.

**Conv2d (2D Convolutional Layer)**  
A PyTorch layer that performs 2D convolution operations on image data. It applies learnable filters (kernels) to extract spatial features from images, such as edges, textures, and patterns.

**Context-Aware**  
A system that considers surrounding information or patient history when making predictions, rather than analyzing data in isolation.

**Cross-Modality Reasoning**  
The ability of a model to combine and reason across different types of data (e.g., medical images and clinical records) to make more informed predictions.

**CUDA**  
NVIDIA's parallel computing platform and programming model that enables GPUs to accelerate deep learning computations. Used when training models on NVIDIA graphics cards.

---

## D

**DataLoader**  
A PyTorch utility class that provides an iterable over a dataset. It handles batching, shuffling, and parallel data loading, making it efficient to feed data to neural networks during training.

**DCE-MRI (Dynamic Contrast-Enhanced MRI)**  
A specialized MRI technique where a contrast agent is injected into the patient, and multiple images are taken over time to observe how tissues absorb and release the contrast. This helps identify abnormal blood flow patterns associated with tumors.

**Deep Learning**  
A subset of machine learning that uses neural networks with multiple layers (hence "deep") to automatically learn complex patterns and representations from data.

**DICOM (Digital Imaging and Communications in Medicine)**  
The international standard format for storing, transmitting, and managing medical imaging data. All medical images (MRI, CT, X-ray, etc.) are typically stored in DICOM format.

**Dual-Branch Architecture**  
A neural network design with two separate processing pathways (branches) that handle different types of input data independently before combining their outputs.

**Dropout**  
A regularization technique that randomly "turns off" (sets to zero) a percentage of neurons during training to prevent overfitting and improve generalization.

---

## E

**Early Fusion**  
A fusion strategy where different data modalities are combined at the input level before being processed by the network.

**EHR (Electronic Health Records)**  
Digital versions of patients' paper charts that contain medical history, diagnoses, medications, treatment plans, and other clinical information. In RadAlert, EHR data includes clinical metadata such as tumor size, demographics, and patient history.

**Embedding**  
A lower-dimensional vector representation of data that captures meaningful features. In RadAlert, embeddings are learned representations of EHR data and MRI images.

**Epoch**  
One complete pass through the entire training dataset during model training. Multiple epochs are typically needed for the model to learn effectively.

---

## F

**F1 Score**  
A metric that balances precision and recall, calculated as the harmonic mean of the two. It's particularly useful when dealing with imbalanced datasets.

**Feature Selection**  
The process of identifying and keeping the most relevant input variables (features) for model training, while removing irrelevant or redundant ones.

**Forward Pass**  
The process of passing input data through a neural network to generate predictions, moving from input layer to output layer.

**Fusion Layer**  
A neural network layer that combines outputs from multiple branches (e.g., EHR and MRI branches) to make a final prediction.

**Flatten**  
A PyTorch layer that reshapes multi-dimensional tensors into a one-dimensional vector. Commonly used to convert the output of convolutional layers into a format suitable for fully connected (linear) layers.

---

## G

**Gradient**  
The derivative of the loss function with respect to model parameters. Gradients indicate the direction and magnitude needed to adjust parameters to reduce error.

---

## H

**Hyperparameter**  
A configuration setting that is set before training begins and is not learned from the data. Examples include learning rate, batch size, number of layers, and dropout rate. These must be tuned manually or through automated search methods.

---

## I

**Inference**  
The process of using a trained model to make predictions on new, unseen data (as opposed to training, where the model learns from labeled data).

**Interpolation**  
A method for resizing or transforming images by estimating pixel values at new positions based on existing pixel values.

---

## L

**Late Fusion**  
A fusion strategy where different data modalities are processed separately through independent branches, and their outputs are combined at a later stage (near the output layer).

**Learning Rate (lr)**  
A hyperparameter that controls how much the model parameters are adjusted during each training step. Too high can cause instability; too low can slow convergence.

**Lesion**  
An area of abnormal tissue, which can be benign or malignant. In breast imaging, lesions are the areas of interest that may indicate cancer.

**Linear Layer**  
A fully connected neural network layer in PyTorch (also called a dense layer) where every input is connected to every output. It performs a linear transformation: output = input × weight + bias.

**Loss Function**  
A mathematical function that measures how far the model's predictions are from the true values. The goal of training is to minimize this loss.

---

## M

**Malignancy**  
The presence of cancerous cells that have the potential to invade surrounding tissues and spread to other parts of the body.

**MaxPool2d (2D Max Pooling)**  
A PyTorch layer that reduces the spatial dimensions of feature maps by taking the maximum value over a small window (typically 2×2). This helps reduce computational complexity and makes the model more robust to small translations.

**MPS (Metal Performance Shaders)**  
Apple's framework for GPU-accelerated computing on Apple Silicon (M1, M2, etc.) chips. PyTorch can use MPS to accelerate training on Mac computers.

**MRI (Magnetic Resonance Imaging)**  
A medical imaging technique that uses strong magnetic fields and radio waves to generate detailed images of the body's internal structures. In RadAlert, MRI scans are used to visualize breast tissue and detect potential tumors.

**Morphology**  
The study of the form and structure of objects. In medical imaging, it refers to the shape, size, and appearance characteristics of tumors or lesions.

**Multimodal**  
A system that processes and integrates multiple types of data (modalities), such as images, text, and numerical data, to make predictions.

---

## N

**Neural Network**  
A computing system inspired by biological neural networks, consisting of interconnected nodes (neurons) organized in layers that process information.

**Normalization**  
The process of scaling data to a standard range (often 0-1 or mean=0, std=1) to ensure all features contribute equally to the model and improve training stability.

---

## P

**Pixel Array**  
The raw numerical data representing an image, where each number corresponds to the intensity value of a pixel at a specific location. In DICOM files, this is accessed via the `pixel_array` attribute.

**pydicom**  
A Python library for reading, modifying, and writing DICOM medical imaging files. It allows access to both the image pixel data and the metadata (patient information, imaging parameters, etc.) stored in DICOM files.

**PyTorch**  
An open-source machine learning framework developed by Facebook (Meta) that provides tools for building and training neural networks, particularly popular in research.

---

## R

**RadAlert**  
The name of this project: a multimodal deep learning system for breast cancer detection that fuses MRI imaging and EHR data.

**ReLU (Rectified Linear Unit)**  
A common activation function in neural networks that outputs the input if it's positive, otherwise outputs zero. It introduces non-linearity, allowing networks to learn complex patterns.

**ROC-AUC (Receiver Operating Characteristic - Area Under Curve)**  
A metric that measures the model's ability to distinguish between classes. An AUC of 1.0 is perfect, 0.5 is random. It's particularly useful for binary classification problems.

---

## S

**Sequential**  
A PyTorch container that allows you to stack multiple layers in sequence. It simplifies the creation of neural networks by automatically connecting layers in the order they are defined.

**Sigmoid**  
An activation function that maps any real number to a value between 0 and 1, commonly used in the output layer for binary classification to produce probabilities.

**SimpleCNN**  
A lightweight convolutional neural network used as a fallback model in RadAlert when the full trained model cannot be loaded.

**StandardScaler**  
A preprocessing technique from scikit-learn that standardizes features by removing the mean and scaling to unit variance, ensuring all features have similar scales. This helps neural networks train more effectively.

**State Dict (State Dictionary)**  
A Python dictionary that contains the learned parameters (weights and biases) of a PyTorch model, allowing the model to be saved and loaded without the full model architecture.

**Stratify**  
A parameter in train/test splitting that ensures the proportion of different classes (e.g., malignant vs. benign) remains the same in both training and testing sets. This prevents class imbalance issues.

---

## T

**tarfile**  
A Python standard library module for reading and writing tar archive files. In RadAlert, it's used to extract DICOM files from compressed tar archives containing the MRI dataset.

**TCIA (The Cancer Imaging Archive)**  
A public repository of medical images of cancer, providing researchers with access to large datasets for developing and testing AI models.

**Tensor**  
A multi-dimensional array used in deep learning frameworks like PyTorch. Scalars are 0D tensors, vectors are 1D, matrices are 2D, and images are typically 3D or 4D tensors.

**Train/Test Split**  
The practice of dividing a dataset into separate portions: one for training the model and another for evaluating its performance on unseen data. This is typically done using scikit-learn's `train_test_split` function.

---

## V

**Visual Embedding**  
A learned vector representation that captures the visual features and patterns extracted from medical images (MRI scans in this case).

---

## Additional Notes

- **Device**: Refers to the computing hardware used (CPU, GPU/CUDA, or Apple Silicon/MPS). PyTorch automatically selects the best available device for computation.
- **Inference Mode**: A PyTorch optimization mode (`torch.inference_mode()`) that disables gradient computation for faster predictions during model evaluation.
- **Patient ID**: A unique identifier used to link EHR data with corresponding MRI images, enabling the fusion of clinical and imaging data.
- **torch.nn**: PyTorch's neural network module that provides building blocks for creating neural networks, including layers, activation functions, and loss functions.

---

*This glossary is designed to help readers understand technical terminology used througit remote set-url origin git@github.com:MoCoMakers/RadAlert.git
ghout the RadAlert project documentation and codebase. Large parts of this glossary were created with AI so be aware errors and hallucinations are possible.*

