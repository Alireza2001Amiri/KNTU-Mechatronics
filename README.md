# **Crop Row Detection and Waypoint Definition Using Aerial Images of Fields**

## **Authors**

**Alireza Amiri**  
Department of Mechatronics Engineering  
Khaje Nasir Toosi University of Technology (KNTU), Tehran, Iran  
[ali.amiri@email.kntu.ac.ir](mailto:ali.amiri@email.kntu.ac.ir)

**Saeed Khankalantary**  
Department of Mechatronics Engineering  
Khaje Nasir Toosi University of Technology (KNTU), Tehran, Iran  
[s.kalantary@kntu.ac.ir](mailto:s.kalantary@kntu.ac.ir)

## **Abstract**

As autonomous agriculture evolves, precise waypoint generation is crucial for defining the paths of autonomous robots. This project presents a method leveraging high-resolution aerial imagery to detect crop positions and determine waypoints. The approach includes:

- **Hardware Setup**: A camera, wireless transmitter, and receiver for capturing live images.
- **Image Processing**: Detecting crops using Unet and K-means clustering; applying Hough Transform for detecting crop row lines.
- **Waypoint Generation**: Identifying points along crop rows and converting these into global coordinates for real-time navigation.

## **Introduction**

In the quest to enhance agricultural productivity and sustainability, autonomous robots play a pivotal role. This project addresses the challenge of accurately defining paths for these robots by integrating advanced image processing techniques and machine learning models. Traditional GPS-based navigation systems face challenges in precise row alignment, which this project aims to overcome using UAV-based aerial imagery.

## **Methodology**

### **1. Data Acquisition**

- **Camera Selection**: The GoPro Hero 4 was chosen for its high-resolution RGB imaging capabilities.
- **GPS Module**: The Ublox-Neo-6m provides global coordinates, essential for converting local pixel positions into global coordinates.

### **2. Image Processing**

- **Preprocessing**: Aerial images are divided into smaller, manageable sections.
- **Crop Detection**:
  - **Color Filtering**: Initially used but refined through HSV conversion.
  - **Unet-Based Segmentation**: Achieved 96% accuracy in detecting crop areas.
- **Crop Row Detection**:
  - **Hough Transform**: Applied to detect and refine lines representing crop rows.

### **3. Path and Waypoint Generation**

- **Waypoint Definition**: Paths are defined as lines parallel to crop rows, with points recorded for navigation.
- **Coordination Conversion**:
  - **Pixel to Meter**: Conversion based on camera height and image length.
  - **Meter to Global**: Translation into global coordinates.

## **Results**

The system successfully detects crop rows and generates waypoints with high accuracy, demonstrating its effectiveness in real-world agricultural scenarios.

## **Conclusion**

This approach provides a robust solution for autonomous agricultural systems, combining aerial imagery with advanced image processing to ensure precise navigation. It supports autonomous robots in navigating fields efficiently and effectively.

## **References**

- [1] Y. Yang et al., "Real-time detection of crop rows in maize fields based on autonomous extraction of ROI," *Expert Systems with Applications*, vol. 213, p. 118826, 2023.
- [2] J. Shi et al., "Row detection BASED navigation and guidance for agricultural robots and autonomous vehicles in row-crop fields," *Agronomy*, vol. 13, no. 7, p. 1780, 2023.
- [3] V. R. Ponnambalam et al., "Autonomous crop row guidance using adaptive multi-roi in strawberry fields," *Sensors*, vol. 20, no. 18, p. 5249, 2020.
- [4] N. Cunha et al., "Multispectral image segmentation in agriculture: A comprehensive study on fusion approaches," in *Iberian Robotics conference*, 2023: Springer, pp. 311-323.
- [5] T. Barros et al., "Multispectral vineyard segmentation: A deep learning comparison study," *Computers and Electronics in Agriculture*, vol. 195, p. 106782, 2022.
- [6] G. Ronchetti et al., "Crop row detection through UAV surveys to optimize on-farm irrigation management," *Remote Sensing*, vol. 12, no. 12, p. 1967, 2020.
- [7] M. Hassanein et al., "Crop row detection procedure using low-cost UAV imagery system," *The International Archives of the Photogrammetry, Remote Sensing and Spatial Information Sciences*, vol. 42, pp. 349-356, 2019.
- [8] M. D. Bah et al., "CRowNet: Deep network for crop row detection in UAV images," *IEEE Access*, vol. 8, pp. 5189-5200, 2019.
- [9] I. Sa et al., "WeedMap: A large-scale semantic weed mapping framework using aerial multispectral imaging and deep neural network for precision farming," *Remote Sensing*, vol. 10, no. 9, p. 1423, 2018.
- [10] S. Sankaran et al., "Low-altitude, high-resolution aerial imaging systems for row and field crop phenotyping: A review," *European Journal of Agronomy*, vol. 70, pp. 112-123, 2015.
- [11] L. Comba et al., "Vineyard detection from unmanned aerial systems images," *Computers and Electronics in Agriculture*, vol. 114, pp. 78-87, 2015.
- [12] K. Ramesh et al., "Detection of rows in agricultural crop images acquired by remote sensing from a UAV," *International Journal of Image, Graphics and Signal Processing*, vol. 8, no. 11, p. 25, 2016.
- [13] M. Pérez-Ortiz et al., "A semi-supervised system for weed mapping in sunflower crops using unmanned aerial vehicles and a crop row detection method," *Applied Soft Computing*, vol. 37, pp. 533-544, 2015.
- [14] Y. Pang et al., "Improved crop row detection with deep neural network for early-season maize stand count in UAV imagery," *Computers and Electronics in Agriculture*, vol. 178, p. 105766, 2020.
- [15] N. Samet et al., "Houghnet: Integrating near and long-range evidence for bottom-up object detection," in *Computer Vision–ECCV 2020: 16th European Conference*, Glasgow, UK, August 23–28, 2020, Proceedings, Part XXV, Springer, pp. 406-423.

## **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
