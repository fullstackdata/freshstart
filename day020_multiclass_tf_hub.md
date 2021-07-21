# Multi-class Image Classification with Tensorflow Hub Model
1. Load data
2. Prepare data 
  * Create one hot encoding labels  
  * Load images
  * convert them to tensors
  * Normalize
  * Resize
3. Create train and validation splits using sci-kit
4. Create batches
  * Check out element_spec of the tensor
5. Setup model url from Tensorflow Hub
6. Creating a model
  * tf.keras.Sequential([hub model layer, output layer])
  * compile
    * loss function 
    * optimizer
    * metrics
  * build
 7. Create Tensorboard hooks
 8. Train the model - model.fit
 9. Predict
 10. Format for a saved keras model - h5


Early stopping helps prevent overfitting when the evaluation metric stop improving.
Number of epochs can be set to a high value, but since early stopping callback is registered, the epochs can be limited to the most optimal number.
