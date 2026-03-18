# ☁️ Secure IoT Communication via AWS IoT Core

## 📌 Project Overview
This project demonstrates the implementation of a secure messaging pipeline between a local device (acting as an IoT 'Thing') and **AWS IoT Core**. [cite_start]It focuses on **Mutual TLS (mTLS)** authentication and real-time telemetry using the **MQTT v5** protocol. [cite: 1, 2, 4]

## 🚀 Key Technical Features
- [cite_start]**Security:** Established a secure handshake using X.509 certificates and an RSA 2048-bit public key. [cite: 1]
- [cite_start]**Authorization:** Configured an AWS IoT Policy with granular permissions (`iot:Publish`, `iot:Subscribe`, `iot:Connect`) restricted to specific MQTT topics like `sdk/test/python`. [cite: 2, 3, 4]
- [cite_start]**Protocol:** Leveraged MQTT v5 for efficient, low-latency bi-directional communication between the edge device and the cloud. [cite: 2]
- [cite_start]**SDK:** Integrated the **AWS IoT Device SDK v2 for Python** to manage the lifecycle of the connection. [cite: 4]

## 📂 Repository Structure
- [cite_start]**`MyLaptop_Thing-Policy`**: The JSON policy defining secure access control for the IoT device. [cite: 2]
- [cite_start]**`MyLaptop_Thing.public.key`**: The public component of the RSA key pair used for device identification. [cite: 1]

## 📊 Results & Verification
The connection was successfully verified with a `SUCCESS: 0` reason code. [cite_start]Real-time messages were monitored through the **AWS MQTT Test Client**, ensuring a stable and encrypted data flow from the local machine to the AWS Cloud infrastructure. [cite: 2]
