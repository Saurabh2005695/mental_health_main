# Mental Health Monitoring System (Django)

This project is a **Django-based mental health monitoring application** that combines computer-vision emotion analysis with patient record management. It analyzes patient video (e.g. webcam feed) to detect facial emotions in real time, storing these emotional cues alongside patient data. Such video-based emotion detection can play a crucial role in mental healthcare, providing insights for diagnosis and monitoring.  
video link : "https://drive.google.com/file/d/1c03YAwsX7VRe_Io6PNINAmkLQ9B0iFQs/view?usp=sharing"

## Features

- **Facial Emotion Detection** – Uses computer vision (OpenCV / DeepFace or similar) to analyze webcam or video input and classify emotions such as happy, sad, angry, surprise, etc.  
- **Patient Record Management** – Maintains models and views for patient profiles and health records. Patient emotional data is logged into the database for tracking.  
- **Dashboard/Admin Interface** – Web interface for clinicians to track patients, review emotional trends, and manage care.  
- **Video Processing Module** – Scripts to capture video frames and perform emotion analysis in real time.  

---

## Setup Instructions (Localhost)

Follow these steps to run the app locally:

### 1. Clone the repository
```bash
git clone https://github.com/Saurabh2005695/mental_health_main.git
cd mental_health_main
2. Create a virtual environment
python3 -m venv venv


Activate it:

Linux/macOS

source venv/bin/activate


Windows (cmd)

venv\Scripts\activate.bat

3. Install dependencies
pip install --upgrade pip
pip install -r requirements.txt

4. Set up environment variables

Create a .env file in the project root (same directory as manage.py) with:

DEBUG=True
SECRET_KEY=your-secret-key
DATABASE_URL=sqlite:///db.sqlite3


⚠️ Make sure to use your own secure SECRET_KEY.

5. Run database migrations
python manage.py makemigrations
python manage.py migrate

6. Create a superuser
python manage.py createsuperuser


Follow the prompts to set up your admin login.

7. Run the development server
python manage.py runserver


The app will be available at: http://localhost:8000

Project Structure
mental_health_main/
├── manage.py
├── requirements.txt
├── mental_health_main/        # Project settings & URLs
│   ├── settings.py
│   ├── urls.py
│   └── ...
├── patients/                  # Example app for patient records
│   ├── models.py
│   ├── views.py
│   └── templates/
├── emotions/                  # Example app for emotion detection
│   ├── video_processing.py
│   ├── views.py
│   └── ...
└── ...


patients/ – manages patient profiles, records, and dashboards

emotions/ – handles emotion detection logic, video capture, and processing

mental_health_main/ – project-level configuration

Demonstration

🎥 Watch the demo video here:  video link : "https://drive.google.com/file/d/1c03YAwsX7VRe_Io6PNINAmkLQ9B0iFQs/view?usp=sharing"
