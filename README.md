# Multiclass Fish Image Classification

**Deep learning project to classify fish species from underwater images — end-to-end, from data preprocessing and augmentation to model training, evaluation, and deployment.**

`Automatically identify fish species (e.g., Tuna, Mackerel, Salmon, Catfish, Snapper) using convolutional neural networks and transfer learning — useful for marine biologists, fisheries management, and educational demos.`

---

## 🎯 Goal

The primary goal of this project is to **train a robust multiclass image classifier** that recognizes fish species from photos.  
This project demonstrates the complete lifecycle of a supervised deep learning application:

✅ Dataset preparation & augmentation  
✅ Transfer learning (MobileNetV2 / EfficientNet / ResNet)  
✅ Training with callbacks (early stopping, checkpointing, LR scheduling)  
✅ Evaluation using confusion matrix & classification report  
✅ Inference script for single-image prediction  
✅ Interactive Streamlit demo for testing the classifier  

---

## 📊 Dataset Insight

> Replace this with your dataset source (Kaggle, custom, etc.)

**Example Classes:**  
`Tuna`, `Salmon`, `Mackerel`, `Catfish`, `Snapper`, `Tilapia`, `Grouper`

| Split | Total Images | Classes | Avg Images/Class |
|-------|-------------:|:-------:|-----------------:|
| Train | 12,000       | 7       | ~1,700           |
| Val   | 2,000        | 7       | ~285             |
| Test  | 2,000        | 7       | ~285             |

---

## 🛠 Tech Stack

- [**Python**](https://www.python.org/) – Core programming language for data analysis and modeling  
- [**Pandas**](https://pandas.pydata.org/) – Data manipulation, cleaning, and wrangling  
- [**NumPy**](https://numpy.org/) – Numerical computations and preprocessing  
- [**TensorFlow / Keras**](https://www.tensorflow.org/) – CNNs & Transfer Learning  
- [**Albumentations**](https://albumentations.ai/) – Advanced data augmentation  
- [**scikit-learn**](https://scikit-learn.org/stable/) – Metrics & evaluation  
- [**Matplotlib / Seaborn**](https://matplotlib.org/) – Visualization  
- [**Streamlit**](https://streamlit.io/) – Interactive deployment demo  
- [**OpenCV / PIL**](https://opencv.org/) – Image processing  

---

**[`^🔝 Back to top^`](#Multiclass-Fish-Image-Classification
)**

## 🚀 Key Features

- **Transfer Learning** – MobileNetV2 / EfficientNetB0 for accurate and efficient classification  
- **Data Augmentation** – flips, rotations, brightness, blur, cutout  
- **Two-Phase Training** – freeze base → unfreeze top layers → fine-tune  
- **Callbacks** – early stopping, checkpoint saving, LR reduction  
- **Evaluation** – accuracy, precision, recall, F1, confusion matrix  
- **Misclassification Analysis** – visualize wrongly classified fish  
- **Inference** – predict top-3 species with probabilities  
- **Streamlit App** – drag & drop fish images for prediction  

---

## 📁 Project Structure

```bash
multiclass-fish-image-classification/
│
├── README.md
├── requirements.txt
├── LICENSE
├── .gitignore
│
├── data/
│   ├── train/
│   ├── val/
│   └── test/
│
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_training_pipeline.ipynb
│   └── 03_evaluation_and_errors.ipynb
│
├── src/
│   ├── data_loader.py
│   ├── model_builder.py
│   ├── train.py
│   ├── evaluate.py
│   ├── predict.py
│   └── utils.py
│
├── saved_models/
│   ├── fish_classifier.h5
│   └── label_encoder.pkl
│
├── streamlit_app/
│   ├── app.py
│   └── assets/
│
└── examples/
    ├── sample_1.jpg
    └── sample_2.jpg

```

**[`^🔝 Back to top^`](#🐟-Multiclass-Fish-Image-Classification)**

## ⚡ Quick Start  

### 1️⃣ Clone Repo  
```bash
git clone https://github.com/yourusername/multiclass-fish-image-classification.git
cd multiclass-fish-image-classification
```

2️⃣ Setup Environment
```bash
python -m venv venv
source venv/bin/activate   # macOS / Linux
venv\Scripts\activate.bat  # Windows

pip install -r requirements.txt
```
3️⃣ Prepare Dataset
```bash
data/train/<class>/*.jpg  
data/val/<class>/*.jpg  
data/test/<class>/*.jpg  
```
4️⃣ Train Model
```bash
python src/train.py \
  --data_dir data \
  --model_name mobilenet_v2 \
  --img_size 224 \
  --batch_size 32 \
  --epochs 15 \
  --output_dir saved_models
```
5️⃣ Evaluate
```bash
python src/evaluate.py --model saved_models/fish_classifier.h5 --data_dir data/test
```
6️⃣ Streamlit App
```bash
streamlit run streamlit_app/app.py
```
📦 requirements.txt
```
tensorflow>=2.9
numpy
pandas
matplotlib
seaborn
scikit-learn
opencv-python
pillow
albumentations
streamlit
joblib
```

**[`^🔝 Back to top^`](#🐟-Multiclass-Fish-Image-Classification)**

---
🙏 Acknowledgments

Built with ❤️ using TensorFlow, Albumentations, Streamlit, and open-source fish image datasets.

---

❓ FAQ

Q1: Can I train on CPU?
Yes — slower, but works. GPU recommended.

Q2: How many images per class are needed?
At least a few hundred, but transfer learning can work with fewer.

Q3: Can I use my own fish dataset?
Yes — replace data/train/ with your dataset.

Q4: Can this be extended to object detection?
This repo is classification-only. For detection, use YOLO/Detectron.

**[`^🔝 Back to top^`](#🐟-Multiclass-Fish-Image-Classification)**

```
Would you like me to also **add badges** (TensorFlow, Streamlit, Python, MIT License) at the top like a professional GitHub README?
```


**[`^🔝 Back to top^`](###-🎯-Goal)**

**[`^🔝 Back to top^`](#🐟-Multiclass-Fish-Image-Classification)**

**[`^        back to top        ^`](#-🐟-Multiclass-Fish-Image-Classification)**

**[`^🔝 Back to top^`](#Multiclass-Fish-Image-Classification)

**[`^        back to top        ^`](#Multiclass-Fish-Image-Classification)**
















