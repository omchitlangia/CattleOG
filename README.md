# AI-Powered Cattle & Buffalo Breed Recognition

An end-to-end solution for automated breed identification of Indian cattle and buffaloes using deep learning (transfer learning with VGG16) and an intuitive Streamlit web app. Designed for use by field-level workers, dairy researchers, and integration with platforms like Bharat Pashudhan App.

#  Features

Transfer Learning with VGG16: Efficient breed classification from limited images per class

Streamlit Web App: Upload cattle/buffalo photos, get instant breed predictions and confidence scores

Metadata Integration: Displays breed origin, milk yield, and physical traits

Batch Processing & CSV Export: Upload multiple images, export results

Fallback API Integration: Roboflow model inference for rapid demo/testing

Automated Testing: Validate key functions and ensure reliability

User Guide & Documentation: For easy adoption by field staff or non-technical users

# 📋 Setup Instructions

1. Clone the repository

``` sh
bash
git clone https://github.com/yourusername/cattle-breed-ai.git
cd cattle-breed-ai
```
2. Install dependencies

```sh
bash
pip install -r requirements.txt
Dataset Preparation
```

3. Download your dataset ZIP (Kaggle/web-scraped) and extract to data/cattle-breeds-dataset/

Ensure images are in breed-labeled subfolders inside train/ and validation/

4. Model Training

```sh
bash
python train.py
# Model will be saved as cattle_breed_classifier.h5
```

5. Run the Streamlit App

```sh
bash
streamlit run app.py
```

6. (Optional) Run API Fallback

Add your Roboflow API key to roboflow_predict.py for instant predictions


# 🐂 Supported Breeds
Gir, Sahiwal, Red Sindhi, Tharparkar, Kankrej, Ongole, Hariana

Murrah, Surti, Jaffarabadi, Mehsana, Nagpuri, Bhadawari, Nili Ravi

(Exotic/Crossbreed support possible; extend as needed!)

# 💡 How it Works
1. Image Upload: Field worker uploads photo via web app

2. Prediction Pipeline:

  Image is preprocessed and passed to CNN
  Model returns predicted breed (+ confidence score)
  Breed metadata is displayed for verification

3. Batch Workflow: Upload multiple images and export full result as CSV

# 📈 Results & Accuracy

Typical accuracy: 85–95% (varies by dataset, augmentation)
Results visualized in accuracy.png and loss.png





