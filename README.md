<h1 align="center">🧠 Handwritten Digit Recognition using MLP Neural Network</h1>

<p align="center"><i>An Artificial Intelligence system for classifying handwritten digits using a Multi-Layer Perceptron trained with cross-validation</i></p>

---

## 📌 Project Overview

This project focuses on developing a machine learning system for recognizing handwritten digits using a Multi-Layer Perceptron (MLP) neural network. The model is trained and evaluated on the UCI Optical Recognition of Handwritten Digits dataset.

A two-fold cross-validation strategy is used to ensure that the model generalizes well across different dataset splits. The final system achieves an average accuracy of **98.51%**, demonstrating strong performance in digit classification tasks.

---

## 🎯 Objective

The main objective of this project is to design and implement an artificial neural network capable of accurately classifying handwritten digits from 0 to 9. The system is built from scratch to gain a deeper understanding of neural network training, optimization, and generalization.

---

## 📊 Dataset Description

The dataset used in this project is the UCI Optical Recognition of Handwritten Digits dataset. Each sample consists of 64 numerical features representing pixel intensity values of handwritten digit images, along with a label ranging from 0 to 9.

Before training, the dataset was normalized to improve numerical stability and ensure that all features contribute equally to the learning process. The data was also shuffled before each run to avoid bias, and a portion of the training data was reserved for validation.

---

## 🧠 Model Architecture

The model is based on a Multi-Layer Perceptron (MLP) neural network designed to learn complex relationships between input features and digit classes.

The input layer receives 64 features representing the pixel intensity values of each digit image. These features are then passed through two fully connected hidden layers. The first hidden layer contains 768 neurons and applies the ReLU activation function to introduce non-linearity and improve learning capability. The second hidden layer contains 512 neurons and also uses ReLU activation to further refine feature extraction and representation learning.

The final output layer consists of 10 neurons, each representing one digit class from 0 to 9. A softmax activation function is applied at the output layer to convert raw predictions into probability distributions, allowing the model to predict the most likely digit class.

This layered structure enables the network to progressively learn hierarchical patterns in the input data, moving from simple feature extraction to more complex decision boundaries.

---

## ⚙️ Training Strategy

The model is trained using mini-batch stochastic gradient descent, which allows efficient learning through small subsets of the dataset at each iteration. The learning rate is gradually reduced during training using exponential decay, helping the model converge more smoothly.

Label smoothing is applied to reduce overconfidence in predictions and improve generalization. Early stopping is also used to prevent overfitting by stopping training once the model reaches stable performance.

---

## 🔁 Two-Fold Cross Validation

To ensure robust evaluation, the dataset is split into two folds. In the first fold, one dataset is used for training while the other is used for testing. In the second fold, the roles are reversed. This approach ensures that the model is evaluated on different data distributions.

The final performance is calculated as the average accuracy across both folds, resulting in a reliable measure of generalization.

---

## 📈 Training Results

The training process demonstrates strong convergence behaviour across both folds of cross-validation. The model shows stable learning with high training accuracy and consistent performance across validation splits, indicating good generalization capability.

The results also highlight that the model is able to learn meaningful patterns from handwritten digit data while maintaining low overfitting due to the use of early stopping, label smoothing, and learning rate decay.

---

### 🧠 Training Performance Visualization

<div align="center">
<img src="https://i.imgur.com/QZ57gaf.png" width="85%" alt="Training Results 1"/>
<br><br>
<img src="https://i.imgur.com/bADAITj.png" width="85%" alt="Training Results 2"/>
</div>

---

## 🔍 Key Results

- Final average accuracy: **98.51%**
- Fold 1 accuracy: 98.43%
- Fold 2 accuracy: 98.58%
- Strong generalization across unseen data
- Minimal overfitting due to early stopping and regularization techniques

---

## 📌 Conclusion

This project demonstrates the effectiveness of a Multi-Layer Perceptron neural network in solving handwritten digit classification problems. Through proper preprocessing, optimization techniques, and cross-validation, the model achieves high accuracy and strong generalization ability.

The results confirm that even a relatively simple neural network architecture can perform very well when properly designed and trained.
