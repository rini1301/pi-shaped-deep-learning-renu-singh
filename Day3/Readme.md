# Day 3 Exercise: Convolutional Neural Networks (CNN) with Fashion-MNIST

## Core Concept Questions – CNNs

### 1. What advantages do CNNs have over traditional fully connected neural networks for image data?
- Exploit **spatial structure** of images using local connections.  
- Reduce the number of parameters through **weight sharing**, making training more efficient.  
- Automatically **learn hierarchical features** (edges → shapes → objects), unlike fully connected networks that treat each pixel independently.  

### 2. What is the role of convolutional filters/kernels in a CNN?
- Filters slide over the image to detect **patterns or features** (like edges, textures, or shapes).  
- Each filter produces a **feature map** highlighting the presence of that feature in the image.  

### 3. Why do we use pooling layers, and what is the difference between MaxPooling and AveragePooling?
- Pooling **reduces spatial dimensions** of feature maps, lowering computation and making the model more robust to small translations.  
- **MaxPooling:** keeps the maximum value in a region → highlights strong features.  
- **AveragePooling:** takes the average value → smooths features, less sensitive to noise.  

### 4. Why is normalization of image pixels important before training?
- Pixel values are scaled to a standard range (usually `[0,1]` or `[-1,1]`).  
- Normalization improves **training stability**, speeds up convergence, and prevents gradients from exploding or vanishing.  

### 5. How does the softmax activation function work in multi-class classification?
- Converts raw outputs (logits) into **probabilities** that sum to 1.  
- The class with the **highest probability** is chosen as the predicted label.  

### 6. What strategies can help prevent overfitting in CNNs?
- **Dropout:** randomly deactivate neurons during training.  
- **Data augmentation:** generate more diverse training images (rotations, flips, shifts).  
- **Early stopping:** stop training when validation loss stops improving.  
- **Regularization:** e.g., L2 weight penalties to constrain model complexity.  

### 7. What does the confusion matrix tell you about model performance?
- Shows **true vs. predicted labels** for all classes.  
- Helps identify which classes are often confused with each other.  

### 8. If you wanted to improve the CNN, what architectural or data changes would you try?
- **Add more convolutional layers** to learn complex features.  
- **Increase filter size or number** for richer feature maps.  
- **Use batch normalization** for faster, stable training.  
- **Increase dataset size** or use **data augmentation** to improve generalization.  
- Experiment with **different optimizers and learning rates**.
