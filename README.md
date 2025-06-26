# TODO Implementing Autoencoder

- [x] Encoders, layers to compress input to latent space with relu activation function
- [x] latent space specifying the bottle neck layer size with 64 dimensions
- [x] decoder is mirroring the encoder to reconstruct input



# MSE loss function maths

For a model with parameters $ \theta $, the loss function is:

$$
L(\theta) = \frac{1}{n} \sum_{i=1}^n (y_i - \hat{y}_i(\theta))^2
$$

The gradient with respect to a parameter $\theta_j $ is:

$$
\frac{\partial L}{\partial \theta_j} = -\frac{2}{n} \sum_{i=1}^n (y_i - \hat{y}_i(\theta)) \cdot \frac{\partial \hat{y}_i(\theta)}{\partial \theta_j}
$$


Advantages of MSE:
Simple to compute and interpret.

Convex for linear models, ensuring a global minimum.

Works well with gradient-based optimization.

Disadvantages:
Sensitive to outliers due to squaring.

Units are squared, which may require taking the square root (RMSE) for interpretability.

