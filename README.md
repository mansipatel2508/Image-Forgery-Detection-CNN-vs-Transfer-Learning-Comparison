# Image Forgery Detection CNN vs Transfer Learning Comparison
Image Preprocessing | Image Handling | Data visualization | Transfer Learning | Deep CNN | Binary Classification | Model Evaluation &amp; Comparison | Conclusion &amp; Future scope
# Problem Statement
In the field of Digital Forensics, it is important to know the authenticity or originality of an image, this project focuses on predicting the given image is pristine or fake/manipulated/edited/photoshoped.

Image Preprocessing | Image Handling | Data visualization | Feature extraction & engineering | Transfer Learning | Deep CNN | Binary Classification | Model Evaluation & Comparison | Conclusion & Future scope | OpenCV

The project definition and dataset is the part of first IEEE Image Forensics challange launched in 2013 and to observe the experimental result of deep CNN network vs Transfer Learning which used VGG16 as trained model.

The challange has 2 phases, dealing with the first phase in this project to detect if its real or fake image, binary classification problem.

The project learnings
* Image Handling and Processing
* Using Image data generator
* Observering the performaces CNN vs Transfer Learning
* Feature engineering.extraction on images
* Otsu’s thresholding on images
* Converting greyscale images to binary
* Image normalization

Libraries Exposure
* OpenCV : cv2
* Image Data Generator
* Pylab : rcParams
* imageio : imread
* pickle

# Dataset
* Dataset has 2 folders containing 900 fake images and 1050 pristine images
* Used the train dataset which arounf 2 GB and splited train-test from that (Processor Contraint)
* Online:  http://ifc.recod.ic.unicamp.br/fc.website/index.py?sec=0
#Understanding the data

* Pristine Images : 1050

* Fake Images : 900

>  * Fake images : 450

> * Masks : 450
## Mask for the fake image
* Indentify where exactly the image is forgerized/edited
* Seperated the masks from the fake images
## Plotting the Depth of the Images
* The images with various channel/depth
* Need to convert all the images to the one majority image channel or remove those.
## Shape conflict
* Fake and mask of the fake images were in different shape 
* Reshape the mask as fake
## Final Data
* Fake Images : 450
> * Converted to 3 channel depth
*Pristine Images : 1025
>* Removed 1 & 4 channel depth
* Masks : 450
>*Converted to 1 channel depth (grayscale)
# Data Sampling
* Fake images : 450
* Pristine images : 450

# Train -Test Split
* Train - Test : 70% - 30%
* Set ‘Stratify’ parameter to labels
# Model Comparison
# Feature Extraction for Performance boost

* Sampled the fake image by using it’s mask values
>* Masks converted into binary so that the masks' boundary would be more prominent and distinctive
>* Sobel kernel concept was implemented to make samples from fake such that 60% in the image is non-edited while 40% is edited
* For pristine image randomly made samples

>* Sample size : 64 x 64 x 3

# Data Volume
* 50,000 fake samples
* 50,000 pristine samples

A fake sample example is as follows
# Model Evaluation
# Model Comparison

Mini Project5

Mansi Patel

May 10, 2019

Prof: H.Chen

CSC 215 
