## 💡 Core Concept Questions & Answers

### 1. What is the role of feature scaling/normalization in training neural networks?  
It ensures all input features are on a similar scale, preventing some features from dominating others and speeding up convergence.

### 2. Why do we split data into training and testing sets?  
To evaluate the model on unseen data, ensuring that performance reflects real-world generalization.

### 3. What is the purpose of activation functions like ReLU or Sigmoid?  
They introduce **non-linearity**:
- **ReLU**: Efficient and avoids vanishing gradients.  
- **Sigmoid**: Maps output between 0 and 1, useful for probabilities in binary classification.

### 4. Why is binary cross-entropy commonly used as a loss function for classification?  
It measures the difference between predicted probabilities and actual labels, penalizing wrong confident predictions more heavily.

### 5. How does the optimizer (e.g., Adam) affect training compared to plain gradient descent?  
Adam adapts learning rates for each parameter, leading to faster and more stable training compared to plain gradient descent.

### 6. What does the confusion matrix tell you beyond just accuracy?  
It shows **true positives, false positives, true negatives, and false negatives**, helping to understand the types of errors the model makes.

### 7. How can increasing the number of hidden layers or neurons impact model performance?  
It allows the model to learn more complex patterns, but may cause overfitting or increase computation time if overdone.

### 8. What are some signs that your model is overfitting the training data?  
- High training accuracy but low test accuracy.  
- Training loss keeps decreasing while validation loss increases.

### 9. Why do we evaluate using precision, recall, and F1-score instead of accuracy alone?  
Accuracy can be misleading on imbalanced datasets. Precision, recall, and F1-score provide a more detailed view of model performance.

### 10. How would you improve the model if it performs poorly on the test set?  
- Collect more data  
- Apply regularization (dropout, L2)  
- Tune hyperparameters  
- Try deeper/wider architectures  
- Use data augmentation or balancing techniques  

---
