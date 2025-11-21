# image_captioning_project
This project implements an Image Caption Generation system that automatically produces meaningful, human-like captions for images using a deep learning pipeline combining InceptionV3, LSTM, and an Attention mechanism.
📂 Dataset Used

# Dataset: COCO 2017

Images Used: 1,000 (validation subset)

Captions per Image: 5 human-written captions

Annotations: captions_val2017.json

Purpose: Training + evaluating the caption-generation model

# 🧠 Model Architecture
🔹 1. Feature Extractor

InceptionV3 pretrained on ImageNet

Converts each image into feature vectors

🔹 2. Caption Generator

Embedding Layer (256-dim)

LSTM Decoder (512 units)

Attention mechanism to focus on important regions

Dense network for vocabulary prediction

# ⚙️ Training Configuration

Epochs: 20

Batch Size: 32

Learning Rate: 0.0005

Vocabulary Size: 5000

Max Caption Length: 40 tokens

Early Stopping: Triggered at Epoch 15

📊 Model Performance
📈 Final Metrics

Training Accuracy: 46.89%

Validation Accuracy: 38.19%

Training Loss: 3.339

Validation Loss: 4.2877

# 🔵 BLEU Score Evaluation

BLEU-1: 0.5295

BLEU-2: 0.3431

BLEU-3: 0.2278

BLEU-4: 0.1593

# Interpretation:

Good at recognizing single words

Moderate at short phrases

Struggles with long, coherent sentence matches due to smaller dataset

# 🖼️ Sample Predictions

The model can describe:

Objects (dog, umbrella, luggage, etc.)

People and groups

Simple outdoor/indoor scenes

# 📌 Conclusion

This project successfully demonstrates a functional image captioning system using a CNN + LSTM + Attention pipeline. Performance is promising for a limited dataset and can be improved using:

Larger COCO training set

Transformer-based decoder (e.g., ViT + Transformer)

More epochs with regularization
