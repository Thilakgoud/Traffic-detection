# 🚦 AI-Based Traffic Congestion Detection and Lane Priority System

## 📌 Project Overview

This project is an AI-based traffic congestion detection system using YOLO11 and computer vision.

The system detects different types of vehicles from traffic images, assigns vehicles to road lanes, calculates lane-wise congestion scores, and identifies the lane that should receive traffic signal priority.

## 🎯 Objectives

- Detect vehicles using YOLO11
- Classify different vehicle types
- Count vehicles lane-wise
- Calculate traffic congestion
- Classify congestion as Low, Medium, or High
- Identify the most congested lane
- Automatically select the lane for green-signal priority

## 🚗 Vehicle Classes

The trained YOLO model detects 7 classes:

1. Bicycle
2. Bus
3. Car
4. Motorbike
5. Rickshaw
6. Truck
7. Van

## 🧠 Technologies Used

- Python
- YOLO11
- Ultralytics
- PyTorch
- OpenCV
- Computer Vision

## 🔄 System Workflow

Traffic Image
↓
YOLO11 Vehicle Detection
↓
Vehicle Classification
↓
Lane Assignment
↓
Vehicle Counting
↓
Vehicle Weighting
↓
Congestion Score
↓
Low / Medium / High
↓
Most Congested Lane
↓
Green Signal Priority

## 📊 Congestion Weighting

Different vehicle types are assigned different weights based on their approximate road occupancy.

| Vehicle | Weight |
|---|---:|
| Bicycle | 0.5 |
| Motorbike | 0.5 |
| Rickshaw | 1.0 |
| Car | 1.0 |
| Van | 1.2 |
| Bus | 2.5 |
| Truck | 3.0 |

## 🚦 Signal Decision

The system compares the congestion score of all four lanes.

The lane with the highest congestion score is selected as the priority lane for the green signal.

## 📁 Project Structure

```text
traffic_congestion/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── src/
│   ├── detect.py
│   ├── lane_detection.py
│   └── congestion.py
│
├── results/
├── models/
└── data/
