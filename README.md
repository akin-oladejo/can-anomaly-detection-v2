# CAN Anomaly Detection
## The Task
The Controller Area Network (CAN) is currently the most widely-used in-vehicle networking protocol. It is a bi-directional, multi-master, serial bus that uses UTP cabling to ensure reliability in electromagnetically noisy environments. Several devices in modern vehicles communicate with each other using the CAN protocol. Some of these devices are connected to the internet, allowing external attacks in various forms such as Replay, Spoofing, Denial of Service (DOS) and so on. In this project, different methods will be employed to detect attacks on the CAN.

The methods are:
- Frequency-based detection
- Density-based anomaly detection (i.e Local Outlier Factor)
- Anomaly detection using the latent representation of normal data (i.e. autoencoder)

## The Dataset
The dataset used in this project is the Automotive Controller Area Network (CAN) Bus Intrusion Dataset v2. It can be found here. This dataset contains automotive Controller Area Network (CAN) bus data from three systems: two cars (Opel Astra and Renault Clio) and from a CAN bus prototype made by the authors of the dataset. Its purpose is to evaluate CAN bus Network Intrusion Detection Systems (NIDS). For each vehicle/system, there is a collection of log files captured from its CAN bus: normal (attack-free) data for training and testing detection algorithms, and different CAN bus attacks (Diagnostic, Fuzzing attacks, Replay attack, Suspension attack and Denial-of-Service attack).

For this project, I used data from the Renault Clio. The description of the different logs and attacks can be found in the README [here](RenaultClio/README)
