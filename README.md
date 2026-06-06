

---
title: Deepguard Ai Detector
emoji: 🐠
colorFrom: pink
colorTo: blue
sdk: gradio
sdk_version: 6.9.0
app_file: app.py
pinned: false
license: mit



---

Check out the configuration reference at https://huggingface.co/docs/hub/spaces-config-reference


# DeepGuard – AI Fake Image Detector

**Advanced AI-Generated Media Detection with Mimi Assistant**

DeepGuard is a free, publicly accessible web application that uses a deepfake model to detect AI-generated images. Upload a photo and instantly get a verdict **Real** or **Fake** along with confidence scores, forensic analysis, and an interactive emoji assistant named Mimi.

## Features

- **Deepfake Detection**: Powered by a custom model (`king1oo1/deepfake-model`)
- **Stable Test‑Time Augmentation**: Reduces false flips and improves reliability
- **Adversarial Robustness Check**: Detects potentially manipulated inputs
- **Confidence Calibration**: Converts raw scores to well‑calibrated probabilities
- **Input Protection**: Rejects QR codes, non‑face images, and random noise
- **Explainability**: Toggle an explanation of the model's decision (why the image was classified as real or fake)
- **Mimi's Corner**: A fun emoji assistant that reacts to your results and feedback
- **User Feedback Loop**: Rate predictions, leave written reviews, and help improve the model
- **Auto‑Clean Temporary Storage**: Images are automatically deleted after reset or new upload
- **Legal & Ethical Safeguards**: Clear terms of use, anonymized data handling, and opt‑out options

## Quick Start

1. Visit the live demo: [king1oo1/deepguard-ai-detector](https://king1oo1-deepguard-ai-detector.hf.space/)
2. Upload an image (JPG, PNG, WEBP) containing a face
3. Click ** Analyze **
4. View the verdict and confidence score
5. Optionally provide feedback or read the explanation

## How It Works

DeepGuard combines several AI and forensic techniques:
- A Vision Transformer (SigLIP2) trained on 500k+ images from 5 diverse datasets
- Test‑Time Augmentation for stable predictions
- Adversarial noise check
- Confidence calibration via Platt scaling
- Input validation using MTCNN face detection and QR code scanner

## Repository Structure

- `app.py` – Main Gradio application
- `requirements.txt` – Python dependencies
- `calibrator.pkl` – Confidence calibrator 
- `deepguard.db` – SQLite database (auto‑created)
- `data/temp/` – Temporary image storage (auto‑cleaned)
- `data/images/real/` and `data/images/fake/` – Permanent storage for feedback‑related images

## Ethical Use

DeepGuard is a **research prototype** intended for educational and verification purposes only. It is not a forensic‑grade tool. Predictions may be incorrect. Do not use DeepGuard to make legally binding decisions.
It is built by using [Gradio](https://gradio.app) and [Hugging Face Spaces](https://huggingface.co/spaces).


