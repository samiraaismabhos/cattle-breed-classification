# 🐄 Cattle Breed Classification Using CNNs  

A Comparative Study of **ResNet18** and **VGG16** with Transfer Learning.

---

## 🔍 Project Overview
This project focuses on multi-class classification of **50 cattle breeds** using deep learning.  
I compare two CNN architectures (**ResNet18** and **VGG16**) and two optimizers (**SGD** and **Adam**),  
and also evaluate training **from scratch vs. transfer learning**.

- Framework: **PyTorch**  
- Environment: **Google Colab (GPU)**  
- Tools: TensorBoard, Jupyter Notebook

---

## 📂 Dataset
- 50 cattle breeds  
- 5949 training images  
- 1254 validation images  
- 1328 test images  
- All resized to **224×224**, normalized with ImageNet mean/std  
- Augmentation: random horizontal flip, random rotation (±15°)

---

## 🧠 Models
- **ResNet18 (Transfer Learning)** – ImageNet pretrained, last layer changed to 50 classes  
- **ResNet18 (Scratch)** – same architecture, random init  
- **VGG16 (Transfer Learning)** – pretrained feature extractor, fine-tuned classifier

Optimizers:
- SGD (lr=0.001, momentum=0.9)  
- Adam (lr=0.0005)

---

## 📊 Results

| Model     | Pretrained | Optimizer | Test Accuracy | Macro F1 |
|----------|-----------|-----------|---------------|----------|
| ResNet18 | Yes       | SGD       | **0.5813**    | **0.5319** |
| ResNet18 | Yes       | Adam      | 0.4902        | 0.4455 |
| ResNet18 | No        | SGD       | 0.1762        | 0.0991 |
| VGG16    | Yes       | SGD       | 0.4495        | 0.3820 |
| VGG16    | Yes       | Adam      | 0.3742        | 0.3560 |

➡ **Best model:** ResNet18 (Transfer Learning) + SGD

---

## 📈 Monitoring with TensorBoard
- Tracked training & validation **accuracy** and **loss**  
- Observed faster convergence with Adam but better generalization with SGD  
- Analysed overfitting behaviour for each architecture

---

## 🧾 Repository Structure (example)
- `notebooks/` – training & evaluation notebook  
- `models/` – saved `.pth` weights  
- `reports/` – project PDF + presentation  
- `src/` – training scripts (train, eval, dataset utils)

---

## 🎯 What I Learned
- Transfer learning is essential for small image datasets  
- Residual connections (ResNet18) make optimization easier than VGG16  
- How to use TensorBoard for debugging and understanding model behaviour

---

## 📬 Contact
If you’d like to discuss this project:  
📧 **samiraaismabhos@gmail.com**
