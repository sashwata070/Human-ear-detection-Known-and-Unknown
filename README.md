# It presents a deep learning-based framework for robust 2D ear recognition, designed to address the challenges of open
set biometric identification. Traditional 2D ear recognition methods often suffer from variations in pose, lighting, and occlusion.
 To overcome these limitations, we leverage 3D depth information and employ a Soft-Max, Open-Max architecture that integrates
 EfficientNet-B0 as a pretrained feature extractor. Image paths and labels for both known and unknown classes are loaded
 and split into training, validation, and unknown sets. Custom datasets and data loaders are created using Albumentations for data
 augmentation. Here we are using Cross Entropy Loss for classification. . Known class accuracy was found to be 100% as found
 from Classification Report and Confusion Matrix. After this we used Soft-Max confidence method and unknown detection rate was
 found to be 54.17% which is very low. Now we apply Open-Max method where the unknown detection rate was found to be 92%
 demonstrating significant robustness in real-world biometric scenarios.
 After this we utilize a TripletNet architecture incorporating EfficientNet-B0 as the feature extractor. The model learns
 512-dimensional embeddings optimized via triplet loss, enhancing intra-class compactness and inter-class separability. Evaluation
 is performed on a curated dataset of 2600 2D ear images across 13 identities, where known class classification using KNN, SVM,
 and Logistic Regression achieves 96–97% accuracy. For open-set recognition, we employ multiple unknown detection strategies,
 including softmax confidence rejection, distance-based thresholding, One-Class SVM, and Isolation Forest. A final ensemble of these
 methods attains an unknown detection rate of 94.33%, demonstrating significant robustness in real-world biometric scenarios. These
 results validate the effectiveness of metric learning and ensemble-based rejection techniques, highlighting the potential of 2D ear
 biometrics for secure and scalable identity verification systems
