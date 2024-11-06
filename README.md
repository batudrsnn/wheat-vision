# Estimation of the number of wheat spikes and spikelets based on deep learning and computer vision
The goal of the thesis is to identify the charac- teristics of an optimal sensor setup for 2D/3D reconstruction of wheat plants to enable extraction of wheat plant phenotypic traits. A robust system using the sensor setup and computer vision algorithms for the field or uncontrolled settings is to be developed to automate the data collection process in the agriculture research to aid the analysis of the wheat crop best practices.

The project focuses on the detection and estimation of wheat head counts and then further detecting and counting grains from the detected wheat heads using the images captured from an RGB camera sensor in controlled or uncontrolled settings. The wheat head count per unit length provides information about plant density in the field, while the average wheat grain count per head can be used to estimate crop yield.

For wheat head detection, Otsu thresholding with dilation is applied on the image to remove the background and noise to achieve plant segmentation and then YOLO model is used to detect the wheat heads from the wheat plants RGB image. The detected wheat head bounding boxes are counted to estimate the number of wheat heads in the image and then further utilized for grain counting.

For wheat grain counting, the detected wheat heads from the previous steps are cropped out and then using Segment Anything Model (SAM) for segmentation and then connected components approach is used to count the grain masks in the wheat head. Further, intensity matching based approach is used to detect potential grains in the undetected grain area of the wheat head to further improve the accuracy of the grain estimates.

The developed solution works well in controlled as well as uncontrolled environment settings with the optimal sensor setup.
