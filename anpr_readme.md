# Automatic NumberPlate Recognition

### Table of contents
* [Problem Statement](#Problem-Statement)
* [Features](#Features)
* [Performance](#Performance)

### Problem Statement
The system was required at a Special Economic Zone(SEZ). Daily approximately 4k to 5k Vehicles enter and exit the zone, All these vehicles go through several steps of verification before entering and exiting. Extracting the license plate number was one of the step which was a bottleneck in the entire pilepline as it was done by a human.

Our task was to design and develop a solution which can complete the task of number plate recognition which does not require the vehicle to stop explicitly to capture the number plate. The solution had to be native as the data is very confidential.


#### Approach
We used a 2 step approach to complete this task with least amount of of latency, high reliablity and low cost.

* **Number Plate Detection** - In this step we developed a highly accurate Numberplate detction model which could run on edge devices for real time detection.

* **Number Plate Recognition** - For this step we tried and tested several already existing solutions but none of then perfomed the way we were explecting, Hence we developed an OCR model to complete the task of recognition


#### Challanges Faced

* **Dataset Imbalance** - While developing a custom OCR model we face the issue of dataset imbalance, as the dataset we collected for site consisted some characters with very high frequency (because of abundance of local vehicles), while some had low frquency.

* **Quality of Dataset** - In India, even after the standardization of numberplates, there are several vehicles which consists of hand painted, decoloured, damaged number plates 

* **Scalablity** - A the SEZ has several gates at different places, the solution developed should be deployed at any gate and should be able to communicate to other gates.

### Features

* **0 downtime** - Since all the computations are done locally, and all the devices are connected on local network, there is no downtime because of internet outage and no data is sent out.

* **Retrofit** - As the computation are done natively, this system can be integrated with existing pipelines


### Performance

* **Speed** - The system is 10-12x fater than the existing manual system (based on the data collected over a month while testing)
* **Accuracy** - The system is 82.41% accurate (based on the data collected over a month while testing)

### Technologies Used
TensorRT, DeepStream SDK, Python, C++, Jetson Nano, OpenCV, Darknet, PyTorch
