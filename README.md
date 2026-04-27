# Laboratory-Work-4-Activity-Improving-CNN-Performance-Using-Regularization

https://colab.research.google.com/drive/1FO4Yp-2LPVYRCsfuuk2TS9pg71ladzKM?usp=sharing

GUIDE QUESTIONS (Student Explanation & Reflection)

#A. Model Evaluation Analysis
1. What were the weakest-performing classes based on the confusion matrix? Based on the classification reports and confusion matrices, almost all classes exhibited extremely poor performance (0.00 for precision, recall, and F1-score) in both models. The model struggled to correctly identify or differentiate most classes.
2. How did Precision, Recall, and F1-score vary across classes? These metrics were 0.00 for the majority of classes. In some cases, a single class might show high recall (e.g., classp bruguiera cylindrica initially, classt heritiera littoralis in the improved model) but with very low precision, indicating the model often misclassified other samples as that specific class.
3. What does a low recall indicate in your model?A low recall means the model is failing to identify a significant proportion of the actual positive instances for that class, resulting in many false negatives.
4. How does AUC score reflect model performance compared to accuracy? Accuracy measures overall correct predictions but can be misleading with imbalanced data. AUC (Area Under the Curve) evaluates the model's ability to distinguish between classes across various thresholds and is generally more robust. Both accuracy (0.01 initial, 0.06 improved) and AUC scores (0.538 initial, 0.613 improved) were low, consistently indicating poor model performance.
   
#B. Model Improvement

5. How did data augmentation affect validation accuracy?Contributed to a slight increase in validation accuracy (from 0.01 to 0.06), but overall performance remained very low.
6. Why is Batch Normalization important in CNNs? Stabilizes network training, allowing for higher learning rates and providing a regularization effect by reducing internal covariate shift.
7. What role did Dropout play in improving your model?Acted as a regularization technique by randomly deactivating neurons, preventing the model from overfitting to the training data and improving generalization.
8. How did Early Stopping prevent overfitting? Prevented overfitting by monitoring validation loss and stopping training when performance stopped improving, restoring the best model weights.

#C. Performance Comparison

9. What improvements were observed after modifying the model?Slight increases in validation accuracy (0.01 to 0.06) and overall AUC score (0.538 to 0.614). However, weighted average Precision, Recall, and F1-score remained very low.
10. Which enhancement contributed the most to performance improvement? Why? Likely the combination of the Improved CNN Architecture and Data Augmentation, which boost model capacity and data variety. Regularization techniques (Dropout, Early Stopping) were crucial for preventing overfitting within this enhanced structure.
11. Did the gap between training and validation accuracy decrease? Explain. No, the gap between training and validation accuracy did not decrease; it remained large. Training accuracy increased, while validation accuracy stayed low and stagnant, indicating severe overfitting despite enhancements.

#D.Explainability (Grad-CAM Integration)

12. How did Grad-CAM help in understanding model predictions?It helps understand model predictions by showing a heatmap on the input image, highlighting regions most influential in the model's decision.
13. Did the improved model focus on more relevant regions? Provide evidence.  Cannot confirm if the improved model focused on more relevant regions as Grad-CAM was only run on the initial model in the notebook. A new Grad-CAM run on the improved model would be needed for evidence.
14. Why is explainability important in real-world AI applications? Crucial for building trust, debugging models, detecting biases, meeting regulatory compliance, and gaining new scientific insights in real-world AI applications.
