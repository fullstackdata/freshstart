##### Loss function 
Error calculated for just one record is called a Loss function.

##### Cost function
Error calculated for a batch, could be a mini-batch or an epoch.

##### Loss Functions
* Mean Squared Error loss
  * Quadratic function yields a global minimum, no local minima
  * Penalization of the model by squaring the error
  * Disadvantage - not robust to outliers
* Mean Absolute Error
  * More robust to outliers
  * Computation is very difficult 
  * May have local minima
* Huber Loss
  * Combination of MSE and MAE
  * If the error is higher than a certain delta, use MAE, else MSE.

#### Classification Loss Functions
* Cross-Entropy
  * Binary class, sigmoid activation
  * Multi-class, softmax activation
  

