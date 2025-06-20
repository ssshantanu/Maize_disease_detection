# 🌽 Maize-disease-classifier

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ssshantanu/Maize-disease-classifier/blob/main/maize_classifier.ipynb)
![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

---

## 🌟 Overview

Maize (corn) is one of the most vital crops globally, and its productivity can be seriously impacted by leaf diseases. **Maize-disease-classifier** is a deep learning model built using PyTorch and ResNet18 that identifies and classifies maize leaf conditions into four categories:

-  Gray Leaf Spot  
-  Common Rust  
-  Blight  
-  Healthy  

This model empowers farmers, agronomists, and agricultural tech platforms to identify diseases early, enabling timely interventions and healthier crop yields.

---

## 🖼️ Dataset

- **Source:** [Corn/Maize Leaf Disease Dataset](https://www.kaggle.com/datasets/smaranjitghose/corn-or-maize-leaf-disease-dataset)
- **Classes:**
  - `Blight`
  - `Common_Rust`
  - `Gray_Leaf_Spot`
  - `Healthy`
- Images were preprocessed (resized, normalized) and split into training and validation sets using a 90:10 ratio.

---

## 🧠 Model Architecture

- **Base Model:** `ResNet18` (pretrained on ImageNet)
- **Modification:** Final fully connected layer adapted to classify 4 disease categories.
- **Loss Function:** CrossEntropyLoss  
- **Optimizer:** Adam with learning rate = 0.0001  
- **Training Epochs:** 6

---

## 📈 Results

| Metric        | Accuracy |
|---------------|----------|
| Training      | 99%      |
| Validation    | 96%      |

> 📊 Training and validation performance was plotted for insights. You can find the training curve inside the notebook.

---

## 🚀 How to Use

### 🔧 Installation

```bash
git clone https://github.com/ssshantanu/Maize-disease-classifier.git
cd Maize-disease-classifier
pip install -r requirements.txt


### 🔍 Inference Example

```python
from PIL import Image
img = Image.open("path_to_leaf_image.jpg")
predicted_label = predict_image(img, model, transform, device)
print(predicted_label)

## 🌾 Use Cases

- Mobile crop disease detection apps  
- Smart farming advisory systems  
- Integration with drone or camera-based monitoring tools  
- Helping agronomists with large-scale crop monitoring

---

## 🔮 Future Work

- ✅ Add real-time camera prediction interface  
- 📲 Convert model to TensorFlow Lite or ONNX for mobile/edge devices  
- 🌱 Train on more diverse crop datasets  
- 🛰️ Integrate with satellite/drone image inputs

---

## 🛠️ Tech Stack

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)  
![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)  
![Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=googlecolab&logoColor=white)  
![Matplotlib](https://img.shields.io/badge/Matplotlib-3776AB?logo=python&logoColor=white)  
![Seaborn](https://img.shields.io/badge/Seaborn-0769AD?logo=python&logoColor=white)

---

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit a pull request to improve the project.

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 📬 Contact

**Author:** Shantanu Dubey  
**GitHub:** [@ssshantanu](https://github.com/ssshantanu)

---

> 🌽 *“Detecting diseases early is like vaccinating the crop—let's bring AI into agriculture.”*

