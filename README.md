## 🧠 Model Architecture

| Layer | Type | Output Shape | Parameters |
|------|------|-------------|-----------|
| conv2d | Conv2D | (None,150,150,32) | 896 |
| max_pooling2d | MaxPooling2D | (None,75,75,32) | 0 |
| conv2d_1 | Conv2D | (None,75,75,64) | 18,496 |
| max_pooling2d_1 | MaxPooling2D | (None,37,37,64) | 0 |
| flatten | Flatten | (None,87616) | 0 |
| dense | Dense | (None,128) | 11,214,976 |
| dropout | Dropout | (None,128) | 0 |
| dense_1 | Dense | (None,128) | 16,512 |
| dense_2 | Dense | (None,15) | 1,935 |

**Total Parameters:** 11,252,815


---

## 📁 Project Structure

```bash
Greenclassify/
├── flask/
│   ├── app.py
│   ├── vegetable_classification.h5
│   ├── static/
│   │   ├── css/style.css
│   │   ├── js/main.js
│   │   └── img/
│   ├── templates/
│   │   ├── index.html
│   │   ├── prediction.html
│   │   └── logout.html
│   └── uploads/
├── notebooks/
│   └── vegetable_classification_training.ipynb
├── requirements.txt
├── README.md
└── LICENSE
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Anaconda Navigator (recommended)
- TensorFlow 2.10+

---

### Installation

```bash
git clone https://github.com/your-username/repository-name.git
cd Greenclassify

python -m venv venv
source venv/bin/activate
# Windows
venv\Scripts\activate

pip install -r requirements.txt
```

---

### Dataset Download

```bash
kaggle datasets download -d misrakahmed/vegetable-image-dataset
```

---

### Run Application

```bash
cd flask
python app.py
```

Open browser:

```
http://127.0.0.1:5000
```
