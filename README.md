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


## **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
