# imres - Image Resolution

### 1. Introduction

Image logs are valuable sources of information used to support the development of petroleum fields.

They allow geoscientists to characterize visually and in a continuous manner different properties of the rocks perfurated by a well. This is used for building more reliable geological models of a field, which leads to more realistic production curves. 

Low resolution images or those presenting strong non-geological attributes (i.e. distortion, noise, pixelated images, etc.) - in other words, displaying low quality - are hard to interpret, losing part of their potential value. Image resolution can be defined based on whether it permits identification of small-scale features (such as structural information), large-scale features (such as lithology discontinuities), or no features at all.

Images obtained via LWD tools (*Logging While Drilling*) reduce the cost of acquisition, when compared to those obtained with wireline tools; however, they are also more susceptible to operational problems and, consequently, more likely to present lower quality.

The Figure below exemplifies well segments with low (red flag) and high (green flag) quality.

XX



### 2. Objective

The objective of this project is to construct a neural network capable of automatically identifying the low, medium and high resolution parts of a LWD image.

The purpose of this classification is to assist in quickly determining if a particular image ha been properly obtained and will be of use in the geological modelling process.

This knowledge can help support decision-making with regards to image acquisition for a particular well; for example, by indicating the need to perform a new LWD log or the need to include an imaging tool in the wireline assembly.

Furthermore, this information can also be correlated with different parameters used for monitoring the drilling operation (Weight-On-Bit, RPM, vibration, etc.), as well as with different BHA configurations being used to drill the wells of a field; thus, it can be used to identify potential factors that cause the image quality to degrade and allow the operator to take action accordingly.


### 3. Data

The data used in this project were the processed LWD images from 11 wells of various types (vertical, horizonal or slanted), and that crossed different lithologies (sand or carbonate reservoirs). In addition, a log of the image resolution was provided for training the neural network, indicating which well depths had low, medium and high resolution data.

The first notebook of the repository **imres_data_setup** should be used to parse through the original image and annotation files, which are tens of thousands of lines long, and create smaller, individual image and annotation files. The width of each image created is 120 pixels, corresponding to each of the channels of the LWD tool, and identical to the original log image. The height of each image was chosen arbitrarily to equal 512 pixels. Cropping was also performed so as to match the depths of the well image and the well resolution logs. The individual annotation files carry the resolution classifications related to their corresponding images.

A visual verification of the indiviual images was performed to ensure that the individual files were being created correctly. The Figure below depicts some of the images that were created by this script (gray scale) alongside the corresponding segment of the original image (orange scale).

XX

The second notebook of the repository **imres_data_split** is design to separate the data into a training set and a validation set, while maintaining a similar proportion of low, medium and high resolution segments in each of the sets as are present in the total population of images.


### 4. Results




