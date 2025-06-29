## Rear-View Camera Object Detection and Alert System
### ITS – Assessment 2

## Project Title Proposal:  
### "AI Driven Driveway Safety System: Preventing Child Accidents with Computer Vision"   


### Overview
This project implements an object detection and alert system designed for use with vehicle rear-view cameras. Its purpose is to enhance safety during low-speed manoeuvring and parking, by detecting the presence of pedestrians, children, and animals within the vehicle’s path, and issuing visual and audible alerts to the driver.

Developed as part of Assessment 2 for the ITS module, this project demonstrates practical application of AI-based object detection in automotive safety systems.

### Features
Real-time object detection using YOLOv5

Detection of target objects including:
- People (Children and Adults)
- Pets (cats, dogs)
- Livestock (horses, sheep, cows)

Visual alerts via pop-up window
Audible alarm when target objects are detected continuously
Adjustable detection confidence threshold
Runs on video feed (rear-view camera simulation)

### Technologies Used
Python 3.x
Ultralytics YOLOv5
OpenCV
Tkinter (GUI alerts)
PyAudio (audio playback)
Wave (audio file handling)

 ### Installation
Requirements
Python 3.x

Required Python packages:
ultralytics
opencv-python
pyaudio
wave (part of Python standard library)
