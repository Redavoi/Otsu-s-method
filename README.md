# Otsu-s-method

Here you can find a code for Otsu's method done by maximizing the inter-class variance.

## Formulae

---
The formula used to find the optimal threshold is:

true_threshold = $\underset{t}{argmax}(\omega_0(t)\omega_1(t)(\mu_0(t) - \mu_1(t))^2)$, where

t - is equal to current threshold,

$\omega_0(t) = \sum\limits_{i=0}^{t-1}P(i)$, P(i) - is probability of i-th grayscale tone

$\omega_1(t) = \sum\limits_{i=t}^{L-1}P(i)$, L - is total amount of our grayscale bins (256)

$\mu_0(t) = \frac{\sum\limits_{i=0}^{t-1}P(i)i}{\omega_0(t)}$

$\mu_1(t) = \frac{\sum\limits_{i=t}^{L-1}P(i)i}{\omega_1(t)}$

## Results

---
That algorithm was tested on this image:

![image](https://user-images.githubusercontent.com/59142478/211662332-7bfc7957-fd7e-489a-95c6-2b264bf0bea9.png)

Histogram of this image:

![image](https://user-images.githubusercontent.com/59142478/211662478-0a97fdb3-de93-4b69-a160-7466f3698ba3.png)

After working algorithm gives us threshold equal to 152:

![image](https://user-images.githubusercontent.com/59142478/211662629-a13161cb-8ddc-432b-8385-d6f9b8a3584e.png)

And final binarization for that threshold:

![image](https://user-images.githubusercontent.com/59142478/211662848-c39d26d4-f3be-4316-b4aa-c7dc097960cb.png)
