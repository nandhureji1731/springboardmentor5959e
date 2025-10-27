# springboardmentor5959e
# 🛢️ AI SpillGuard – Oil Spill Detection using Deep Learning (U-Net, Streamlit + Flask + Pyngrok)

An AI-powered environmental monitoring project developed under the **Infosys Springboard Internship Program (AI & ML Track)**.  
This system detects and segments **oil spill regions** in satellite images using **U-Net deep learning architecture**, with a user-friendly interface built using **Streamlit** and a backend powered by **Flask**.  
The complete app is hosted via **Pyngrok** for real-time web access directly from Google Colab.

---

## 🚀 Project Overview

Oil spills are one of the most destructive marine disasters, affecting aquatic life and ecosystems.  
This project leverages **Artificial Intelligence** to automate oil spill detection from satellite imagery through **semantic segmentation**.

The model:
- Is trained on the **Zenodo Oil Spill Dataset (2024)**
- Achieves **94% segmentation accuracy**
- Integrates **Streamlit + Flask + Pyngrok** for real-time demo deployment

---

## 📂 Repository Structure

├── app.py # Flask backend for model inference
├── streamlit_app.py # Streamlit user interface
├── oil_spill_detection.ipynb # Google Colab notebook (training & evaluation)
├── oil_spill_model.keras # Trained U-Net model
├── requirements.txt # Required dependencies
├── README.md # Project documentation (this file)
└── screenshots/ # Folder containing project screenshots


---

## 🧩 Key Features

- 🧠 **Deep Learning Segmentation** using U-Net architecture  
- 📊 Achieved **>93% pixel-level accuracy**  
- 🌐 **Streamlit UI** for interactive prediction visualization  
- ⚙️ **Flask Backend** serving TensorFlow model predictions  
- ☁️ **Pyngrok Integration** for public access via Google Colab  
- 🖼️ Generates red-highlighted overlays of oil spill regions  

---

## 🧰 Tech Stack

| Category | Tools / Frameworks |
|-----------|-------------------|
| Language | Python |
| Deep Learning | TensorFlow, Keras |Unet
| Image Processing | OpenCV, Pillow, NumPy |
| Web Interface | Streamlit |
| Backend | Flask |
| Deployment | Pyngrok |
| Platform | Google Colab |

---

## 🧮 Model Workflow

1️⃣ **Dataset Loading** – Satellite images + binary masks from Zenodo  
2️⃣ **Preprocessing** – Resize (128×128), normalization, augmentation  
3️⃣ **Model Building** – U-Net encoder-decoder structure  
4️⃣ **Training** – Optimized using Adam, Dice Loss + Binary Crossentropy  
5️⃣ **Evaluation** – Accuracy, IoU, and Dice metrics  
6️⃣ **Deployment** – Flask + Streamlit integrated with Pyngrok  

---

## 📊 Model Results

| Metric | Value |
|---------|-------|
| Accuracy | 94.1% |
| Dice Coefficient | 0.92 |
| IoU Score | 0.90 |
| Loss | 0.17 |

The model produces accurate segmentation masks that effectively highlight oil spill zones across different water surfaces.

📷 *Predicted overlays highlight detected oil spill regions in red.*

---

## 🌍 Deployment Instructions

### 🧱 Local Setup
```bash
# Install dependencies
pip install -r requirements.txt

# Start Flask backend
python app.py

# Start Streamlit interface
streamlit run streamlit_app.py

🎯 Learning Outcomes

Hands-on experience in deep learning image segmentation

Understanding of U-Net architecture

Real-time app deployment using Flask + Streamlit + Pyngrok

Integration of backend AI model with frontend visualization

Practical exposure to MLOps-style end-to-end workflow

🧾 References

Zenodo Oil Spill Dataset (2024)

Ronneberger et al., U-Net: Convolutional Networks for Biomedical Image Segmentation, MICCAI 2015

TensorFlow and Keras Documentation

Streamlit Documentation

Pyngrok & Flask Official Docs


🤝 Author

Developed by: Nandhu

📫 Infosys Springboard AI/ML Internship – 2025
💬 “Empowering sustainability through intelligent AI-driven detection.”

### requirements.txt*

# Core Machine Learning & Deep Learning
tensorflow==2.16.1
keras==3.3.3
numpy==1.26.4
pandas==2.2.2

# Image Processing & Visualization
opencv-python==4.10.0.84
Pillow==10.3.0
matplotlib==3.9.0

# Web Frameworks
flask==3.0.3
streamlit==1.38.0

# Tunneling & Deployment
pyngrok==7.2.0

# Utilities
scikit-learn==1.5.2
tqdm==4.66.4
requests==2.32.3

# Optional (safety for Colab + TensorFlow GPU)
protobuf==4.25.3
h5py==3.11.0


