# Kaggle MNIST Digit Recognizer - Numpy and Pandas Only
## _Simple NN from scratch_



This is a simple NN with 1 hidden layer trained to classify digits from the Kaggle MNIST data set. 
The architechture of the neywork is very basic: 
- 784-node  input layer
- 16-node hidden layer with ReLU activation
- 10-node output layer with softmax activation

Loss function: categorical cross-entropy (log loss). 
## Motivation💡

As someone deeply interested in the math and algorithms that form the foundation of even the most intricate models, I wanted to code a small model that illustrates the main principles of neural networks without relying on frameworks. 
This project is motivated by wanting to more profoundly understand the math behind NNs in practice, as an intro to AI development.
Perhaps someone just getting started with the field may also find value in this project, and be inspired to discover more.

## Features
- Parameter and cache dictionaries
- Forward prop, backprop, gradient descent
- Prediction and visualization of random test digits [^1]
- Accuracy visualization with confusion matrix  
 

## Batching

The model is trained using the following batching and epoch hyperparameters:
- 64 batch size
- 937 batches per epoch
- 20 epochs


## Accuracy Calculation
The model accuracy is calculated as an average accuracy over 20 epochs.
The epoch accuracy is calculated as $$\text{accuracy} = \frac{\text{correct predictions}}{\text{total predictions}}$$ over 937 batches.



##  Notes
This is a minimal NN for a simple dataset, so it’s not designed for deployment. The value lies in gaining a deeper understanding of:  
- Working with data formats  
- Linear algebra & calculus behind NNs  
- Backpropagation & gradient descent  
- Training loops & accuracy evaluation

There are many tweaks and augmentations one could do to make a model with similar characteristics perform better, possible improvements being:
- Increasing neuron count, 
- Adding more hidden layers, 
- Data Augmentation
- [He initialization] for ReLU activations
- Decreasing the learning rate for greater stability given a more complex model.

##  Confusion Matrix Example
![Confusion Matrix](/confusion_matrix.png)


####

   [He initialization]: <https://en.wikipedia.org/wiki/Weight_initialization#He_initialization>


   [^1]: since the Kaggle MNIST competition dataset is structured such that only the training data contains labels, an accuracy score for test images isn't a feasible metric to measure. If data augmentation is employed, one could create a separate test set using the labeled training set, and actually obtain test set accuracy

