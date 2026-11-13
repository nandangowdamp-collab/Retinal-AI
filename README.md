# 🏥 AI-Based Retinal Image Classification for Early Detection of Eye Diseases

**An AI-powered healthcare web application for retinal disease detection, patient management, and doctor–patient communication.**

---

## 📌 1. Project Overview

The **AI-Based Retinal Image Classification for Early Detection of Eye Diseases** is a full-stack healthcare web application that uses Artificial Intelligence (AI), Machine Learning (ML), and Deep Learning to analyze retinal fundus images and identify potential eye diseases.

The system uses a **TensorFlow-based Convolutional Neural Network (CNN)** model to classify retinal images into four categories:

1. Normal
2. Glaucoma
3. Diabetic Retinopathy
4. Hypertensive Retinopathy

The application provides three independent portals:

- **Patient Portal:** Allows patients to upload retinal images, view AI-generated prediction reports, check previous results, and communicate directly with doctors.
- **Doctor Portal:** Allows doctors to view assigned patients, access retinal image analysis reports, review AI predictions, communicate with patients, and provide medical recommendations.
- **Admin Portal:** Allows administrators to manage patients, doctors, appointments, user accounts, and overall platform activities.

The main objective is to assist healthcare professionals in identifying possible retinal abnormalities at an early stage and improving the efficiency of preliminary eye screening.

> **Important:** This application is an academic decision-support prototype. AI predictions are not medical diagnoses. All results must be reviewed by a qualified ophthalmologist.

---

## 🎯 2. Project Objectives

- Develop an AI-powered retinal image classification system.
- Detect four categories of retinal conditions using TensorFlow.
- Generate percentage-based prediction results for each disease category.
- Provide separate dashboards for patients, doctors, and administrators.
- Enable direct communication between patients and doctors through an integrated messenger.
- Allow doctors to access patient reports and prediction history.
- Maintain patient records and previous prediction results.
- Generate downloadable retinal analysis reports.
- Develop a responsive and user-friendly healthcare platform.

---

## 🚀 3. Key Features

### 👤 A. Patient Portal

The Patient Portal provides patients with a personalized dashboard to manage their retinal health records.

**Features:**

- Patient registration and secure login.
- Personal profile management.
- Upload retinal fundus images.
- AI-powered retinal image analysis.
- View classification results and confidence percentages.
- View previous prediction history.
- Download AI-generated PDF reports.
- View assigned doctor details.
- Direct messaging with doctors.
- Request appointments.
- View doctor recommendations and prescriptions.
- Track report and consultation history.

### 🩺 B. Doctor Portal

The Doctor Portal provides doctors with tools to review patient information and AI-generated retinal analysis reports.

**Features:**

- Doctor registration and login (subject to admin approval).
- Doctor profile management.
- View assigned patients.
- View patient retinal images.
- Access AI-generated prediction reports.
- View disease classification percentages.
- Review patient prediction history.
- Add medical observations and recommendations.
- Create and manage prescriptions.
- Manage patient appointments.
- Direct messaging with patients.
- Download patient reports.
- Update consultation status.

**Doctor Dashboard Modules:**

1. Total Assigned Patients
2. Pending Appointments
3. New Patient Reports
4. AI Prediction History
5. Patient Messenger
6. Medical Recommendations

### 🛡️ C. Admin Portal

The Admin Portal provides centralized management of the entire healthcare platform.

**Features:**

- Admin authentication.
- Dashboard analytics.
- Manage patient accounts.
- Manage doctor accounts.
- Approve or reject doctor registrations.
- Activate or deactivate accounts.
- View all patient records.
- Manage doctor–patient assignments.
- Monitor AI prediction records.
- Manage appointments.
- Monitor communication activity where authorized.
- Manage system settings.
- View platform usage statistics.

---

## 🧠 4. AI-Based Retinal Disease Classification

The AI module is the core component of this project.

It uses a trained Deep Learning model built with **TensorFlow and Keras** to analyze retinal fundus images.

### Supported Disease Categories

| Class | Description |
|---|---|
| Normal | Retinal image without detected signs of the target conditions |
| Glaucoma | Identifies retinal features associated with possible glaucoma |
| Diabetic Retinopathy | Identifies retinal changes associated with diabetic retinopathy |
| Hypertensive Retinopathy | Identifies retinal changes associated with hypertension |

### AI Prediction Workflow

1. Patient uploads a retinal fundus image.
2. Flask backend validates the uploaded image.
3. Image preprocessing is performed.
4. The processed image is passed to the trained TensorFlow model.
5. The model predicts probabilities for all four classes.
6. The system identifies the highest-scoring class.
7. Prediction results are displayed on the patient dashboard.
8. The prediction report is stored in the database.
9. The assigned doctor can review the report.

### Example AI Prediction Result

The following values are illustrative examples, not actual model outputs.

| Disease Category | Prediction Confidence |
|---|---:|
| Normal | 10% |
| Glaucoma | 15% |
| Diabetic Retinopathy | 65% |
| Hypertensive Retinopathy | 10% |

**Predicted Class:** Diabetic Retinopathy

**Highest Model Confidence:** 65%

The system should display all four class scores instead of showing only the predicted class.

**Note:** These percentages represent model confidence scores, not the probability that a patient has a disease or the severity of that disease. Model calibration and clinical validation are required before interpreting them clinically.

---

## 🏗️ 5. Technology Stack

### Frontend Technologies

| Technology | Purpose |
|---|---|
| HTML5 | Webpage structure |
| CSS3 | Styling and responsive design |
| JavaScript | Frontend interactions |
| React.js | Component-based user interface |
| React Router | Portal navigation |
| Axios | API communication |

### Backend Technologies

| Technology | Purpose |
|---|---|
| Python | Backend programming |
| Flask | Pure Python backend framework |
| Flask-CORS | Cross-origin API communication |
| Flask-JWT-Extended | Authentication and authorization |
| Flask-SocketIO | Real-time doctor–patient messaging |
| Werkzeug | Secure file upload utilities |

### AI / Machine Learning

| Technology | Purpose |
|---|---|
| TensorFlow | Deep Learning framework |
| Keras | CNN model development |
| NumPy | Numerical operations |
| Pillow / OpenCV | Image preprocessing |
| Scikit-learn | Model evaluation |
| Matplotlib | Model performance visualization |

### Database

- MySQL / PostgreSQL – Primary database.
- SQLAlchemy – Database ORM.
- Local or cloud-based secure storage – Retinal image and report storage.

### Additional Tools

- Git and GitHub – Version control.
- VS Code – Development environment.
- Postman – API testing.
- ReportLab – PDF report generation.

---

## 🏛️ 6. System Architecture

The application follows a three-tier architecture.

```text
                 USER INTERFACE
                       |
          +------------+------------+
          |            |            |
      PATIENT        DOCTOR        ADMIN
       PORTAL        PORTAL        PORTAL
          |            |            |
          +------------+------------+
                       |
                 REACT FRONTEND
                       |
                  AXIOS / API
                       |
              PYTHON FLASK BACKEND
                       |
       +---------------+----------------+
       |               |                |
   AUTH MODULE     AI PREDICTION    MESSAGING
       |               |                |
       |           TENSORFLOW       SOCKET.IO
       |           CNN MODEL            |
       |               |                |
       +---------------+----------------+
                       |
                  DATABASE
                       |
          +------------+------------+
          |            |            |
       PATIENT       DOCTOR       REPORTS
       RECORDS       RECORDS      HISTORY
```

### Architecture Explanation

- React.js provides the frontend interface.
- HTML and CSS are used to structure and style the application.
- Flask handles backend business logic and REST APIs.
- TensorFlow performs retinal image classification.
- Socket.IO enables real-time doctor–patient messaging.
- MySQL/PostgreSQL stores application records.
- Secure file storage maintains retinal images and generated reports.

---

## 💬 7. Doctor–Patient Messenger

One of the major features of the application is the integrated messaging system.

Patients and doctors can communicate directly without switching to an external messaging application.

### Patient Messenger Features

- View assigned doctor.
- Send text messages.
- Receive doctor responses.
- View previous conversations.
- Share report references with doctors.
- View message timestamps.
- Receive new-message notifications.

### Doctor Messenger Features

- View assigned patient conversations.
- Reply to patient messages.
- Review patient reports during consultation.
- Share medical recommendations.
- Send appointment-related messages.
- Access previous conversation history.

### Messaging Architecture

```text
       PATIENT PORTAL
              |
         SEND MESSAGE
              |
        FLASK-SOCKETIO
              |
       MESSAGE VALIDATION
              |
           DATABASE
              |
        REAL-TIME EVENT
              |
        DOCTOR PORTAL
              |
        RECEIVE MESSAGE
```

**Technology:** Flask-SocketIO and Socket.IO Client.

**Security:** Only authorized patients and their assigned doctors should be allowed to access a conversation.

---

## 📊 8. AI-Generated Medical Report

After image classification, the application generates a structured report.

### Report Contents

- Patient ID
- Patient Name
- Report ID
- Image Upload Date
- Retinal Image
- Predicted Disease Category
- Normal Confidence Percentage
- Glaucoma Confidence Percentage
- Diabetic Retinopathy Confidence Percentage
- Hypertensive Retinopathy Confidence Percentage
- AI Model Version
- Doctor's Observations
- Doctor's Recommendations
- Consultation Status

### Sample Report

```text
=========================================
       RETINAL IMAGE ANALYSIS REPORT
=========================================

Patient ID       : PAT001
Report ID        : REP001
Analysis Date    : DD-MM-YYYY

AI CLASSIFICATION RESULTS

Normal                    : 10%
Glaucoma                  : 15%
Diabetic Retinopathy      : 65%
Hypertensive Retinopathy  : 10%

Predicted Category:
Diabetic Retinopathy

Model Confidence:
65%

Doctor Review:
Pending

=========================================
Note: AI-generated screening result.
Not a confirmed medical diagnosis.
=========================================
```

Reports can be downloaded in PDF format.

---

## 🗄️ 9. Database Design

The application uses a relational database to organize patient information, doctor details, reports, appointments, and conversations.

### Main Database Tables

| Table | Purpose |
|---|---|
| users | Authentication and account information |
| patients | Patient profile details |
| doctors | Doctor profile and qualification details |
| doctor_patient | Patient–doctor assignments |
| retinal_images | Uploaded retinal images |
| predictions | AI classification results |
| reports | Generated medical reports |
| appointments | Appointment details |
| conversations | Doctor–patient conversation records |
| messages | Individual chat messages |
| prescriptions | Doctor-issued prescriptions |
| notifications | System notifications |

### Database Relationship Overview

```text
USERS
  |
  +---- PATIENTS
  |
  +---- DOCTORS
  |
  +---- ADMINS

PATIENTS
  |
  +---- RETINAL_IMAGES
  |          |
  |          +---- PREDICTIONS
  |                     |
  |                     +---- REPORTS
  |
  +---- APPOINTMENTS
  |
  +---- CONVERSATIONS
               |
               +---- MESSAGES

DOCTORS
  |
  +---- DOCTOR_PATIENT
  |
  +---- PRESCRIPTIONS
  |
  +---- APPOINTMENTS
```

---

## 📁 10. Project Folder Structure

The following is the recommended folder structure for the project.

```text
AI-Retinal-Disease-Classification/
│
├── frontend/
│   ├── public/
│   │   ├── logo.png
│   │   └── assets/
│   │
│   ├── src/
│   │   ├── assets/
│   │   │
│   │   ├── components/
│   │   │   ├── Navbar.jsx
│   │   │   ├── Sidebar.jsx
│   │   │   ├── ProtectedRoute.jsx
│   │   │   ├── Messenger.jsx
│   │   │   └── ReportCard.jsx
│   │   │
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── Register.jsx
│   │   │   │
│   │   │   ├── patient/
│   │   │   │   ├── PatientDashboard.jsx
│   │   │   │   ├── UploadRetinalImage.jsx
│   │   │   │   ├── PatientReports.jsx
│   │   │   │   └── PatientMessages.jsx
│   │   │   │
│   │   │   ├── doctor/
│   │   │   │   ├── DoctorDashboard.jsx
│   │   │   │   ├── PatientList.jsx
│   │   │   │   ├── PatientReports.jsx
│   │   │   │   └── DoctorMessages.jsx
│   │   │   │
│   │   │   └── admin/
│   │   │       ├── AdminDashboard.jsx
│   │   │       ├── ManagePatients.jsx
│   │   │       ├── ManageDoctors.jsx
│   │   │       └── ManageAppointments.jsx
│   │   │
│   │   ├── services/
│   │   │   ├── api.js
│   │   │   └── socket.js
│   │   │
│   │   ├── context/
│   │   │   └── AuthContext.jsx
│   │   │
│   │   ├── styles/
│   │   │   ├── global.css
│   │   │   ├── dashboard.css
│   │   │   └── messenger.css
│   │   │
│   │   ├── App.jsx
│   │   └── main.jsx
│   │
│   └── package.json
│
├── backend/
│   ├── app.py
│   ├── config.py
│   ├── extensions.py
│   │
│   ├── routes/
│   │   ├── auth_routes.py
│   │   ├── patient_routes.py
│   │   ├── doctor_routes.py
│   │   ├── admin_routes.py
│   │   ├── prediction_routes.py
│   │   ├── report_routes.py
│   │   ├── appointment_routes.py
│   │   └── message_routes.py
│   │
│   ├── models/
│   │   ├── user.py
│   │   ├── patient.py
│   │   ├── doctor.py
│   │   ├── prediction.py
│   │   ├── report.py
│   │   ├── appointment.py
│   │   └── message.py
│   │
│   ├── services/
│   │   ├── prediction_service.py
│   │   ├── image_service.py
│   │   ├── report_service.py
│   │   └── messaging_service.py
│   │
│   ├── ai_model/
│   │   ├── predictor.py
│   │   ├── preprocessing.py
│   │   └── retinal_model.keras
│   │
│   ├── uploads/
│   │   └── retinal_images/
│   │
│   ├── generated_reports/
│   │
│   └── requirements.txt
│
├── database/
│   └── schema.sql
│
├── docs/
│   ├── architecture.png
│   └── screenshots/
│
├── .env.example
├── .gitignore
└── README.md
```

---

## 🔗 11. Main Backend API Endpoints

The backend uses RESTful APIs developed using pure Python Flask.

### Authentication APIs

| Method | Endpoint | Description |
|---|---|---|
| POST | /api/auth/register | Register a user |
| POST | /api/auth/login | Login |
| POST | /api/auth/logout | Logout |
| GET | /api/auth/profile | Get user profile |

### Patient APIs

| Method | Endpoint | Description |
|---|---|---|
| GET | /api/patient/dashboard | Patient dashboard |
| POST | /api/patient/upload | Upload retinal image |
| GET | /api/patient/reports | View reports |
| GET | /api/patient/history | Prediction history |
| GET | /api/patient/doctors | View assigned doctors |

### Doctor APIs

| Method | Endpoint | Description |
|---|---|---|
| GET | /api/doctor/dashboard | Doctor dashboard |
| GET | /api/doctor/patients | View assigned patients |
| GET | /api/doctor/reports | View patient reports |
| POST | /api/doctor/recommendation | Add recommendations |
| POST | /api/doctor/prescription | Create prescription |

### Admin APIs

| Method | Endpoint | Description |
|---|---|---|
| GET | /api/admin/dashboard | Admin dashboard |
| GET | /api/admin/patients | Manage patients |
| GET | /api/admin/doctors | Manage doctors |
| PUT | /api/admin/doctor/approve/:id | Approve doctor |
| DELETE | /api/admin/user/:id | Manage user deletion |

### Prediction APIs

| Method | Endpoint | Description |
|---|---|---|
| POST | /api/prediction/classify | Classify retinal image |
| GET | /api/prediction/history | Get prediction history |
| GET | /api/prediction/:id | Get prediction details |

### Messaging APIs

| Method | Endpoint | Description |
|---|---|---|
| GET | /api/messages/:conversation_id | Get conversation |
| POST | /api/messages/send | Send message |
| GET | /api/messages/conversations | Get conversations |

Real-time messaging events are handled separately using Flask-SocketIO.

---

## ⚙️ 12. Installation and Setup

### Prerequisites

Install the following tools:

- Python 3.10 or 3.11
- Node.js and npm
- MySQL or PostgreSQL
- Visual Studio Code
- Git

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/AI-Retinal-Disease-Classification.git

cd AI-Retinal-Disease-Classification
```

### Step 2: Backend Setup

Navigate to the backend folder.

```bash
cd backend
```

Create a virtual environment.

```bash
python -m venv venv
```

Activate the environment on Windows.

```bash
venv\Scripts\activate
```

Install the dependencies.

```bash
pip install -r requirements.txt
```

### Step 3: Configure Environment Variables

Create a `.env` file inside the project root or configure it according to your backend settings.

Example:

```env
SECRET_KEY=your-secret-key
JWT_SECRET_KEY=your-jwt-secret
DATABASE_URL=mysql+pymysql://root:password@localhost/retinal_ai
UPLOAD_FOLDER=uploads/retinal_images
MODEL_PATH=ai_model/retinal_model.keras
```

Use your own database credentials and keep `.env` out of Git.

### Step 4: Start Flask Backend

```bash
python app.py
```

Backend server:

```text
http://127.0.0.1:5000
```

### Step 5: Frontend Setup

Open another terminal.

```bash
cd frontend
```

Install dependencies.

```bash
npm install
```

Start the React development server.

```bash
npm run dev
```

Frontend server:

```text
http://localhost:5173
```

---

## 📦 13. Recommended Python Requirements

Create `backend/requirements.txt`:

```txt
Flask
Flask-Cors
Flask-SQLAlchemy
Flask-JWT-Extended
Flask-SocketIO
python-dotenv
tensorflow
numpy
Pillow
opencv-python
scikit-learn
matplotlib
pandas
reportlab
PyMySQL
eventlet
```

Use compatible package versions for your selected Python and TensorFlow versions. For production, configure and test the Socket.IO deployment with a compatible server and async mode.

---

## 🔐 14. Security and Privacy

Because this project handles sensitive healthcare information, security is an important part of the application.

Recommended security practices:

- Hash passwords before storing them.
- Use JWT-based authentication.
- Implement role-based access control.
- Restrict patient reports to authorized doctors.
- Validate uploaded image file types and sizes.
- Generate unique filenames for uploaded images.
- Prevent unauthorized access to uploaded files.
- Use secure environment variables.
- Protect messaging conversations with access permissions.
- Maintain audit logs for sensitive actions.
- Use HTTPS in deployment.
- Obtain appropriate consent before storing patient information.

---

## 📈 15. Future Enhancements

The project can be extended with the following features:

1. Integration of advanced CNN architectures such as EfficientNet and ResNet.
2. Grad-CAM visualization to highlight important retinal image regions.
3. Improved AI model accuracy through larger and more diverse datasets.
4. Model confidence calibration and external clinical validation.
5. Real-time video consultation between doctors and patients.
6. Online appointment booking.
7. Automated email and notification services.
8. Multilingual user interface.
9. Cloud-based image and report storage.
10. Mobile application integration.
11. Doctor analytics dashboard.
12. Advanced patient health-history tracking.

---

## 🎓 16. Expected Project Outcome

The expected outcome is a fully functional AI-powered healthcare web application that combines retinal image classification, patient management, doctor consultation, and administrative management in one platform.

The application will provide:

- Three separate user portals.
- TensorFlow-based classification of four retinal image categories.
- Percentage-based AI prediction results.
- Patient report generation.
- Doctor access to patient reports.
- Direct doctor–patient messaging.
- Appointment and patient management.
- Secure centralized healthcare records.

---

## 👨‍💻 17. Project Team

**Project Title:** AI-Based Retinal Image Classification for Early Detection of Eye Diseases

**Project Type:** Full-Stack Development + Artificial Intelligence + Deep Learning

**Frontend:** React.js, HTML5, CSS3, JavaScript

**Backend:** Python Flask

**AI Framework:** TensorFlow / Keras

**Database:** MySQL / PostgreSQL

---

## 📜 18. Disclaimer

This project is developed for academic and research purposes. AI-generated classifications are intended to support preliminary retinal image screening and must not replace professional medical examinations, clinical diagnosis, or treatment decisions.

The model's performance depends on the quality, diversity, and validation of its training data. A qualified eye-care professional must review the findings.

---

**⭐ AI-Based Retinal Image Classification for Early Detection of Eye Diseases**

*Combining Artificial Intelligence and Healthcare Technology to support early retinal disease screening.*
