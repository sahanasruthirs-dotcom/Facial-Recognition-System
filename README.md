# 👤 Face Recognition System using Python

## 📌 Project Overview

This project implements a **Face Recognition System using Python** that identifies individuals from images by comparing facial features with previously registered faces.

The system allows users to upload images of different people, extract facial encodings, store the encodings, and recognize faces in new images. If a face does not match any registered person within the predefined threshold, it is classified as **UNKNOWN**.

The project combines facial detection, face encoding, similarity comparison, and model evaluation to demonstrate a basic face recognition pipeline.

## 🎯 Objectives

- Detect faces from uploaded images.
- Create a dataset of known individuals.
- Extract and store facial encodings.
- Recognize individuals from test images.
- Identify unknown faces.
- Evaluate recognition performance using accuracy and classification metrics.

## 🛠️ Technologies Used

- **Python**
- **OpenCV** – Image processing and face detection
- **face_recognition** – Facial encoding and face comparison
- **NumPy** – Numerical operations
- **Scikit-learn** – Model evaluation and metrics
- **Matplotlib** – Visualization
- **Seaborn** – Confusion matrix visualization
- **Google Colab** – Development and execution environment

## ⚙️ System Workflow

1. **Dataset Collection** – Upload facial images of different individuals.
2. **Face Detection** – Detect faces from the uploaded images.
3. **Face Encoding** – Extract facial feature encodings using the `face_recognition` library.
4. **Encoding Storage** – Save the facial encodings and corresponding labels using Pickle.
5. **Face Recognition** – Compare the encodings of test images with the stored encodings.
6. **Identity Prediction** – Assign the name of the closest matching individual.
7. **Unknown Face Detection** – Label unmatched faces as `UNKNOWN`.
8. **Performance Evaluation** – Calculate accuracy and generate classification reports.

## 🧠 Recognition Method

The system uses facial encodings to represent faces numerically.

When a test image is provided:

- Facial features are extracted from the image.
- The extracted encoding is compared with the stored known encodings.
- Face distance is calculated to determine similarity.
- The closest match is selected if it satisfies the recognition threshold.

### Recognition Threshold

The project uses a face-distance threshold of **0.50**.

- If the minimum face distance is below `0.50`, the face is recognized as the closest registered individual.
- If the distance is greater than or equal to `0.50`, the face is classified as `UNKNOWN`.

## 📂 Dataset Structure

### Training Dataset

Images of registered individuals are stored in separate folders.

```text
my_dataset/
├── person1/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── image3.jpg
├── person2/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── image3.jpg
└── person3/
    ├── image1.jpg
    ├── image2.jpg
    └── image3.jpg
```

### Testing Dataset

Test images are organized according to the actual identity of each person.

```text
test_dataset/
├── person1/
│   ├── test1.jpg
│   └── test2.jpg
├── person2/
│   ├── test1.jpg
│   └── test2.jpg
└── person3/
    ├── test1.jpg
    └── test2.jpg
```

## 🚀 Features

- 📸 Upload facial images for multiple individuals.
- 🧑‍💻 Generate facial encodings for registered people.
- 💾 Save and reload encodings using Pickle.
- 🔍 Recognize faces in test images.
- ❓ Detect and classify unrecognized faces as `UNKNOWN`.
- 📊 Evaluate the system using accuracy and classification reports.
- 📈 Visualize face recognition results.

## 📊 Evaluation Metrics

The system evaluates its performance using:

- **Accuracy** – Overall percentage of correctly identified test images.
- **Precision** – Correct identification performance for each class.
- **Recall** – Ability to correctly identify actual individuals.
- **F1-Score** – Balance between precision and recall.
- **Confusion Matrix** – Visual representation of actual versus predicted labels.

## 📦 Installation

Install the required libraries:

```bash
pip install face-recognition
pip install opencv-python
pip install numpy
pip install scikit-learn
pip install matplotlib
pip install seaborn
```

> Note: The `face-recognition` library depends on `dlib`, which may require additional setup depending on your operating system and Python environment.

## ▶️ How to Run

### 1. Open the Notebook

Open `face_rec.ipynb` using Google Colab.

### 2. Install Dependencies

Run the notebook's installation cells to install the required packages.

### 3. Upload Training Images

Upload clear facial images of individuals into their respective folders:

```text
my_dataset/person1/
my_dataset/person2/
my_dataset/person3/
```

### 4. Generate Face Encodings

Run the encoding cells to extract facial features and save the encodings into:

```text
face_encodings.pkl
```

### 5. Perform Face Recognition

Provide a test image and execute the recognition cell. The system will display the image with the predicted identity or `UNKNOWN`.

### 6. Evaluate the System

Upload test images into the `test_dataset` directory and run the evaluation cells to obtain accuracy and classification metrics.

## 📁 Project Structure

```text
Face-Recognition-System/
│
├── face_rec.ipynb          # Main face recognition notebook
├── my_dataset/             # Images of registered individuals
├── test_dataset/           # Images used for evaluation
├── face_encodings.pkl      # Stored facial encodings (generated)
└── README.md               # Project documentation
```

## 🔮 Future Enhancements

- Real-time face recognition through a webcam.
- Recognition of multiple faces in a single image.
- Improved recognition under different lighting conditions.
- Face recognition from video streams.
- Integration with a web-based interface.
- Secure database storage for facial encodings.
- Improved unknown-person detection and recognition accuracy.

## ⚠️ Disclaimer

This project is developed for educational and experimental purposes. Facial recognition accuracy may vary depending on image quality, lighting, pose, and the size and diversity of the dataset.

Facial images and biometric encodings are sensitive personal data. Ensure that images are collected and processed with consent and stored securely.

## 👩‍💻 Author

**Sahana Sruthi R.S.**

---

⭐ If you find this project interesting, feel free to explore the repository!
