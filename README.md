\# ## DeepShield — Deepfake Detection System
A multi-model ensemble deepfake detection system built using **React + FastAPI + Vision Transformers (ViT)**.
DeepShield allows users to upload an image and uses **five specialized AI models** to analyze whether the image is **real or AI-generated (fake)**. Instead of relying on a single detector, the system uses an **ensemble voting approach**, improving reliability and reducing false predictions.

##  Problem Statement
With the rapid rise of AI-generated images and manipulated media, detecting deepfakes has become increasingly important for digital safety, journalism, cybersecurity, and trust verification.
Traditional single-model detectors often fail when exposed to unseen or advanced fake content.
DeepShield solves this by combining multiple expert models, where each model specializes in detecting different types of deepfakes

##  Features
* Upload image for instant deepfake analysis
* 5-model ensemble detection system
* Majority voting mechanism for final prediction
* Specialized models for different fake-generation techniques
* FastAPI backend for model inference
* React frontend for smooth user interaction
* Real-time prediction results

##  Models Used
### 1. Haywoodsloan
**SwinV2-based Generalist Detector**
* Strong general-purpose detector
* Good performance across multiple fake types

### 2. Organika
**SDXL / Flux Specialist**
* Specialized in detecting AI-generated images from SDXL and Flux models

### 3. Wvolf
**Vision Transformer (ViT)**
* High-performance detector
* Reported accuracy: **98.7%**

### 4. PrithivMLmods v2
**ViT-based Detector**
* Strong balanced detection performance
* Reported F1 Score: **92.12%**

### 5. Heem2
**Low False-Positive Specialist**
* Designed to reduce incorrect fake detection
* Helps improve trust in final prediction

##  Tech Stack
### Frontend
* React.js
* Vite
* JavaScript
* CSS

### Backend
* FastAPI
* Python
* Uvicorn

### AI / ML
* Hugging Face Models
* Vision Transformers (ViT)
* SwinV2
* Ensemble Voting System

##  Working Flow
1. User uploads an image
2. Backend sends the image to all 5 models
3. Each model predicts Real or Fake
4. Final result is decided using majority voting
5. Frontend displays prediction instantly

## How to Run
## Backend
```bash
pip install -r requirements.txt
uvicorn backend:app --reload --port 8000
```
## Frontend
```bash
cd frontend
npm install
npm run dev
```
Open:
http://localhost:5173
We can also view the frontend at "deepshield-three.vercel.app"
(working on deployin the backend here too)
## Future Improvements

* Video deepfake detection
* Audio deepfake detection
* Confidence score visualization
* Model explainability dashboard
* Admin analytics panel
* Deployment on cloud for public use

##  Conclusion

DeepShield improves deepfake detection reliability using a multi-model ensemble approach rather than depending on a single detector.
This makes the system more robust, accurate, and practical for real-world fake media detection.

