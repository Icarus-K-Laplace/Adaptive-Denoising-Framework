
---

### 6. 📝 `docs/performance_report.md` (性能报告示例)

这是一个**模板**，展示你的框架能生成什么样的报告。

```markdown
# Performance Benchmark Report

**Date:** 2024-01-20
**Device:** Intel Core i7-12700H, 16GB RAM
**Dataset:** Tianjin University UAV Infrared Dataset

---

## 1. Summary

| Metric | Speed Mode | Quality Mode | Improvement |
| :--- | :---: | :---: | :---: |
| **Avg PSNR** | 32.5 dB | **34.8 dB** | +2.3 dB |
| **Avg SSIM** | 0.91 | **0.96** | +0.05 |
| **Avg Time** | **0.8s** | 4.2s | 5.2x Faster |

> **Conclusion**: Quality Mode provides significant visual improvements for high-texture images, while Speed Mode is suitable for real-time preview streams.

---

## 2. Detailed Results by Noise Level

### Noise Density: 20%
*   **Quality Mode**: PSNR 39.84 dB | Time 2.1s
*   **Speed Mode**: PSNR 37.12 dB | Time 0.4s

### Noise Density: 60%
*   **Quality Mode**: PSNR 31.19 dB | Time 6.5s
*   **Speed Mode**: PSNR 28.50 dB | Time 1.1s

---

## 3. Adaptive Selector Accuracy

The `AdaptiveModeSelector` correctly identified the optimal mode in **85%** of test cases:
*   Correctly switched to **Speed Mode** for high-noise (>50%), low-texture images.
*   Correctly switched to **Quality Mode** for low-noise, high-texture images.
