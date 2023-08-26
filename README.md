# CAN Anomaly Detection
## The Task
The Controller Area Network (CAN) is currently the most widely-used in-vehicle networking protocol. CAN is a bi-directional, multi-master, serial bus that uses UTP cabling to ensure reliability in electromagnetically noisy environments.
It provides an effective method for the components of a vehicle called the Electronic Control Units (ECU) to communicate among themselves, as opposed to traditional point-to-point wiring. It is also used in industrial applications as the basis for Devicenet, reducing the wiring needed between a control system and I/O devices.

While it provides a means to communicate reliably, CAN is not known for security. Modern vehicles allow you to plug in devices that can communicate on this network through the OBD-II port or some other port like the USB. Also, some of the devices in modern vehicles that use the CAN are connected to the internet, allowing external attacks in various forms. These attacks include Replay, Spoofing, Denial of Service (DOS) and so on.  

The task in this project is to **detect attacks on the CAN**.  
  
This will be done using different methods. The methods are:
1. Frequency-based detection  
Frequency-based methods use the increase in CAN transmission during attacks as the heuristic for detection.
2. Payload-based detection  
Payload-based methods read the data that is transmitted and detect when the data is unusual or unexpected. I will implement two payload-based detection models, one using the Local Outlier Factor algorithm (density estimation) and the second using an autoencoder (reconstruction error).

## The Dataset
The dataset used in this project is the **Real ORNL Automotive Dynamometer (ROAD) CAN Intrusion Dataset**, from (Verma et al., 2020). It can be found [here](https://0xsam.com/road/). The dataset consists of over 3.5 hours of an (unspecified) vehicle’s CAN data. ROAD contains ambient data recorded during a diverse set of activities, and attacks of increasing stealth with multiple variants and instances of real fuzzing, fabrication, and unique advanced attacks, as well as simulated masquerade attacks. In the paper, the authors discuss that the purpose of the dataset is to provide a CAN benchmark dataset free of the problems of previous public datasets such as the lack of comparability and the inconsistency of CAN message intervals due to the insertion of synthetic data post-recording.

The dataset consists of three folders: ambient, attacks and signal extractions.