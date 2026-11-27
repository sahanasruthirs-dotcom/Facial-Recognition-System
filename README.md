# Facial Recognition System Using Python

A face recognition system that identifies people in images by comparing facial encodings with a set of registered faces.

## Overview
Users add photos of different people, the system extracts a numeric encoding for each face, and new test images are matched against the stored encodings. A face that is not close enough to any registered person is labeled `UNKNOWN`. The notebook also evaluates recognition performance.

## Technologies Used
- Python
- face_recognition: face detection and encoding
- OpenCV: image handling
- NumPy: numerical operations
- Scikit-learn: accuracy and classification report
- Matplotlib and Seaborn: results and confusion matrix
- Pickle: saving encodings
- Google Colab / Jupyter Notebook

## Implementation Details
1. **Dataset:** training images of each person in a separate folder.
2. **Face detection:** locate faces in each image.
3. **Encoding:** extract facial encodings with `face_recognition`.
4. **Storage:** save encodings and labels to `face_encodings.pkl` with Pickle.
5. **Recognition:** compare a test face with stored encodings using face distance.
6. **Threshold:** if the smallest distance is below **0.50**, the closest person is returned; otherwise the face is labeled `UNKNOWN`.
7. **Evaluation:** accuracy, precision, recall, F1-score and a confusion matrix on a test set.

## Dataset Structure
```
my_dataset/            # registered people
├── person1/
├── person2/
└── person3/

test_dataset/          # images for evaluation
├── person1/
├── person2/
└── person3/
```
Face images are personal data. The dataset is not included in this repository, so add your own images with the owners' consent.

## Results
The notebook displays each test image with its predicted name or `UNKNOWN` and reports accuracy, a classification report and a confusion matrix.

Add screenshots to an `images/` folder:
```
![Recognition result](images/recognition_result.png)
```

## Project Structure
```
Facial-Recognition-System/
├── face_rec.ipynb      # Encoding, recognition and evaluation
├── requirements.txt
└── README.md
```
`face_encodings.pkl`, `my_dataset/` and `test_dataset/` are created when you run the notebook with your own images.

## Setup Instructions
```bash
git clone https://github.com/sahanasruthirs-dotcom/Facial-Recognition-System.git
cd Facial-Recognition-System
pip install -r requirements.txt
```
`face-recognition` depends on `dlib`, which may need extra setup (CMake and a C++ compiler) on some systems. Google Colab is the easiest option.

## Usage
1. Open `face_rec.ipynb` in Google Colab.
2. Run the install cells.
3. Upload training images into `my_dataset/<person>/`.
4. Run the encoding cells to create `face_encodings.pkl`.
5. Run the recognition cell on a test image.
6. Upload test images to `test_dataset/<person>/` and run the evaluation cells.

## Limitations
Accuracy varies with image quality, lighting, pose and dataset size. This is an educational project and should not be used for security decisions.

## Future Improvements
- Real-time recognition from a webcam or video
- Multiple faces in one image
- Better handling of lighting changes
- A web interface and secure storage for encodings

## Author
**Sahana Sruthi R.S.** · B.Tech CSE (AI & Data Analytics)
[LinkedIn](https://www.linkedin.com/in/sahana-sruthi-r-s-4612b4315) · [Portfolio](https://sahanasruthirs-dotcom.github.io)
