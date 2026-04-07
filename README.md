##  Vision-Based End-to-End Trajectory Prediction for Autonomous Vehicles

This project investigates **which visual features contribute most to accurate 
trajectory prediction in autonomous vehicles**, and whether task-specific 
attention mechanisms can outperform generic models for waypoint prediction.


![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat-square&logo=python)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0-orange?style=flat-square&logo=pytorch)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.19-FF6F00?style=flat-square&logo=tensorflow)
![Dataset](https://img.shields.io/badge/Dataset-Waymo%20Motion%20v1.3.1-green?style=flat-square)
![Status](https://img.shields.io/badge/Status-Active%20Research-yellow?style=flat-square)

---


Using the **Waymo Open Dataset Motion v1.3.1**, the research pipeline extracts 
agent trajectories, renders Bird's Eye View (BEV) scene representations from 
map features, and trains a CNN-LSTM model to predict future waypoints. The core 
contribution, currently in development - is a **spatial attention mechanism** 
that explicitly prioritizes semantically meaningful road regions (lane markings, 
vehicles, pedestrians) while suppressing irrelevant features.

> 🔬 This research is conducted as part of the **Fulton Undergraduate Research 
> Initiative (FURI)** at **Arizona State University**, under the supervision of 
> Professor Bharatesh Chakravarthi at the School of Computing and Augmented 
> Intelligence. The researcher is an undergraduate AI/CS researcher investigating 
> explainability and interpretability in autonomous vehicle perception systems.

## Tech Stack

| Category | Tools |
|---|---|
| Deep Learning | PyTorch, torchvision |
| Data Processing | TensorFlow, NumPy, Pandas |
| Visualization | Matplotlib, OpenCV |
| Infrastructure | Google Colab Pro, Tesla T4 GPU, Google Cloud Storage |
| Dataset | Waymo Open Dataset Motion v1.3.1 |

---

## Roadmap

- [x] Literature review — Trajectron++, ViP3D
- [x] Waymo data pipeline — tfrecord parsing, sequence extraction
- [x] BEV scene rendering — map features → top-down images
- [x] Baseline LSTM — ADE/FDE tracked across 15 epochs
- [x] CNN-LSTM architecture — ResNet18 + LSTM fusion
- [x] Train and evaluate CNN-LSTM baseline
- [ ] Implement task-specific spatial attention mechanism
- [x] Evaluate attention model vs baseline on ADE/FDE
- [x] Generate attention heatmaps — visualize feature importance
- [ ] Benchmark against Trajectron++ and ViP3D
- [ ] FURI final report and Fulton Forge Expo poster

---
