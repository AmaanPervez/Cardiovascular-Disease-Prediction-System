# ❤️ Detection of Cardiovascular Diseases from ECG Images

## 📌 Project Overview

I developed this project to automate the detection of cardiovascular diseases using Electrocardiogram (ECG) images by combining **Image Processing, Signal Processing, and Machine Learning** techniques.

An ECG is one of the most widely used diagnostic tools for monitoring the electrical activity of the heart. However, a large number of ECG records are still available in paper format. Manually analyzing these ECG records is time-consuming and requires medical expertise.

To address this challenge, I built a machine learning-based application that converts ECG images into one-dimensional signals, extracts important cardiac waveforms, and classifies the ECG into different cardiovascular health categories.

The application provides an interactive web interface where users can upload ECG images, visualize the processing workflow, and receive classification results.

---

## 🎯 Problem Statement

Cardiovascular diseases are among the leading causes of mortality worldwide. Early detection and diagnosis play an important role in preventing serious cardiac complications.

Traditional ECG analysis involves manually examining ECG waveforms to identify abnormalities in the heart's electrical activity. This process presents several challenges:

- Manual ECG interpretation can be time-consuming.
- Analyzing paper-based ECG records requires specialized medical knowledge.
- Digitizing ECG records for automated analysis is challenging.
- ECG images contain grid lines, noise, and other visual artifacts that make signal extraction difficult.
- Identifying important ECG components such as P waves, QRS complexes, and T waves requires accurate image processing.
- Processing large numbers of ECG records manually is not scalable.

### Proposed Solution

To overcome these challenges, I developed an automated ECG analysis system that:

1. Accepts ECG images as input from users.
2. Preprocesses ECG images to remove noise and unwanted grid lines.
3. Extracts ECG waveforms using image processing techniques.
4. Converts the extracted waveforms into one-dimensional ECG signals.
5. Normalizes the extracted signals.
6. Uses a pre-trained machine learning model to classify the ECG.
7. Displays the predicted cardiovascular condition through a web application.

---

## 🎯 Project Objectives

The primary objectives of this project are:

- To develop an automated system for cardiovascular disease detection using ECG images.
- To convert paper-based ECG images into digital one-dimensional signals.
- To perform image preprocessing and noise reduction.
- To extract important ECG components, including P waves, QRS complexes, and T waves.
- To apply machine learning techniques for ECG classification.
- To classify ECG images into multiple cardiovascular health categories.
- To develop an interactive web application for real-time ECG image analysis.
- To make ECG analysis more accessible through automation.

---

## 🧠 Proposed Methodology

The project follows a complete image-to-signal-to-classification pipeline.

### 1. ECG Image Acquisition

The process begins when a user uploads an ECG image through the web application.

The dataset contains ECG images belonging to healthy individuals and individuals with different cardiovascular conditions.

### 2. Image Preprocessing

The uploaded ECG image undergoes several preprocessing operations to improve signal extraction.

The following techniques are applied:

- **RGB to Grayscale Conversion:** Converts the input image into grayscale to simplify further processing.
- **Gaussian Filtering:** Reduces image noise and smoothens unwanted variations.
- **Image Resizing:** Resizes images into a consistent dimension required for processing.
- **Thresholding:** Separates ECG waveforms from the background and grid lines.
- **Noise Removal:** Removes unwanted visual elements that may affect waveform extraction.

### 3. ECG Signal Extraction

One of the most challenging parts of this project is extracting the actual ECG waveform from the image.

I implemented contour-based image processing techniques to identify and extract the ECG signal while minimizing the influence of background grid lines.

The extracted waveform is converted into a one-dimensional numerical signal.

### 4. ECG Waveform Identification

The extracted ECG signal contains several important components that represent the electrical activity of the heart.

The major components considered in this project are:

- **P Wave:** Represents atrial depolarization.
- **QRS Complex:** Represents ventricular depolarization.
- **T Wave:** Represents ventricular repolarization.

These waveform components provide important information about cardiac electrical activity.

### 5. Signal Normalization

After extracting the one-dimensional ECG signal, normalization is performed to maintain consistency in the input data.

This helps prepare the extracted signal for the machine learning classification stage.

### 6. Machine Learning Classification

The normalized ECG signal is passed to a pre-trained machine learning model.

The model analyzes the extracted signal and predicts the corresponding ECG category.

The classification system supports four categories:

| Class | Description |
|---|---|
| Normal | ECG signals classified as normal |
| Myocardial Infarction | ECG signals associated with myocardial infarction |
| Abnormal Heartbeat | ECG signals showing abnormal heartbeat patterns |
| History of Myocardial Infarction | ECG signals associated with a previous myocardial infarction |

### 7. Result Visualization

Once classification is complete, the predicted result is displayed to the user through the web application.

The application also allows users to observe the different stages of the ECG image processing workflow.

---

## 🔄 System Workflow

The complete workflow of the project is as follows:

```text
       ECG Image Upload
               |
               v
       Image Preprocessing
               |
               v
       RGB to Grayscale
               |
               v
        Gaussian Filtering
               |
               v
         Image Resizing
               |
               v
           Thresholding
               |
               v
       ECG Signal Extraction
               |
               v
       Contour-Based Processing
               |
               v
       1-D Signal Conversion
               |
               v
        Signal Normalization
               |
               v
       Pre-trained ML Model
               |
               v
       ECG Classification
               |
               v
         Result Display
