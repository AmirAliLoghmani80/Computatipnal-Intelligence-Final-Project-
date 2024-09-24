# Computational Intelligence Final Project: EEG Signal Classification

This project was completed as part of the Computational Intelligence course. The goal of the project is to classify EEG signals recorded during the viewing of videos that elicited either positive or negative emotions. The signals were recorded using a 59-channel EEG system, and the objective is to design a neural network to classify the signals into two classes: *Positive Emotions* and *Negative Emotions*.

## Project Overview

The project focuses on feature extraction, feature selection, classification, and evaluation of EEG signals. The following steps were involved:

1. **EEG Signal Preprocessing**: The data consists of EEG signals recorded from 59 channels at a sampling rate of 1000 Hz. The signals were recorded from 10 individuals who were presented with emotion-eliciting videos.

2. **Feature Extraction**: Various features were extracted from the EEG signals, including:
   - **Statistical Features**: Simple to compute and provide useful information from the shape of the signal.
   - **Frequency Domain Features**: Extracted from each channel's signal for more detailed analysis.

3. **Feature Selection**: 
   - **Fisher's Criterion**: Used to select the most effective features by maximizing the separation between classes.
   - **Dimensionality Reduction**: Applied to identify and select features that improve classification accuracy.

4. **Classification**:
   - A **Multilayer Perceptron (MLP)** neural network was designed and trained using the extracted features.
   - **k-Fold Cross-Validation** was employed to evaluate the performance of the classifier.
   - The network was tuned by varying the number of layers, neurons per layer, and activation functions.

5. **Phase 1 - Feature Selection and MLP Design**:
   - Several feature sets were tested using MLP, and the classification accuracy was computed using 5-fold cross-validation.
   - The best MLP architecture was determined by iterating over different configurations.

6. **Phase 2 - Evolutionary Algorithms for Feature Selection**:
   - Evolutionary and swarm intelligence algorithms were applied for feature selection to improve classification performance.
   - The selected features were used to train and evaluate both MLP and **Radial Basis Function (RBF)** networks.

## Data Description

- **Training Data**: 550 trials, each associated with either positive or negative emotions (1 for positive, -1 for negative).
- **Test Data**: 159 trials were used for evaluation, with the goal of predicting their corresponding labels.

## Implementation

1. **Preprocessing**: The raw EEG signals were normalized, and features were extracted for each channel.
2. **Feature Selection**: Fisher's criterion and matrix-based selection methods were used to choose the most relevant features.
3. **Classification**:
   - Two classifiers were implemented:
     - **MLP Neural Network**
     - **RBF Neural Network**
   - Performance was evaluated using cross-validation.
4. **Evolutionary Feature Selection**: Swarm intelligence and evolutionary algorithms were applied to refine feature selection, further enhancing classifier accuracy.

## Results

- The **MLP** and **RBF** classifiers were trained using the selected features, and their performance was compared.
- The accuracy of each model was evaluated using the test data, and the final classification labels were determined.

## Deliverables

- **Code**: All MATLAB scripts are provided for feature extraction, feature selection, and classification.
- **Data**: The training and test data are included.
- **Report**: A detailed report summarizing the methods, results, and conclusions.
  
