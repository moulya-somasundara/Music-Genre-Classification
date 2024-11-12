# Project Title: Music Genre Classification with CNN and Random Forest

### Project Description
This project aims to classify music genres using both Convolutional Neural Networks (CNN) for image-based spectrogram analysis and a custom Random Forest model. 
Using spectrogram images and various extracted audio features, the models are trained to distinguish between genres, improving genre classification accuracy for digital audio files.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

---

## Project Overview

### CNN Model
The CNN model is used for classifying genres based on spectrogram images. It includes:
- Multiple convolutional and pooling layers.
- Dropout regularization for reducing overfitting.
- A fully connected layer with softmax activation for output classification.

### Random Forest Model
The Random Forest model uses audio feature data extracted from `.wav` files, including MFCC, zero-crossing rate, spectral contrast, etc. It performs classification by building an ensemble of decision trees to improve accuracy.

---

## Features
- **CNN for Image Classification**: Classifies spectrogram images representing different music genres.
- **Custom Random Forest Implementation**: Uses audio features to classify genres with an interpretable model.
- **Audio Feature Extraction**: Processes audio files to extract features like MFCC, spectral roll-off, and more.
- **Data Loading and Preprocessing**: Reads and formats data for training and testing across both models.

---

## Project Structure
```plaintext
├── CNN.ipynb                   # Jupyter Notebook for CNN implementation
├── feature_extraction.ipynb     # Jupyter Notebook for audio feature extraction
├── random_forest.ipynb          # Jupyter Notebook for Random Forest model
├── README.md                    # Project description and instructions
├── requirements.txt             # Required libraries and dependencies
└── data/                        # Folder for dataset storage
    ├── train/                   # Training data
    └── test/                    # Testing data
```


## Usage

### Data Preparation
1. **Spectrograms for CNN**:
   - Place your spectrogram images in the `data/train/` and `data/test/` directories.
   - Ensure images are organized by genre folders (e.g., `data/train/rock`, `data/train/pop`, etc.).

2. **Audio Files for Feature Extraction**:
   - Place `.wav` audio files in a dedicated folder for processing.
   - Run the `feature_extraction.ipynb` notebook to generate and save feature data.

### Model Training
1. **Train CNN Model**:
   - Open `CNN.ipynb` and run the cells to preprocess data and train the CNN model.
   - Evaluate model accuracy on test data.

2. **Train Random Forest Model**:
   - Open `random_forest.ipynb` and run the cells to preprocess data and train the Random Forest model.


## Contributing

1. Fork the project.
2. Create your feature branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add YourFeature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a Pull Request.
