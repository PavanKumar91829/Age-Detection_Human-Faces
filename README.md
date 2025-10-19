# Age Detection Using CNN & Transfer Learning (ResNet18)

This project implements an **Age Class Detection System** that predicts the **age range (18–60 years)** of a person based on their face image.  
It uses **Convolutional Neural Networks (CNNs)** and **Transfer Learning with ResNet18** for efficient age group classification.

🔗 **GitHub Repository:** [PavanKumar91829/Age-Detection_Human-Faces](https://github.com/PavanKumar91829/Age-Detection_Human-Faces)

---

## 📂 Dataset

**Source:** [Kaggle – Age Detection: Human Faces (18–60 years)](https://www.kaggle.com/datasets/trainingdatapro/age-detection-human-faces-18-60-years)

The dataset contains labeled human face images grouped by different age ranges between 18 and 60 years.  
Each folder represents an age group (e.g., `18-25`, `26-35`, etc.).

> ⚠️ **Note:** The dataset used in this project contains only around **150 images** for training and testing combined.  
> As a result, the **model accuracy is relatively low** due to limited training data.  
> Increasing the dataset size or applying data augmentation techniques can **significantly improve performance**.

**Dataset structure:**
```
dataset/
│
├── train/
│   ├── 18-25/
│   ├── 26-35/
│   ├── 36-45/
│   ├── 46-60/
│
└── test/
    ├── 18-25/
    ├── 26-35/
    ├── 36-45/
    ├── 46-60/
```

---

## 🧰 Project Structure

```
AgeDetection_CNN/
│
├── AgeDetection_CNN.ipynb    # Main Jupyter Notebook              
└── README.md     # Project documentation       
```

---

## 🚀 Features

- **Transfer Learning** with pre-trained ResNet18  
- **Data Augmentation** using PyTorch’s `transforms`  
- **GPU acceleration** (CUDA compatible)  
- **Cross-entropy loss** and **Adam optimizer**  
- **Model performance visualization** (accuracy/loss curves)  

---

## ⚙️ Installation

Clone the repository:
```bash
git clone https://github.com/PavanKumar91829/Age-Detection_Human-Faces.git
cd Age-Detection_Human-Faces
```

Install dependencies:
```bash
pip install -r requirements.txt
```

If `requirements.txt` is not available, install manually:
```bash
pip install torch torchvision matplotlib numpy
```

---

## 📘 Usage

1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/trainingdatapro/age-detection-human-faces-18-60-years).
2. Extract it into a folder named `dataset/`.
3. Open the notebook:
   ```bash
   jupyter notebook AgeDetection_CNN.ipynb
   ```
4. Run all cells to:
   - Preprocess and transform images  
   - Load and train the ResNet18 model  
   - Evaluate accuracy and visualize metrics  

---

## 🧩 Model Details

- **Base Model:** ResNet18 (pre-trained on ImageNet)  
- **Modified Layers:** Final fully connected (FC) layer replaced to match number of age classes  
- **Loss Function:** CrossEntropyLoss  
- **Optimizer:** Adam  
- **Learning Rate:** 0.001  
- **Batch Size:** 32  
- **Epochs:** 10–25 (configurable)  

---

## 📊 Results

Due to the **small dataset size (≈150 images)**, the model achieves **limited accuracy**.  
However, the results demonstrate that the **ResNet18 architecture can generalize age-based facial features** when trained on larger datasets.

---

## 🧠 Future Improvements

- Increase dataset size (more face samples per class)  
- Apply advanced **data augmentation** (rotation, cropping, brightness, etc.)  
- Experiment with deeper architectures (ResNet50, EfficientNet)  
- Implement **age regression** instead of classification  
- Hyperparameter tuning (learning rate, batch size)  
- Deploy as a **web or mobile app** for real-time age detection  

---

## 🏅 Acknowledgements

- Dataset provided by [TrainingDataPro on Kaggle](https://www.kaggle.com/datasets/trainingdatapro/age-detection-human-faces-18-60-years)  
- Model architecture inspired by [ResNet: Deep Residual Learning for Image Recognition (He et al., 2015)](https://arxiv.org/abs/1512.03385)

---

## 📄 License

This project is open-source under the [MIT License](LICENSE).
