# Face Attendance System
Attendance system based on facial recognition is a method for identifying individuals based on their facial features and registering thier respective attendance.

### Table of contents
* [Problem Statement](#Problem-Statement)
* [Features](#Features)
* [Performance](#Performance)

### Problem Statement
The Existing attendance system used by the client was slow, inefficent, unreliable and consisted several loopholes. The new system had to overcome all the shortcomings of existing system at a low cost. A new pipeline was required to register the attendance of 500+ employees with high accuracy and low processing time.

#### Approach
Face attendance system can be of 2 types
* **Verification based sytem** - In such systems, usually a sub-system is used based on RFID or some other identifiers. The role of face recognition is to verify if the RFID credentials belongs to the person presenting it.

* **Recognition based system** - These systems solely depends on facial features and do not require any sub system for authentiaction.

To make cost effective solution and keep the complexity of the system minimum, we developed a Recognition based face attendance system. We throughly researched all the possible solutions available for the purpose of face recognition, vigorously tried and tested them and after 100+ iterations we sucessfully developed a solution, which met all the client demands along with additional perks.

#### Challanges Faced

* **Design** - To consider only the person standing in front of the system, we made a system inspired by a kiosk design so that only the person bent a little bit is only considered which drastically decreases the chance of unwanted detection

* **Computation** - The entire pipeline is deployed on edge devices, hence we had to develop efficient face detection and recognition pipeline that is not computationally expensive

* **Scalablity** - To register attendance of 500+ employees, we developed a scalable pipeline which can support n number of devices connected locally
#### Open Source Contributions

While developing this soultion we used several open source tools, we also collabrated and contributed to many open source projects such as,
* [Head Pose Estimation](https://github.com/by-sabbir/HeadPoseEstimation)
* [FaceNet TensorRT](https://github.com/nwesem/mtcnn_facenet_cpp_tensorRT/tree/develop)

### Features

* **0 downtime** - Since all the computations are done locally, and all the devices are connected on local network, there is no downtime because of internet outage.

* **Unkonwn People Attendance** - If there are people who arrive less frequently and aren't the part of attendance db, this system assigns a ID to the person and remembers the person when he/she arrives again.

* **Feedback** - For specially abled people, the feedback of attendace is conveyed through audio (in native language) as well as on the display

* **Spoof-Proof**



### Performance

* **Speed** - The system is 4x fater than the existing atendance system (based on the data collected over a month while testing)
* **Accuracy** - The system is 91.88% accurate (based on the data collected over a month while testing)

### Technologies Used
TensorRT, DeepStream SDK, Python, C++, Jetson Nano, TTS engine, Dlib, OpenCV, Face detection and Recognition models

