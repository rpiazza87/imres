# imres
## Identify segments of low and high resolution in LWD images



### 1. Introduction

Image logs are valuable sources of information used to support the development of petroleum fields.

They allow geoscientists to characterize visually and in a continuous manner different properties of the rocks perfurated by a well, which serves to construct more reliable geological models of a field - leading, in turn, to more realistic production curves. 

Low resolution images or those with strong non-geological attributes (i.e. distortion, noise, pixelated images, etc.) - in other words, displaying low quality - are hard to interpret, losing part of their potential value. Another form of classifying the quality of an image is through its resolution. That is, whether it is possible to identify small-scale features (such as structural information), large-scale features (such as lithology discontinuities), or no features at all.

Images obtained via LWD tools (*Logging While Drilling*) reduce the cost of acquisition, when compared to those obtained with wireline tools; however, they are also more susceptible to operational problems and, consequently, to present lower quality.

The Figure below exemplifies well segments with low (red flag) and high (green flag) quality.

XX



### 2. Objective

The objective of this project is to construct a neural network capable of automatically identifying the low, medium and high resolution parts of a LWD image.

The purpose of this classification is to aid in quickly determining if a particular image ha been properly obtained and will be of use in the geological model.

This knowledge can help support decision-making with regards to image acquisition for a particular well; for example, by indicating the need to perform a new LWD log or the need to include an imaging tool in the wireline assembly.

Furthermore, this information can be correlated with different parameters used for monitoring the drilling operation (Weight-On-Bit, RPM, vibration, etc.), as well as with different BHA configurations being used, so as to identify potential factors that cause the image quality to degrade and take action accordingly.



### 3. Data

The data used in this project were the processed LWD images from 11 wells of various types (vertical, horizonal or slanted), and that crossed different lithologies (sand or carbonate reservoirs). In addition, a log of the image resolution was provided for training the neural network.



### 4. Results




