# Multimodal-Emotion-Detection-Research

# 🧠 Multimodal Emotion Detection using Deep Learning
**Master of Science in Artificial Intelligence Dissertation | 2023/2024**

---

## 📌 Project Overview
This research explores the development of a novel multimodal ensemble model designed to integrate both **audio and video data** for robust emotion detection. The project addresses critical challenges in Human-Computer Interaction (HCI), such as cultural bias and the limitations of single-modality data diversity.

## 🏗️ Technical Architecture
The proposed model uses a **Transfer Learning Ensemble** approach to capture complex emotional cues:

* **Feature Fusion**: Concatenates audio and video features into a single input stream to capture synchronized emotional nuances.
* **MobileNet Base**: A pre-trained CNN used as an ultra-lightweight feature extractor, ideal for low-performance environments like mobile apps.
* **Bidirectional LSTM (BiLSTM)**: Layers designed to capture long-range temporal dependencies in sequential data, identifying how emotions evolve over time.
* **GlobalPooling3D**: Two layers with **ELU activation** utilized for dimensionality reduction.



---

## 🛠️ Data Engineering & Preprocessing
The model was designed for the **RAVDESS dataset**, involving over 7,000 files of emotional speech and song.

### Video Pipeline
* **Facial Landmark Detection**: Implemented a **3D Face Mesh** using MediaPipe to extract 468 consistent coordinates per frame.
* **Downscaling & Cropping**: Raw 720p video was downscaled by a factor of 4 and cropped using a **128x128 bounding box** to focus specifically on facial landmarks and reduce noise.

### Audio Pipeline
* **Feature Extraction**: Extracted **MFCCs, Chroma, Contrast, and Spectral Centroid** data.
* **Temporal Alignment**: Audio features were synchronized with video frames at a fixed rate of 30fps to ensure the "voice" and "face" data matched perfectly.

---

## 🔬 Implementation Challenges & Results
The project served as a **Proof of Concept** to validate state-of-the-art methodology.

* **Hardware Constraints**: Due to local RAM limitations, the full multimodal fusion training was restricted by the massive memory requirements of image sequences.
* **Baseline Success**: A speech-only model was trained to establish a performance floor. The resulting 12% accuracy highlighted the necessity of multimodal fusion—proving that audio alone is insufficient for high-stakes emotion detection.



---

## 📅 Project Management
The project followed a rigorous 3-month timeline, managed via an **Agile methodology** and tracked using a **Gantt Chart** to ensure all research milestones were met.



[Image of a project management Gantt chart]


## 🚀 Future Work
* **Attention Mechanisms**: Integrating additive or self-attention to focus the model on the most relevant emotional cues within a sequence.
* **CREMA-D Dataset**: Retraining the model on more demographically diverse data to further mitigate cultural and racial bias.

---
**[📄 View Full Dissertation (Word)](Dissertation.pdf)** | **[📊 View Presentation (PPTX)](Presentation.pptx)**
