# IOT_DEVICE_CLASSIFICATION


# Overview

This project focuses on classifying IoT devices based on their network traffic captured in PCAP files. PCAP (Packet Capture) files are records of network traffic, capturing details of packets transmitted between devices. These PCAP files are preprocessed and converted into CSV files to extract relevant features for classification.

# Data Preprocessing

# Packet Capture and Parsing:
- Utilize packet capturing tools to record network traffic from IoT devices.
- Parse captured packets to extract relevant information.

# Feature Extraction:

Extract the following properties for each packet:

-Packet Size (int)
-Destination IP counter (int)
-Source Port (int)
-Destination Port (int)
-Link layer protocol (ARP / LLC) - Binary
-Network layer protocol (IP / ICMP / ICMPv6 / EAPoL) - Binary
-Transport layer protocol (TCP / UDP) - Binary
-Application layer protocol (HTTP / HTTPS / DHCP / BOOTP / SSDP / DNS / MDNS / NTP) - Binary
-IP options (Padding / RouterAlert) - Binary
-Packet Content (Size (int) / Raw data) - Binary
-IP Address (Destination IP counter) - Binary
-Port Class (Source (int) / Destination (int)) - Binary
-Array Representation:
-Convert extracted features into a structured array, ensuring a consistent format for subsequent steps.
-Normalize numerical features for model training.


# GRU-Based Encoder-Decoder Model

Model Architecture:

Design a GRU-based neural network architecture with an encoder-decoder structure.

Input the array representation of each packet into the encoder.

# Temporal Encoding:
Leverage GRU layers to capture temporal dependencies within network traffic data.

The encoder transforms input arrays into a latent space representation.

# Decoder Reconstruction:

Utilize the decoder to reconstruct the original input from the latent space representation.

# Training and Evaluation

Dataset Split:

Divide the dataset into training, validation, and test sets to ensure unbiased evaluation.

Loss Function and Optimizer:

Choose an appropriate loss function (e.g., mean squared error) and optimizer (e.g., Adam) for model training.
