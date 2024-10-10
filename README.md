# Towards Accurate Head Shape Classification: A Machine Learning Approach Using Feature Extraction

## Overview
This project aims to develop a machine learning methodology to classify head shapes into various categories with high accuracy. This method has potential applications in automating the detection of cranial abnormalities, simplifying the early diagnosis of craniofacial issues. By associating the classification model with diagnostic tools, it can enhance diagnostic rates and reduce reliance on extensive medical expertise.

## Dataset
Due to the lack of publicly available datasets containing overhead images of alopecia heads, a new dataset was created. The images were collected from various sources and preprocessed by cropping, rotating, and augmenting them to ensure consistency and robustness for future research.

## Methodology
The [Segment Anything Model (SAM)](https://segment-anything.com/) was applied to the dataset to generate segmentation masks that accurately captured the head's contours. The following key metrics were defined and extracted from these masks for feature extraction:
- **Aspect Ratio**
- **Circumference**
- **Convexity**
- **Eccentricity**: Computed as the ratio of the distance between the foci of the shape over the major axis length to detect elongated or compressed head shapes.
- **Compactness**: The ratio of the head area to its smallest enclosing circle, indicating how well the head fills its boundary.
- **Symmetry**: Measured by comparing the left and right halves of the mask using Mean Squared Error, where a lower error indicates higher symmetry.
- **Ellipticity**

These metrics were then used to train a machine learning model capable of classifying different head shapes.

## Next Steps
- **Dataset Expansion**: The dataset will be expanded using Generative Adversarial Networks (GANs) and 3D modeling to synthesize head images with controlled variations in shape and pose.
- **Testing Generalization**: The model will be tested for its ability to generalize across varied head poses, ensuring consistent and robust performance.
- **Facial Shape Prediction**: The project will explore predicting specific facial shapes based on cranial outlines, potentially advancing fields such as forensic science and virtual reality.

## Applications
This project has the potential to contribute to multiple fields, including:
- **Medical Diagnosis**: Early detection of craniofacial abnormalities.
- **Forensic Science**: Prediction of facial shapes based on cranial outlines.
- **Virtual Reality**: Enhanced head and face modeling for virtual environments.
