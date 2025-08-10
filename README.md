# 🌸 Flower GAN – Generate Realistic Flower Images with Deep Learning

## 📌 Project Overview

This project uses a **Generative Adversarial Network (GAN)** to generate realistic flower images from scratch, trained on the **Flower Color Images** dataset from Kaggle.
The GAN consists of:

* **Generator** – Creates new images from random noise.
* **Discriminator** – Distinguishes between real and generated images.

By training both networks together, the Generator learns to produce increasingly realistic flowers over time.

---

## 📂 Dataset

**Source:** https://www.kaggle.com/datasets/olgabelitskaya/flower-color-images

* **Total Images:** Multiple categories of flowers
* **Format:** PNG
* **Preprocessing:** Resizing to 64×64 pixels and normalizing to \[-1, 1]

---

## 🛠 Technologies Used

* **Python**
* **TensorFlow / Keras**
* **NumPy, OpenCV**
* **Matplotlib**
* **Google Colab**
* **Kaggle API**

---

## 🚀 How to Run

### 1️⃣ Download Dataset

```python
from google.colab import files
files.upload()  # Upload kaggle.json API key

!mkdir -p ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json
!kaggle datasets download -d olgabelitskaya/flower-color-images
!unzip -q flower-color-images.zip -d flower_data
```

### 2️⃣ Preprocess Images

* Resize to 64×64
* Convert BGR → RGB
* Normalize pixel values to \[-1, 1]

### 3️⃣ Train GAN

```python
EPOCHS = 500
train(train_dataset, EPOCHS)
```

### 4️⃣ View Generated Images

```python
show_random_generated_image()
show_image_at_epoch(500)
```

---

## 📊 Training Process

* **Batch Size:** 32
* **Noise Vector Size:** 100
* **Optimizer:** Adam (learning rate 0.0001)
* **Loss Function:** Binary Cross-Entropy

---

## 📈 Future Improvements

* Train for more epochs with higher resolution images.
* Experiment with **DCGAN** and **StyleGAN** architectures.
* Add color/style conditioning for specific flower types.

---

## 📜 License

This project is licensed under the MIT License.

