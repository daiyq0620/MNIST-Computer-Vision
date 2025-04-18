# MNIST-Computer-Vision
## **Introduction**

Computer vision began as a research field aimed at enabling machines to interpret visual data. Today, it is widely used in industries such as healthcare, finance, security, and automation. Applications like medical image analysis, facial recognition, autonomous vehicles, and industrial quality control have greatly improved efficiency, reduced human effort, and minimized errors. As a result, computer vision has become a key technology driving automation and intelligent systems.

One important application of computer vision is handwritten digit recognition, which helps automate document processing. This technology is used in postal sorting systems to automatically categorize mail based on handwritten addresses. In banking, it speeds up check verification by recognizing handwritten numbers, ensuring fast and accurate transactions. It also plays a vital role in assistive technologies, converting handwritten text into speech or Braille to improve accessibility for visually impaired individuals.

In this project, we aim to classify handwritten digits using various machine learning models, including k-Nearest Neighbors (kNN), Decision Trees, Support Vector Machines (SVM), and Convolutional Neural Networks (CNN). The dataset used for this task is a collection of images represented as numerical pixel values in CSV format. The goal is to analyze and compare the performance of different classifiers in recognizing handwritten digits accurately. 

This report presents an analysis of exploratory data analysis (EDA), the implementation of various models, and a comparative evaluation of their performance. For each model, we provide a detailed technical explanation, including the rationale for selection, underlying algorithms, implementation details, and performance results. Following this, we conduct a comparative analysis across all models and discuss the practical significance of applying these techniques in real-world business contexts.

## **Conclusion**

Our project focuses on classifying handwritten digits using the MNIST dataset, a well-established benchmark in computer vision. We evaluated four models, including kNN, Decision Trees, SVM with two different kernels, and a CNN, based on their accuracy, computational cost, and interpretability.

For **accuracy** comparison, we examined each model’s training accuracy and cross-validation accuracy. For CNN, we used validation accuracy instead of cross-validation due to its higher computational requirements. Decision Trees showed clear signs of overfitting, with a 14% gap between training accuracy (100%) and cross-validation accuracy (85.55%). This indicates the model memorized the training data but failed to generalize to unseen examples. In contrast, the other models demonstrated strong generalization, with both training and validation accuracies consistently falling between 97% and 99%. CNN achieved the highest validation accuracy of 99.17%, with a training accuracy of 99.11%, indicating excellent performance with minimal overfitting.

From a **computational** perspective, kNN was the most expensive to evaluate due to repeated distance calculations across multiple *k* values. SVMs, particularly with non-linear kernels, also incurred moderate computational costs. While CNNs are generally resource-intensive, our model reached over 99% accuracy in just 10 epochs, making the computational cost acceptable given the performance gain.

In terms of **interpretability**, CNNs are the least transparent, as their deep, non-linear architectures make it difficult to trace how specific predictions are made. In contrast, kNN is simple and intuitive, with decisions based on the closest training samples. However, its performance deteriorates on high-dimensional data, where all pixels are treated equally regardless of their relevance. Decision Trees are fully transparent and easy to interpret, but they evaluate pixels independently and fail to capture spatial relationships, which leads to overfitting. SVMs offer moderate interpretability, especially with linear kernels, but require effective feature extraction when dealing with raw pixel data to maintain performance.

Given the nature of our task and the requirements of the application context, we prioritize accuracy and computational efficiency over interpretability. In domains such as credit scoring, interpretability is essential. Financial institutions must clearly explain decisions such as loan denials or credit limits to users and regulators. In these situations, transparent models like Decision Trees or linear classifiers are more appropriate. In contrast, handwritten digit recognition is typically used in applications such as postal code scanning, form digitization, and automated grading systems, where individual prediction explanations are not required. In these scenarios, achieving fast and highly accurate classification is the primary objective. 

In conclusion, considering the accuracy, efficiency, and practical demands of our task, CNNs are the most suitable and recommended model for handwritten digit classification.

## About

A collaborative effort by Pathomporn, Yiting, Luna, Xinya 

