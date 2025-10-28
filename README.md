 Smart Waste Classification & Carbon Emission Estimation
   Overview

This project uses Deep Learning (MobileNetV2) and Streamlit to classify different types of waste (Hazardous, Recyclable, Organic, and Non-Recyclable).
It also estimates the carbon emissions saved if the waste is properly managed or recycled — supporting environmental sustainability goals.

  Objectives

Automatically classify waste images into categories using CNN (MobileNetV2).

Provide estimated CO₂ emissions saved per item based on waste type.

Offer an easy-to-use Streamlit web interface for uploading images.

Raise awareness of sustainable waste disposal and recycling.

  Features

✅ Image classification using MobileNetV2 (Transfer Learning)
✅ Displays predicted category and CO₂ savings (kg/item)
✅ Built-in Carbon Emission Mapping CSV
✅ Simple and interactive Streamlit dashboard
✅ Real-time prediction using uploaded waste images

  Project Structure
📦 SmartWasteClassifier
│
├── waste_flat/                     # Flattened dataset (organized by subfolders)
├── waste_classifier_cnn_improved.h5 # Trained MobileNetV2 model
├── carbon_mapping.csv               # Category-to-CO₂ mapping data
├── app.py                           # Streamlit app code
├── requirements.txt                 # All dependencies
└── README.md                        # Project documentation

 Dataset

The dataset includes four main categories:

Hazardous Waste (batteries, e-waste, paints, pesticides)

Recyclable Waste (paper, cans, glass, plastics)

Non-Recyclable Waste (diapers, sanitary napkins, styrofoam)

Organic Waste (food scraps, coffee/tea bags, yard trimmings)

All images were stored under /content/waste_flat/ and used to train the CNN.

  Model

Base Model: MobileNetV2 (pretrained on ImageNet)

Fine-tuned on custom waste dataset

Optimizer: Adam

Loss: Categorical Crossentropy

Metrics: Accuracy

Epochs: 10

Achieved accuracy: ~85–90% (depending on dataset quality)

  Sustainability Impact

By classifying waste and estimating CO₂ savings, this solution:

Encourages recycling and proper waste segregation

Helps reduce landfill emissions

Promotes data-driven sustainability initiatives

  Deployment

In Google Colab, use pyngrok to expose the Streamlit app publicly:

from pyngrok import ngrok
public_url = ngrok.connect(8501)
print(f"🌍 App Live at: {public_url.public_url}")

 Future Improvements

Improve accuracy with more training data

Add support for real-time camera input

Deploy on Streamlit Cloud or Hugging Face Spaces

Integrate with government or NGO recycling APIs

  References

TensorFlow Documentation: https://www.tensorflow.org/

Streamlit Documentation: https://docs.streamlit.io/

MobileNetV2 Paper: Sandler et al., 2018

Dataset: Custom waste image dataset from Google & Kaggle resources

  Contributors

  Priyalakshmi R
  Dharshini S
  Sivasoruba B

Anna University Regional Campus Madurai / CSE Department 