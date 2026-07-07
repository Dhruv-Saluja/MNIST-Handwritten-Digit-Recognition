# MNIST Digit Classification

A simple neural network built with TensorFlow / Keras to classify handwritten digits from the MNIST dataset.

## 📌 Overview

This project trains a fully-connected (dense) neural network on the classic MNIST handwritten digit dataset and evaluates it on the test set.

- **Framework:** TensorFlow / Keras
- **Dataset:** MNIST (60,000 training images, 10,000 test images, 28×28 grayscale digits)
- **Task:** 10-class image classification (digits 0–9)
- **Final test accuracy:** ~0.9706

## 🧠 Model Architecture

A `Sequential` Keras model with the following layers:

| Layer  | Type    | Output Shape | Parameters |
|--------|---------|--------------|------------|
| 1      | Flatten | (None, 784)  | 0          |
| 2      | Dense   | (None, 157)  | 123,245    |
| 3      | Dense   | (None, 32)   | 5,056      |
| 4      | Dense   | (None, 10)   | 330        |

- **Total params:** 128,631
- **Activation (hidden):** ReLU
- **Activation (output):** Softmax
- **Loss:** `sparse_categorical_crossentropy`
- **Optimizer:** Adam
- **Epochs:** 15

## 📂 Project Structure

```
MNST/
├── mnst.ipynb        # Main notebook — data loading, training & evaluation
├── README.md         # Project documentation
├── requirements.txt  # Python dependencies
├── .gitignore        # Files to ignore in Git
└── LICENSE           # MIT License
```

## ⚙️ Setup

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd MNST
   ```

2. (Optional) Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Launch Jupyter Notebook and open `mnst.ipynb`:
   ```bash
   jupyter notebook
   ```

## 📈 Results

After 15 epochs of training, the model achieves an accuracy of **~0.9706** on the MNIST test set.
