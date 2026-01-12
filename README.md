# Adaptive-Denoising-Framework 🛠️

### A Modular, Reproducible, and Adaptive Image Restoration Platform

> **Developed independently by an undergraduate student.**
> This project bridges the gap between theoretical algorithms and production-ready systems. It provides a robust infrastructure for evaluating, comparing, and deploying impulse noise removal algorithms under real-world constraints.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

---

## 💡 Design Philosophy

In academic research, reproducibility and systematic evaluation are often overlooked. I built this framework to address three key engineering challenges in image restoration:

1.  **Adaptability**: How to balance quality vs. speed dynamically based on image content?
2.  **Reliability**: How to prevent memory leaks and ensure stability during large-scale batch processing?
3.  **Reproducibility**: How to manage configurations, random seeds, and evaluation metrics in a standardized way?

This framework integrates a **Quality-Speed Dual Pipeline**, an **Adaptive Mode Selector**, and a **Robust Memory Manager** to solve these problems.

---

## 🏗️ System Architecture

The framework is organized into three layers:

*   **Core Layer**: Implements the fundamental restoration logic (AWLF-based), feature extraction, and clustering.
*   **Pipeline Layer**: Orchestrates the core modules into `QualityMode` (high precision), `SpeedMode` (high throughput), and `AdaptiveMode` (smart selection).
*   **Infrastructure Layer**: Handles configuration validation, memory safety, caching, and experiment logging.

---

## 📊 Key Features

- **🧠 Adaptive Mode Selection**: Automatically switches between Quality and Speed modes based on noise density and texture complexity.
- **🛡️ Memory Safety**: Built-in `MemoryManager` monitors RAM usage and performs active garbage collection and cache eviction.
- **⚡ Smart Caching**: Feature maps are cached with hash-based keys to avoid redundant computations.
- **📈 Comprehensive Evaluation**: Integrated calculation of PSNR, SSIM, FSIM, and VIF metrics.

---

## 🚀 Quick Start

### 1. Installation
```bash
pip install -r requirements.txt

