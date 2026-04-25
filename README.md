# CompressorLeak
Compressor Leak Detection System UI
# 🌬️ Indufy: IoT-Based Compressor Leak Detection System

![System Status](https://img.shields.io/badge/Status-Prototype_v0.5-blue)
![Hardware](https://img.shields.io/badge/Hardware-ESP32--S3-orange)
![Network](https://img.shields.io/badge/Network-LoRa_|_Wi--Fi-green)

**Indufy** is a continuous, smart monitoring solution designed to detect compressed air leaks in industrial manufacturing plants. Developed as a Capstone/Graduation Project, this system utilizes ultrasonic acoustic sensing, Edge Digital Signal Processing (DSP), and a scalable LoRa/Wi-Fi mesh topology to identify, quantify, and report energy-wasting leaks in real-time.

## 📖 About the Project

Compressed air is one of the most expensive utilities in manufacturing, with 20-30% of compressor output typically lost to hidden leaks. Traditional handheld detection methods are manual, periodic, and reactive. 

**Indufy solves this by providing a 24/7 continuous monitoring system.** By "listening" to the 40-50 kHz ultrasonic frequency band, the system isolates the sound of turbulent air leaks from standard plant background noise. 

This project is supported by **TÜBİTAK 1812 (BİGG)** and developed at **Baskent University** (Electrical and Electronics Engineering Department).

## ✨ Key Features

*   **Continuous 24/7 Monitoring:** Fixed nodes eliminate the need for periodic manual inspections.
*   **Ultrasonic Precision:** Uses Digital PDM MEMS microphones combined with software-defined Band-Pass Filtering (40-50 kHz) via I2S to ensure high Signal-to-Noise Ratio (SNR).
*   **Hysteresis Decision Logic:** Advanced firmware algorithms prevent false alarms from temporary mechanical noises.
*   **Flexible Topology (Master/Slave):** 
    *   **Nodes (Slaves):** Gather acoustic data and send leak events via low-power LoRa (868 MHz).
    *   **Gateways (Masters):** Forward aggregated data to the cloud via 2.4 GHz Wi-Fi.
*   **Apple-Style Web App:** A dark-mode, responsive industrial UI for maintenance teams to track leak rates, system health, and estimated energy losses.

## 🛠️ Hardware Architecture

All field devices share a unified, compact PCB design. Roles (Node vs. Gateway) are assigned logically via firmware based on Wi-Fi coverage availability.

*   **Microcontroller:** Dual-core ESP32-S3 (Handles DSP, I2S, LoRa stack, and Wi-Fi).
*   **Acoustic Sensor:** SPH0641LU4H-1 (Bottom-port, digital PDM MEMS microphone).
*   **Wireless Communication:** Ai-Thinker Ra-01 (LoRa @ 868 MHz) & Integrated ESP32 Wi-Fi (2.4 GHz).
*   **Power Regulation:** TPS62840DLCR (High-efficiency step-down converter with ultra-low quiescent current).

## 💻 Software & Dashboard

The web dashboard is built using modern HTML, CSS, and vanilla JavaScript. It provides a real-time summary of the factory floor, active leak locations, and allows technicians to provision new devices seamlessly using an interactive SoftAP simulation.

made on earth by humans _TAMER_
