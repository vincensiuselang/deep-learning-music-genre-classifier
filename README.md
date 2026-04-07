# 🎧 Music Genre Classification (Deep Learning)

## 📌 Overview

Project ini bertujuan untuk melakukan klasifikasi genre musik
menggunakan Deep Learning dengan arsitektur ResNet18 (transfer
learning).

Dataset berupa audio yang sudah diubah menjadi representasi gambar
(spectrogram), lalu diproses sebagai image classification.

------------------------------------------------------------------------

## 🚀 Features

-   Exploratory Data Analysis (EDA)
-   Data cleaning & validation
-   Stratified train-validation split
-   Data augmentation
-   Transfer learning (ResNet18 pretrained)
-   Early stopping untuk mencegah overfitting
-   Evaluation lengkap (Accuracy, Classification Report, Confusion
    Matrix)
-   Visualisasi learning curve
-   Inference dari folder gambar

------------------------------------------------------------------------

## 🗂️ Dataset Structure

DataTrain/ ├── blues/ ├── classical/ ├── jazz/ ├── rock/ └── ...

------------------------------------------------------------------------

## ⚙️ Tech Stack

-   Python
-   PyTorch
-   Torchvision
-   Scikit-learn
-   Matplotlib
-   PIL

------------------------------------------------------------------------

## 🧠 Model Architecture

Model menggunakan ResNet18 pretrained dengan modifikasi:

model.fc = nn.Sequential( nn.Linear(model.fc.in_features, 256),
nn.ReLU(), nn.Dropout(0.5), nn.Linear(256, num_classes) )

------------------------------------------------------------------------

## 🔄 Training Strategy

-   Optimizer: Adam
-   Learning rate: 1e-4
-   Loss: CrossEntropyLoss
-   Epoch: 15
-   Early stopping (patience=3)

------------------------------------------------------------------------

## 📊 Data Augmentation

Training: - Resize (224x224) - Random Horizontal Flip - Random Rotation

Validation: - Resize only

------------------------------------------------------------------------

## 📈 Evaluation Metrics

-   Accuracy
-   Precision, Recall, F1-score
-   Confusion Matrix

------------------------------------------------------------------------

## 🔮 Inference

predict_folder(model, folder, device, class_names)

------------------------------------------------------------------------

## 💾 Model Saving

torch.save(model.state_dict(), "../models/model_music_genre.pth")

------------------------------------------------------------------------

## ⚠️ Limitations

-   Hanya berbasis spectrogram image
-   Belum hyperparameter tuning
-   Belum deploy

------------------------------------------------------------------------

## 🔥 Future Improvements

-   Mel spectrogram optimization
-   Fine-tuning lebih dalam
-   Model lebih advanced (EfficientNet, ViT)
-   Deploy ke web (Streamlit/FastAPI)
-   Explainability (Grad-CAM)

------------------------------------------------------------------------

## 🧑‍💻 Author

Vincen -- AI Enthusiast
