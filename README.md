Colab: https://colab.research.google.com/drive/14X8VorpFqq39nbBnPEQO5gu7mb3YjbVJ?usp=sharing

Drive: https://drive.google.com/drive/folders/1-TxAXpFBgLboG6Zu8aahFlRKvp7PWzjE?usp=sharing

Guide Questions (Student Reflection & Explanation)
Students must answer the following:
1. Dataset Preparation
○ How did you organize your dataset in Google Drive?
Answer: Images were organized in MyDrive/ImageDataset/ with subfolders named after each plant species class containing their respective image files for easy access and management. Folder structure is crucial because TensorFlow's image_dataset_from_directory() function automatically interprets directory names as class labels, eliminating manual labeling and streamlining the data loading process significantly.

○ Why is folder structure important for TensorFlow image loading?
Answer: Folder structure is crucial because TensorFlow's image_dataset_from_directory() function automatically interprets directory names as class labels, eliminating manual labeling and streamlining the data loading process significantly.
3. Model Training
○ What is the role of convolutional layers in image classification?
Answer: Convolutional layers serve as feature extractors that detect hierarchical visual patterns ranging from simple edges and textures in early layers to complex structures like leaves and stems in deeper layers.
○ Why do we split data into training and validation sets?
Answer: Data is split into training and validation sets to enable proper evaluation of model generalization capabilities and to detect overfitting early during the training process.

4. Performance Analysis
○ What accuracy did your model achieve?
Answer: My model achieved 49.9% validation accuracy, which is only slightly better than random guessing for 20 classes (5%), indicating significant underfitting and poor generalization to unseen plant species data.
○ How did the number of images affect the model’s performance?
Answer: The limited number of images per class, combined with high visual similarity between plant species, severely restricted the model's ability to learn discriminative features and distinguish between categories effectively.

6. Critical Thinking
○ What challenges did you encounter while using your own dataset?
Answer: The extremely low accuracy suggests challenges including insufficient dataset diversity, poor image quality across samples, confusingly similar plant appearances, and potentially inadequate model complexity for this difficult 20-class classification problem.

○ How can data augmentation improve your model?
Answer: Data augmentation would improve my model by artificially expanding the limited training data, introducing rotational and scaling variations that force the model to learn more robust, generalizable features rather than memorizing specific examples.

8. Application
○ Suggest a real-world application for your trained model.
Answer: Real-world applications include automated agricultural disease detection systems for farmers, biodiversity monitoring tools for ecological research, and user-friendly plant identification applications designed for home gardeners and nature enthusiasts.

○ How can this system be integrated into a mobile or web application?
Answer: The system can be integrated into mobile applications using TensorFlow Lite for efficient on-device inference or deployed as scalable web APIs using TensorFlow Serving for cloud-based classification services.

Guide Questions (Student Explanation & Reflection)
Students must answer:
Visualization & Overfitting
1. What signs indicated overfitting in your first model?
   Answer: Overfitting signs included training accuracy increasing while validation accuracy plateaued or decreased, and validation loss rising while training loss fell.
3. How did data augmentation affect validation accuracy?
Answer: Data augmentation improved validation accuracy by reducing the generalization gap and stabilizing validation metrics.

Model Improvement
3. What is the purpose of dropout layers?
Answer: Dropout layers randomly deactivate neurons during training to prevent co-adaptation and reduce overfitting.

4. Why does data augmentation improve generalization?
Answer: Data augmentation improves generalization by exposing the model to diverse transformations and teaching prediction invariance.

Performance Comparison
5. Compare accuracy before and after improvements.
Answer: The improved model shows lower training accuracy but higher validation accuracy with a reduced generalization gap from ~25% to ~5-10%.

6. Which technique contributed most to improvement?
   Answer: Data augmentation contributed most to improvement by diversifying training data, while dropout stabilized the results.

Deployment & Application
7. Why is saving the model important?
Answer: Saving the model preserves trained weights for deployment, enables reproducibility, and avoids costly retraining.

8. How can this model be deployed in a real-world system?
Answer: The model can be deployed via TensorFlow Lite for mobile devices, TensorFlow Serving for cloud APIs, or converted to TensorFlow.js for browser applications.
