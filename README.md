
# 🌀 Parkinson's Disease Detection Using Machine Learning

This project explores the use of **machine learning** and **computer vision** to detect Parkinson's disease by analyzing spiral and wave drawings. By leveraging traditional computer vision techniques and a Random Forest Classifier, this model achieves impressive accuracy even with a small dataset of 204 images.

## 🚀 Features
- **Feature Extraction:** Utilizes Histogram of Oriented Gradients (HOG) to quantify geometric drawings.
- **Machine Learning Model:** Implements a Random Forest Classifier for robust predictions.
- **Metrics Evaluation:** Provides accuracy, sensitivity, and specificity for model performance.
- **Visualization:** Displays a montage of test images with predictions.

## 📂 Dataset
The dataset consists of **204 grayscale images**:
- **Spirals:** 102 images (72 for training, 30 for testing)
- **Waves:** 102 images (72 for training, 30 for testing)

Each image belongs to one of two classes:
- `healthy`
- `parkinson`

The dataset is pre-split into training and testing directories.

## 📋 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo-url.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the script:
   ```bash
   python detect_parkinsons.py --dataset path/to/dataset --trials 5
   ```

## 🛠️ Dependencies
- Python 3.7+
- OpenCV
- scikit-image
- scikit-learn
- NumPy
- imutils

Install all dependencies with:
```bash
pip install opencv-python scikit-image scikit-learn numpy imutils
```

## 🔍 How It Works
1. **Image Preprocessing:**
   - Converts images to grayscale.
   - Resizes to 200x200 pixels.
   - Applies binary thresholding to highlight drawings.

2. **Feature Extraction:**
   - Extracts features using HOG (Histogram of Oriented Gradients).

3. **Training the Model:**
   - Trains a Random Forest Classifier with 100 trees.
   - Encodes labels (`healthy`, `parkinson`) into integers.

4. **Model Evaluation:**
   - Calculates accuracy, sensitivity, and specificity across multiple trials.
   - Displays results with mean and standard deviation.

5. **Visualization:**
   - Randomly selects test images.
   - Generates a labeled montage with predictions (`healthy` in green, `parkinson` in red).

## 📊 Results
- **Accuracy:** 80-90% (depending on the trial).
- **Sensitivity:** High detection rate for Parkinson’s cases.
- **Specificity:** Reliable distinction between healthy and Parkinson’s cases.

## 🎯 Key Functions
- `quantify_image(image)`: Extracts HOG features from an image.
- `load_split(path)`: Loads images and labels from the dataset directory.
- `RandomForestClassifier`: Trains and evaluates the model.

## 🖼️ Visualization
The script generates a **montage** of test images with predictions. Healthy cases are highlighted in **green**, and Parkinson’s cases in **red**.

## 🧠 Why It Matters
Detecting Parkinson's disease early can significantly improve patient outcomes. This project demonstrates how even small datasets can yield meaningful results with the right techniques.

## 🤝 Contributions
Feel free to contribute by:
- Adding new features.
- Improving the dataset.
- Optimizing the model.

## 📄 License
This project is licensed under the MIT License. Feel free to use and modify the code as needed.
