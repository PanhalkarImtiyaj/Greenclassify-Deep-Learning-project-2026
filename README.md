Vegetable Image Classification
Deep Learning-Based Vegetable Image Classification
Python TensorFlow Flask License

📋 Project Overview
This deep learning-based web application accurately identifies and categorizes various types of vegetables using Convolutional Neural Networks (CNNs). The system analyzes input images of vegetables and classifies them into 15 predefined categories.

🎯 Key Features
Deep Learning Classification: CNN model trained on 15,000+ vegetable images

15 Vegetable Categories:
Bean, Bitter Gourd, Bottle Gourd, Brinjal, Broccoli, Cabbage, Capsicum, Carrot, Cauliflower, Cucumber, Papaya, Potato, Pumpkin, Radish, Tomato

Web Interface: User-friendly Flask-based web application

Real-time Prediction: Instant classification results

🏗️ Technical Architecture
User → UI (Upload Image) → Flask App → CNN Model → Prediction → Display Result

Model Architecture

Layer	Type	Output Shape	Parameters
conv2d	Conv2D	(None, 150, 150, 32)	896
max_pooling2d	MaxPooling2D	(None, 75, 75, 32)	0
conv2d_1	Conv2D	(None, 75, 75, 64)	18,496
max_pooling2d_1	MaxPooling2D	(None, 37, 37, 64)	0
flatten	Flatten	(None, 87616)	0
dense	Dense	(None, 128)	11,214,976
dropout	Dropout	(None, 128)	0
dense_1	Dense	(None, 128)	16,512
dense_2	Dense	(None, 15)	1,935

Total Parameters: 11,252,815

📁 Project Structure

Greenclassify/
├── flask/
│   ├── app.py                          # Flask application
│   ├── vegetable_classification.h5     # Trained model
│   ├── static/
│   │   ├── css/
│   │   │   └── style.css              # Stylesheets
│   │   ├── js/
│   │   │   └── main.js                # JavaScript
│   │   └── img/                       # Images
│   ├── templates/
│   │   ├── index.html                 # Home page
│   │   ├── prediction.html            # Prediction page
│   │   └── logout.html                # Result page
│   └── uploads/                       # Uploaded images
├── notebooks/
│   └── vegetable_classification_training.ipynb  # Training notebook
├── requirements.txt                    # Dependencies
├── README.md                          # Documentation
└── LICENSE                            # License file

🚀 Getting Started

Prerequisites
Python 3.8+
Anaconda Navigator (recommended)
TensorFlow 2.10+

Installation

Clone the repository
git clone https://github.com/your-username/repository-name.git
cd Greenclassify

Create a virtual environment
python -m venv venv
source venv/bin/activate
On Windows: venv\Scripts\activate

Install dependencies
pip install -r requirements.txt

Download the dataset (for training)
kaggle datasets download -d misrakahmed/vegetable-image-dataset

Run the Flask application
cd flask
python app.py

Open in browser
http://127.0.0.1:5000

📊 Dataset

The model is trained on the Vegetable Image Dataset from Kaggle:

Training Images: 15,000
Validation Images: 3,000
Test Images: 3,000
Categories: 15 vegetable types

🧠 Model Training

Open the Jupyter notebook:
jupyter notebook notebooks/vegetable_classification_training.ipynb

Follow the steps in the notebook:

Data Collection
Data Preprocessing
Model Building
Model Training
Model Evaluation
Save Model

🌐 Web Application Pages

Home Page (index.html): Landing page with project information
Prediction Page (prediction.html): Upload and classify vegetables
Result Page (logout.html): Display classification results

Usage

Navigate to the Prediction page
Click "Choose File" to select a vegetable image
Click "Submit" to classify
View the prediction result

📈 Use Cases

Automated Sorting: Vegetable processing facilities can automate sorting
Quality Control: Distributors can ensure consistent quality standards
Smart Inventory: Retail stores can manage vegetable inventory efficiently

🤝 Contributing

Fork the repository
Create your feature branch (git checkout -b feature/AmazingFeature)
Commit your changes (git commit -m 'Add some AmazingFeature')
Push to the branch (git push origin feature/AmazingFeature)
Open a Pull Request

👨‍💻 Author

Imtiyaj Panhalkar

📄 License

This project is licensed under the MIT License — see the LICENSE file for details.
