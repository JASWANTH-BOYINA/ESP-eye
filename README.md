# ESP-eye (Object detection using ESP32-CAM and Edge Impulse)
## **Project Overviwe**
This project explores the implementation of real-time object detection using the ESP32-CAM microcontroller and Edge Impulse, a machine learning development platform optimized for edge devices. By leveraging the low-cost, Wi-Fi-enabled ESP32-CAM module and Edge Impulse's cloud-based model training and deployment tools, we create a compact, efficient system capable of recognizing and classifying objects in real-time. The system captures image data through the onboard camera, processes it with a lightweight neural network trained on custom datasets, and delivers detection results locally or via a web interface. This approach demonstrates the potential of embedded AI for applications in surveillance, automation, and IoT with minimal hardware and cost.
____
## **Components**
1.	ESP32-CAM
2.	USB to Serial Converter
3.	OLED Display
4.	Breadboard
5.	Jumper wires
____
## **Methodology**
  The development of this project follows a structured and modular approach to achieve real-time object detection on a resource-constrained embedded device. The steps involved are:
  
1. **Hardware Setup**
    - The ESP32-CAM module is connected to an FTDI USB-to-Serial programmer for code uploading.
    -	An OLED display is interfaced with the ESP32-CAM using I2C (GPIO 14 for SDA and GPIO 15 for SCL) to visualize object detection results.
2. **Data Collection**
    -	A dataset of object images is either collected using the ESP32-CAM or uploaded manually to the Edge Impulse platform.
    -	Images are labeled into classes (e.g., "bottle", "pen", "phone") to train the model.
3. **Model Training on Edge Impulse**
    -	Images are preprocessed and fed into a Convolutional Neural Network (CNN) using Edge Impulse.
    -	The model is trained and optimized using techniques such as quantization to reduce memory usage, allowing it to run efficiently on the ESP32-CAM.
4. **Model Deployment**
    -	After training, the model is exported from Edge Impulse as an Arduino library.
    -	This library is integrated into an Arduino sketch that includes logic for capturing images and running inference.
    -	The sketch is uploaded to the ESP32-CAM using the Arduino IDE and FTDI programmer.
5. **Inference and Display**
    -	Once deployed, the ESP32-CAM captures images in real-time.
    -	The onboard model classifies each image and sends the predicted object label to the OLED display.
    -	The system functions completely offline, without the need for a cloud server.
____
## **Future Scope**
-	Enhanced Model Accuracy with Edge AI
-	Integration with Cloud & IoT
-	AI-Powered Automation
-	5G and Low-Power Connectivity
____
## **Tools Required**
1. Edge Impulse
2. Arduino IDE
