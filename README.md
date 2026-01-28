# UCS654-assignment2
# Learning Probability Density Functions using GAN

## Methodology

- The NO₂ concentration data was extracted from the India Air Quality dataset.
- Missing values were removed before further processing.
- The input data was normalized to ensure stable GAN training.

### Data Transformation
Each value of the feature x was transformed using the equation:

z = x + a*sin(b x)

The parameters a and b were computed using the university roll number (102313060).

### GAN-based PDF Learning
- A Generative Adversarial Network (GAN) was used to learn the unknown distribution of z.
- The generator takes random noise from a normal distribution and produces synthetic z samples.
- The discriminator distinguishes between real and generated samples.
- Binary cross-entropy loss and Adam optimizer were used for training.

### PDF Estimation
- After training, a large number of samples were generated using the trained generator.
- Kernel Density Estimation (KDE) was applied to the generated samples to approximate the PDF.

### Estimated PDF
- The KDE plot of GAN-generated samples shows a smooth probability density function.
- A dominant mode and right-skewed behavior are observed.
- This indicates successful learning of the underlying distribution.
  
## Conclusion
The GAN successfully learned the probability density function of the transformed variable using only data samples. KDE applied on generated samples provided a smooth and reliable PDF approximation without assuming any parametric distribution.

