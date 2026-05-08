# ITAI1378_Midterm_TradeVision
# TradeVision: Automated Chart Pattern Detection 

**Team Members:** Angelo Ochoa
**Course:** ITAI 1378: Computer Vision and AI  
**Tier Selection:** Tier 2. We are taking an established object detection architecture (YOLOv8) and applying it to a non-traditional computer vision domain (financial chart images) to solve a quantitative analysis problem.

## Problem Statement
Traders spend countless hours manually scanning daily stock charts to identify technical trading patterns. This process is slow, tedious, and subject to emotional bias, causing traders to miss setups or make costly mistakes.

## Solution Overview
TradeVision automates technical analysis using computer vision. By feeding candlestick chart images into our system, the model detects and draws bounding boxes around high-probability technical patterns (like Bull Flags or Double Tops), generating a list of actionable alerts.

## Technical Approach
* **Technique:** Object Detection
* **Model:** YOLOv8
* **Framework:** PyTorch, Ultralytics, mplfinance (for rendering charts)

## Dataset Plan
* **Source:** Kaggle (Stock Market Candlestick Image Dataset) / Custom generation via `yfinance`.
* **Size:** ~5,000 images
* **Labels:** Bounding boxes ("Bull_Flag", "Double_Top", "Head_and_Shoulders")

## Metrics
* **Primary Metric:** Precision > 90% (Crucial to minimize false signals in trading).
* **Secondary Metric:** Inference speed > 50 charts per second.

## Week-by-Week Plan
* **Week 10:** Secure dataset and set up environment.
* **Week 11:** Train baseline YOLO model.
* **Week 12:** Tune hyperparameters to maximize precision.
* **Week 13:** Create visual inference demo.
* **Week 14:** Final testing and GitHub documentation.
* **Week 15:** Presentation.

## Resources Needed
* **Compute:** Google Colab / Local GPU
* **Cost:** $0
* **APIs:** Yahoo Finance (yfinance) for live testing.

## Risks & Mitigation
| Risk | Probability | Mitigation |
| False Positives (Bad signals) | High | Set a strict confidence threshold (e.g., > 0.85) for inference. |
| Lack of diverse data | Medium | Apply image augmentation (scaling, aspect ratio changes). |

