Overview

The Face Recognition App is a Python-based application designed to capture, register, and authenticate faces using facial landmarks and distances. The app leverages several libraries, including OpenCV, Dlib, and Kivy, to provide a user-friendly interface for face recognition tasks.

Features

Capture Images: Use the built-in camera to capture facial images.

Register Faces: Extract facial landmarks and distances, and store them in an SQLite database for future authentication.

Authenticate Faces: Compare captured facial features against stored data to authenticate users.

Database Storage: Store facial landmarks and distance metrics in a secure SQLite database.

Requirements

Python Libraries

Ensure the following Python libraries are installed:

opencv-python

dlib

imutils

numpy

sqlite3 (built-in Python module)

kivy

Additional Files

Download the Dlib's 68-point shape predictor model and extract the shape_predictor_68_face_landmarks.dat file. Place it in the project directory.

Installation

Clone the repository:

git clone https://github.com/yourusername/FaceRecognitionApp.git
cd FaceRecognitionApp

Install the required libraries:

pip install opencv-python dlib imutils numpy kivy

Download and place the shape_predictor_68_face_landmarks.dat file in the project directory.

Usage

Run the application:

python app.py

Use the UI for:

Capturing an Image: Click the Capture Image button to capture a face image.

Registering a Face: Enter a name, then click Register Face to save the facial features in the database.

Authenticating a Face: Click Authenticate Face to verify the captured image against the database.

Database Structure

The app uses SQLite to store facial data:

Landmarks Table:

id: Primary key

label: User's name

part: Facial landmark index (0-67)

x, y: Coordinates of the landmark

Distances Table:

id: Primary key

label: User's name

eye_distance: Distance between eyes

nose_mouth_distance: Distance between nose tip and mouth center

Other distance metrics...

File Structure

.
├── app.py                      # Main application file
├── face_data.db                # SQLite database (auto-generated)
├── shape_predictor_68_face_landmarks.dat # Pre-trained Dlib model
└── README.md                   # Project documentation

Future Improvements

Add a more robust authentication mechanism using machine learning models.

Optimize facial landmark extraction for real-time performance.

Enhance the UI for a smoother user experience.


Acknowledgments

Dlib for the shape predictor model.

OpenCV for image processing.

Kivy for creating the graphical user interface.
