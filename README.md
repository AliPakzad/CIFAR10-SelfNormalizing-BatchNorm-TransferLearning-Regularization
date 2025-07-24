# CIFAR10-SelfNormalizing-BatchNorm-TransferLearning-Regularization
Investigate how architectural choices and training techniques affect the performance of image classification models.

### 📝 Project Tasks Overview

This project involves several key experiments and modifications on a deep neural network trained on the CIFAR10 dataset:

1. **Self-Normalizing Network**  
   Reuse the deep network designed in the previous phase. Without changing the number of layers or neurons, use **SELU** activation in the hidden layers and initialize the weights properly to build a **self-normalizing network**. Plot the train and validation accuracy and loss.

2. **Batch Normalization Comparison**  
   Replace the SELU activations with other activations and apply **Batch Normalization** after each layer (except the final output). Compare the results with the self-normalizing network in a combined plot.

3. **Binary Classification (Horse vs. Not Horse)**  
   Modify the dataset labels to perform **binary classification**: predicting whether an image contains a horse or not.  
   - Use only 6000 images from the CIFAR10 dataset.  
   - Freeze all layers of the best-performing model and fine-tune only the last layer for the new task. Report training time and accuracy.  
   - Then unfreeze all layers and repeat. Compare performance and training time with the frozen case.

4. **Optimizer Comparison**  
   Evaluate the following optimizers using a **constant learning rate** over 50 epochs:  
   `SGD`, `SGD with momentum`, `Nesterov`, `AdaGrad`, `Adam`, `Nadam`.  
   Plot and compare the **accuracy** and **loss** of each optimizer.

5. **Regularization Techniques**  
   Apply different regularization methods:  
   - `Dropout`  
   - `MC Dropout`  
   - `L1 + L2 Regularization`  
   Train each for 100 epochs and compare performance using accuracy and loss plots.  
   Discuss whether regularization improved the model.
