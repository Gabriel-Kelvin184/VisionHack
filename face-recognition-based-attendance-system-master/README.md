# Face Recognition Attendance System

This project is a **Face Recognition Attendance System** built using Python, Flask, OpenCV, and machine learning. It allows users to register their faces, take attendance using a webcam, and manage attendance records.

---

## Features
1. **User Registration**: Add new users by capturing their face data using a webcam.
2. **Attendance Tracking**: Detect and mark attendance using face recognition.
3. **Manage Users**: List or delete registered users.
4. **Daily Attendance Logs**: Automatically saves attendance records for each day.

---

## Prerequisites
Ensure you have the following installed:
- Python 3.8 or above
- OpenCV
- Flask
- Numpy
- Pandas
- Scikit-learn
- Joblib

---

## Installation and Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-repository/face-recognition-attendance.git
cd face-recognition-attendance
```

### 2. Install Dependencies
Install the required Python libraries:
```bash
pip install -r requirements.txt
```

### 3. Download Haarcascade XML
Download the Haarcascade XML file for face detection:
- File: [haarcascade_frontalface_default.xml](https://github.com/opencv/opencv/blob/master/data/haarcascades/haarcascade_frontalface_default.xml)
- Save it in the project root directory.

### 4. Directory Structure
The application expects the following directory structure:
```plaintext
project-root/
├── Attendance/        # Stores daily attendance logs
├── static/
│   ├── faces/         # Stores user face data
│   ├── face_recognition_model.pkl  # Trained ML model (auto-generated)
├── templates/         # HTML templates
└── app.py             # Main application script
```
- These folders will be created automatically during runtime.

---

## Running the Application

### 1. Start the Flask App
Run the following command to start the server:
```bash
python app.py
```

### 2. Open in Browser
Open your browser and navigate to:
```
http://127.0.0.1:5000/
```

---

## How to Use

### **1. Add a New User**
- Navigate to the **Add User** page.
- Enter the **Name** and **Roll Number** of the new user.
- The webcam will activate to capture facial images.
- After capturing images, the system will automatically train the model.

### **2. Take Attendance**
- Click on the **Take Attendance** button on the home page.
- The webcam will activate to detect faces and mark attendance.

### **3. View Attendance**
- View attendance records on the home page.
- The attendance is saved in the `Attendance/` folder as CSV files (e.g., `Attendance-12_06_24.csv`).

### **4. Manage Users**
- View all registered users on the **List Users** page.
- Delete a user by selecting their profile.

---

## Important Notes
1. **Model Training**: The model is retrained whenever a new user is added.
2. **Minimum Requirements**:
   - Ensure `haarcascade_frontalface_default.xml` is present.
   - Add at least one user to create the ML model.
3. **Face Detection**: Ensure proper lighting and face alignment during registration and attendance.
4. **Webcam**: Ensure your webcam is working properly.

---

## Troubleshooting

### Issue: No trained model found
- Add at least one user to train the model.

### Issue: Webcam not detected
- Ensure your webcam is connected and accessible by OpenCV.

### Logs and Errors
- Check the terminal for error logs during runtime.

---

## Future Improvements
1. Replace Haarcascade with a more robust face detection model (e.g., Dlib or Mediapipe).
2. Add a backend database to manage users and attendance records.
3. Improve the UI for better user experience.

---

## Credits
- **OpenCV**: For face detection.
- **Scikit-learn**: For building the KNN-based face recognition model.
- **Flask**: For web application framework.

---

Enjoy using the **Face Recognition Attendance System**! 😊