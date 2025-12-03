# 🖼️ Image Caption Generator

<div align="center">

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)](https://www.tensorflow.org/)
[![Keras](https://img.shields.io/badge/Keras-Deep%20Learning-red)](https://keras.io/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Siddhant-Pragyan-Sinha/Image-Caption-Generator)

*A deep learning model that generates descriptive captions for images using CNN-RNN architecture*

[Demo](#demo) • [Features](#features) • [Architecture](#architecture) • [Installation](#installation) • [Usage](#usage) • [Results](#results)

</div>

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Model Architecture](#architecture)
- [Installation](#installation)
- [Dataset Preparation](#dataset-preparation)
- [Training](#training)
- [Inference](#inference)
- [Results](#results)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## 🎯 Overview

This project implements an **Image Caption Generator** using a deep learning approach that combines **Computer Vision** and **Natural Language Processing**. The model uses a CNN encoder (InceptionV3) to extract image features and an LSTM decoder with attention mechanism to generate descriptive captions.

The generator can understand context, objects, and relationships within images to produce human-like descriptions, making it useful for accessibility tools, content management systems, and AI-assisted image tagging.

## ✨ Features

- **Dual-Modality Architecture**: Combines CNN for visual feature extraction with RNN for language generation
- **Attention Mechanism**: Implements Bahdanau attention for better caption alignment
- **Pre-trained Models**: Supports InceptionV3 as feature extractors
- **Beam Search**: Implements beam search algorithm for improved caption generation
- **BLEU Score Evaluation**: Quantitative evaluation of generated captions
- **Web Interface**: Optional Flask-based web application for easy interaction (comingup in future update)
- **Batch Processing**: Efficient handling of large datasets
- **Model Checkpointing**: Automatic saving of best models during training

## 🏗️ Architecture
![model-architecture](/model.png)


### Components
1. **Encoder**: Pre-trained CNN (InceptionV3) for image feature extraction
2. **Decoder**: LSTM with embedding layer and attention mechanism
3. **Attention**: Bahdanau attention to focus on relevant image regions
4. **Text Processing**: Tokenization, padding, and sequence generation

### Technical Specifications
- **Embedding Dimension**: 256
- **LSTM Units**: 512
- **Dropout Rate**: 0.3
- **Attention Units**: 512
- **Vocabulary Size**: 7500+ words
- **Max Caption Length**: 34 tokens

## 🚀 Installation

### Prerequisites
- Python 3.8+
- TensorFlow 2.x
- 8GB+ RAM (16GB recommended)
- GPU support (optional but recommended for training)

### Step-by-Step Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Siddhant-Pragyan-Sinha/Image-Caption-Generator.git
   cd Image-Caption-Generator
   ```
2. **Create virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
# 📊 Dataset Preparation

### Using Flickr8k Dataset
1. Download the ![Flickr8k dataset](https://drive.google.com/file/d/1u3oqx36XApnAykFDB6EEWUIfd_CxRQQ9/view) and ![Flicker8k text](https://drive.google.com/file/d/1qcRy3WpQv4dGtu65gETtYLWxDPBrRtx1/view)

2. Extract and Organise
```
├── Flicker8k_Dataset
│  
└── Flicker8k_text
```   
# 🏋️ Training
## Quick Start
```bash
python main.py
```
## TODO List

    Week 1: Quick Wins

    ✅ Implement beam search (2-3 hours)
    ✅ Add temperature sampling (1 hour)
    ✅ Test and measure improvement
   
    Week 2: Architecture
   
    ✅ Add attention mechanism (1 day)
    ✅ Use spatial features (1 day)
    ✅ Retrain model
   
    Week 3: Training

    ✅ Learning rate scheduling (2 hours)
    ✅ Early stopping (1 hour)
    ✅ Train for more epochs (20-30 instead of 10)
   
    Week 4: Advanced (Optional)
   
    ✅ Consider Transformer decoder
    ✅ Experiment with CLIP features

## 📈 Expected Results with Combined Improvements
| Metric | Current | Phase 1 | Phase 2 | Phase 3 | Phase 4 |
|--------|---------|---------|---------|---------|---------|
| BLEU-1 | 0.366 | 0.41 | 0.45 | 0.48 | 0.52-0.55 |
| BLEU-4 | 0.066 | 0.10 | 0.13 | 0.15 | 0.18-0.22 |
| METEOR | 0.241 | 0.26 | 0.28 | 0.30 | 0.32-0.35 |
| CIDEr  | 0.118 | 0.16 | 0.21 | 0.25 | 0.35-0.45 |

# 📄 License

This project is licensed under the MIT License - see the ![LICENSE](/License) file for details.