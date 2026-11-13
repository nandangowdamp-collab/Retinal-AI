# 🏥 AI-Based Retinal Image Classification for Early Detection of Eye Diseases

### An Intelligent Healthcare Platform Powered by Artificial Intelligence, Deep Learning and Full-Stack Web Technologies

<p align="center">
  <b>AI-Powered Retinal Screening | Doctor–Patient Communication | Smart Healthcare Management</b>
</p>

---

## 📌 1. About the Project

The **AI-Based Retinal Image Classification for Early Detection of Eye Diseases** is an intelligent healthcare web application designed to assist in the preliminary identification of retinal diseases using Artificial Intelligence and Deep Learning.

The application uses a trained **TensorFlow/Keras CNN model** to analyze retinal fundus images and classify them into four categories:

1. Normal
2. Glaucoma
3. Diabetic Retinopathy
4. Hypertensive Retinopathy

The system provides a centralized platform with three separate portals:

- **Patient Portal:** Upload retinal images, view AI prediction results, download reports, manage appointments and communicate directly with doctors.
- **Doctor Portal:** View assigned patients, access retinal images and AI reports, review predictions, provide recommendations and communicate with patients.
- **Admin Portal:** Manage patients, doctors, appointments, accounts and platform activities.

The main objective is to combine AI-powered retinal image analysis with a practical healthcare management system.

---

## 🎯 2. Project Objectives

- Develop an AI-powered retinal disease classification application.
- Classify retinal images into four different categories.
- Generate confidence percentages for all four disease categories.
- Provide separate dashboards for patients, doctors and administrators.
- Implement real-time communication between doctors and patients.
- Allow doctors to view and review patient retinal reports.
- Generate downloadable PDF analysis reports.
- Maintain patient records and prediction history.
- Implement secure role-based authentication.
- Develop a responsive and user-friendly interface.

---

## 🚀 3. Main Modules

### 3.1 Patient Portal

The Patient Portal provides patients with a personalized healthcare dashboard.

**Features:**

- Patient registration and login.
- Personal profile management.
- Upload retinal fundus images.
- AI-based retinal disease classification.
- View all four prediction percentages.
- View the highest-confidence prediction.
- Access previous prediction history.
- Download PDF analysis reports.
- View assigned doctor information.
- Direct messaging with doctors.
- Request doctor appointments.
- View medical recommendations and prescriptions.
- Track consultation history.

### 3.2 Doctor Portal

The Doctor Portal allows doctors to manage patient consultations and review AI-generated retinal reports.

**Features:**

- Doctor login and profile management.
- Admin-approved doctor accounts.
- View assigned patients.
- View patient retinal images.
- Access AI-generated reports.
- View all four classification percentages.
- Review patient prediction history.
- Add medical observations.
- Provide recommendations.
- Create prescriptions.
- Manage appointments.
- Direct communication with patients.
- Download patient reports.

**Doctor Dashboard Sections:**

1. Dashboard Overview
2. Assigned Patients
3. Patient Reports
4. AI Prediction Analysis
5. Appointments
6. Patient Messenger
7. Medical Recommendations

### 3.3 Admin Portal

The Admin Portal provides centralized control over the complete application.

**Features:**

- Admin authentication.
- Dashboard analytics.
- Manage patient accounts.
- Manage doctor accounts.
- Approve or reject doctor registrations.
- Activate and deactivate accounts.
- Assign doctors to patients.
- Manage appointments.
- View prediction statistics.
- Monitor platform activities.
- Manage user access permissions.
- Maintain system records.

---

## 🧠 4. AI-Based Retinal Disease Classification

The AI module is the core functionality of this project.

It uses a trained **Convolutional Neural Network (CNN)** developed using TensorFlow and Keras.

### 4.1 Supported Classification Categories

| Category | Description |
|---|---|
| Normal | No visible signs of the target conditions detected by the model |
| Glaucoma | Retinal features associated with possible glaucoma |
| Diabetic Retinopathy | Retinal abnormalities associated with diabetes |
| Hypertensive Retinopathy | Retinal abnormalities associated with hypertension |

### 4.2 AI Prediction Workflow

```text
Patient Uploads Retinal Image
             |
             v
      Flask Image API
             |
             v
       Image Validation
             |
             v
     Image Preprocessing
             |
             v
     TensorFlow CNN Model
             |
             v
      Four-Class Prediction
             |
             v
     Confidence Calculation
             |
             v
       Prediction Results
             |
       +-----+------+
       |            |
       v            v
 Patient Portal  Doctor Portal
       |            |
       +-----+------+
             |
             v
       Database Storage
```

### 4.3 Prediction Result Example

The following is an illustrative example, not a real model prediction.

| Disease Category | Confidence Score |
|---|---:|
| Normal | 10% |
| Glaucoma | 15% |
| Diabetic Retinopathy | 65% |
| Hypertensive Retinopathy | 10% |

**Highest Model Confidence:** 65%

**Top Predicted Category:** Diabetic Retinopathy

The application must display all four scores using visual progress bars or charts.

**Important:** These percentages are model confidence scores, not confirmed disease probabilities or disease severity measurements. They should not be interpreted as a medical diagnosis.

### 4.4 Recommended AI Architecture

Use EfficientNetB0 with TensorFlow/Keras as the initial model architecture.

**Model pipeline:**

1. Collect a suitable retinal fundus image dataset.
2. Organize images into four classes.
3. Remove corrupted or unsuitable images.
4. Resize images to the model's required input dimensions.
5. Normalize images using the exact preprocessing expected by the selected model.
6. Apply data augmentation to the training dataset.
7. Train the CNN model.
8. Evaluate the model.
9. Save the trained model.
10. Integrate the model with the Flask backend.

**Recommended evaluation metrics:**

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- Per-class performance

Use patient-level separation between training, validation and test datasets to reduce data leakage.

---

## 💬 5. Real-Time Doctor–Patient Messenger

The application includes a built-in messenger that allows patients and doctors to communicate directly.

The messaging functionality is implemented using **Flask-SocketIO** and the Socket.IO client.

### Patient Messenger

- View assigned doctor.
- Send messages directly.
- Receive real-time responses.
- View previous conversations.
- Share retinal report references.
- View message timestamps.
- Receive notifications.

### Doctor Messenger

- View assigned patient conversations.
- Reply to patient messages.
- Access patient reports during consultations.
- Share medical recommendations.
- Send appointment updates.
- View conversation history.

### Messaging Architecture

```text
       PATIENT PORTAL
              |
              v
        SEND MESSAGE
              |
              v
       SOCKET.IO CLIENT
              |
              v
       FLASK-SOCKETIO
              |
              v
       MESSAGE VALIDATION
              |
              v
           DATABASE
              |
              v
        REAL-TIME EVENT
              |
              v
        DOCTOR PORTAL
```

**Security requirements:**

- Only authenticated users can send messages.
- Patients can access their own conversations.
- Doctors can access conversations with their assigned patients.
- Messages must be stored securely.
- Unauthorized conversation access must be rejected.

---

## 📊 6. AI-Generated Retinal Analysis Report

Once the patient uploads a retinal image, the system generates an analysis report.

### Report Information

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
- Doctor Review Status
- Doctor's Observations
- Doctor's Recommendations

### Sample Report

```text
==========================================
       RETINAL IMAGE ANALYSIS REPORT
==========================================

Patient ID: PAT001
Report ID: REP001
Date: DD-MM-YYYY

AI CLASSIFICATION RESULTS

Normal                     : 10%
Glaucoma                   : 15%
Diabetic Retinopathy       : 65%
Hypertensive Retinopathy   : 10%

Top Predicted Category:
Diabetic Retinopathy

Model Confidence:
65%

Doctor Review:
Pending

==========================================
AI-generated screening result.
Not a confirmed medical diagnosis.
==========================================
```

Reports can be generated using Python ReportLab and downloaded as PDF documents.

---

## 🏗️ 7. Technology Stack

### Frontend

| Technology | Usage |
|---|---|
| HTML5 | Webpage structure |
| CSS3 | Styling and responsive design |
| JavaScript | Frontend functionality |
| React.js | Component-based frontend |
| React Router | Navigation between portals |
| Axios | Backend API communication |
| Socket.IO Client | Real-time messaging |

### Backend

| Technology | Usage |
|---|---|
| Python | Backend programming |
| Flask | Backend web framework |
| Flask-CORS | Cross-origin API communication |
| Flask-JWT-Extended | Authentication |
| Flask-SQLAlchemy | Database operations |
| Flask-SocketIO | Real-time communication |
| Werkzeug | Secure image upload handling |

### AI and Machine Learning

| Technology | Usage |
|---|---|
| TensorFlow | Deep Learning framework |
| Keras | CNN model development |
| EfficientNetB0 | Image classification architecture |
| NumPy | Numerical operations |
| OpenCV | Image preprocessing |
| Pillow | Image processing |
| Scikit-learn | Model evaluation |
| Matplotlib | Visualization |

### Database and Tools

| Technology | Usage |
|---|---|
| MySQL | Relational database |
| ReportLab | PDF report generation |
| Git | Version control |
| GitHub | Source code management |
| VS Code | Development environment |
| Postman | API testing |

**Architecture decision:** React.js is the frontend framework, while Python Flask is the only backend framework. HTML5 and CSS3 are used within the React frontend.

---

## 🏛️ 8. System Architecture

The project follows a modular three-tier architecture.

```text
                 USERS
                   |
       +-----------+-----------+
       |           |           |
    PATIENT      DOCTOR       ADMIN
     PORTAL      PORTAL       PORTAL
       |           |           |
       +-----------+-----------+
                   |
             REACT FRONTEND
                   |
             AXIOS / SOCKET.IO
                   |
           PYTHON FLASK BACKEND
                   |
       +-----------+-----------+
       |           |           |
   AUTH MODULE  AI MODULE  MESSAGING
       |           |           |
       |       TENSORFLOW   SOCKET.IO
       |        CNN MODEL      |
       |           |           |
       +-----------+-----------+
                   |
                DATABASE
                   |
       +-----------+-----------+
       |           |           |
    PATIENT      DOCTOR      REPORTS
    RECORDS      RECORDS     HISTORY
```

### Architecture Components

- **Presentation Layer:** React.js, HTML5 and CSS3.
- **Application Layer:** Python Flask.
- **AI Layer:** TensorFlow and Keras.
- **Communication Layer:** Flask-SocketIO.
- **Data Layer:** MySQL and SQLAlchemy.
- **Report Layer:** Python ReportLab.

---

## 🗄️ 9. Database Design

The application uses MySQL to store user accounts, patient records, prediction history, appointments and conversations.

### Main Database Tables

| Table Name | Purpose |
|---|---|
| users | Login and authentication details |
| patients | Patient profile information |
| doctors | Doctor profile information |
| doctor_patient | Doctor–patient assignments |
| retinal_images | Uploaded retinal images |
| predictions | AI prediction results |
| reports | Generated reports |
| appointments | Appointment information |
| conversations | Chat conversation records |
| messages | Individual messages |
| prescriptions | Medical prescriptions |
| notifications | User notifications |

### Database Relationships

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
```

---

## 📁 10. Recommended Project Folder Structure

```text
AI-Retinal-Classification/
│
├── frontend/
│   ├── public/
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
│   │   │   └── PredictionChart.jsx
│   │   │
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── Register.jsx
│   │   │   │
│   │   │   ├── patient/
│   │   │   │   ├── PatientDashboard.jsx
│   │   │   │   ├── UploadImage.jsx
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
│   ├── generated_reports/
│   └── requirements.txt
│
├── database/
│   └── schema.sql
│
├── docs/
│   └── architecture.png
│
├── .env.example
├── .gitignore
└── README.md
```

---

## 🔗 11. Backend API Endpoints

### Authentication

| Method | Endpoint | Description |
|---|---|---|
| POST | /api/auth/register | Register user |
| POST | /api/auth/login | Login user |
| POST | /api/auth/logout | Logout user |
| GET | /api/auth/profile | Get user profile |

### Patient

| Method | Endpoint | Description |
|---|---|---|
| GET | /api/patient/dashboard | Patient dashboard |
| POST | /api/patient/upload | Upload retinal image |
| GET | /api/patient/reports | View reports |
| GET | /api/patient/history | Prediction history |
| GET | /api/patient/doctors | Assigned doctors |

### Doctor

| Method | Endpoint | Description |
|---|---|---|
| GET | /api/doctor/dashboard | Doctor dashboard |
| GET | /api/doctor/patients | Assigned patients |
| GET | /api/doctor/reports | Patient reports |
| POST | /api/doctor/recommendation | Add recommendation |
| POST | /api/doctor/prescription | Create prescription |

### Admin

| Method | Endpoint | Description |
|---|---|---|
| GET | /api/admin/dashboard | Admin dashboard |
| GET | /api/admin/patients | View patients |
| GET | /api/admin/doctors | View doctors |
| PUT | /api/admin/doctors/:id/approve | Approve doctor |
| DELETE | /api/admin/users/:id | Delete user |

### AI Prediction

| Method | Endpoint | Description |
|---|---|---|
| POST | /api/prediction/classify | Classify retinal image |
| GET | /api/prediction/history | Prediction history |
| GET | /api/prediction/:id | Prediction details |

### Messaging

| Method | Endpoint | Description |
|---|---|---|
| GET | /api/messages/conversations | Get conversations |
| GET | /api/messages/:id | Get messages |
| POST | /api/messages/send | Send message |

Real-time message events are handled through Flask-SocketIO.

---

## ⚙️ 12. Installation and Execution

### Prerequisites

Install:

- Python 3.10 or 3.11
- Node.js and npm
- MySQL
- Visual Studio Code
- Git

### Step 1: Clone Repository

```bash
git clone https://github.com/your-username/AI-Retinal-Classification.git

cd AI-Retinal-Classification
```

### Step 2: Backend Environment Setup

```bash
cd backend

python -m venv venv
```

Activate virtual environment on Windows:

```bash
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

### Step 3: Environment Configuration

Create a `.env` file.

```env
SECRET_KEY=your-secret-key
JWT_SECRET_KEY=your-jwt-secret

DATABASE_URL=mysql+pymysql://root:password@localhost/retinal_ai

UPLOAD_FOLDER=uploads/retinal_images

MODEL_PATH=ai_model/retinal_model.keras
```

Configure the database and credentials according to your local setup.

### Step 4: Run Flask Backend

```bash
python app.py
```

Backend URL:

```text
http://127.0.0.1:5000
```

### Step 5: Frontend Setup

Open another terminal.

```bash
cd frontend

npm install
```

Start React:

```bash
npm run dev
```

Frontend URL:

```text
http://localhost:5173
```

---

## 📦 13. Python Dependencies

Create `backend/requirements.txt`.

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
```

Install all dependencies:

```bash
pip install -r requirements.txt
```

Use package versions compatible with the selected Python and TensorFlow versions.

---

## 🔐 14. Security Implementation

The application handles sensitive healthcare information, so security must be implemented at every layer.

- Password hashing.
- JWT authentication.
- Role-based access control.
- Patient and doctor authorization.
- Secure image upload validation.
- Unique filenames for uploaded images.
- Protected report downloads.
- Restricted messenger conversations.
- Environment-based secret management.
- HTTPS for deployment.
- Audit logging.
- Patient consent and data privacy controls.

---

## 🧪 15. Model Evaluation

The AI model should be evaluated using a separate test dataset.

Recommended metrics:

| Metric | Purpose |
|---|---|
| Accuracy | Overall classification performance |
| Precision | Correct positive predictions |
| Recall | Ability to identify positive samples |
| F1-score | Balance between precision and recall |
| Confusion Matrix | Class-wise prediction performance |

Evaluate each of the four categories independently, particularly the false-negative rate, because missed retinal abnormalities can have serious consequences.

---

## 🔮 16. Future Enhancements

- Advanced EfficientNet and ResNet architectures.
- Grad-CAM-based retinal image visualization.
- Real-time video consultation.
- Mobile application.
- Cloud-based image storage.
- Email and notification integration.
- Multilingual support.
- Advanced doctor analytics.
- Improved AI model calibration.
- External clinical validation.
- Integration with electronic health records.

---

## 🎓 17. Expected Outcome

The project aims to deliver a centralized AI-powered retinal screening and healthcare management platform.

The completed application will provide:

- Three independent user portals.
- Secure patient and doctor authentication.
- TensorFlow-based four-class retinal classification.
- Percentage-based model confidence results.
- Patient retinal image upload.
- AI-generated PDF reports.
- Doctor report review.
- Real-time doctor–patient communication.
- Appointment management.
- Centralized administration.

---

## 👨‍💻 18. Project Information

| Field | Details |
|---|---|
| Project Title | AI-Based Retinal Image Classification for Early Detection of Eye Diseases |
| Project Type | Mini Project |
| Domain | Artificial Intelligence and Healthcare |
| Frontend | React.js, HTML5, CSS3, JavaScript |
| Backend | Python Flask |
| AI Framework | TensorFlow / Keras |
| Model | EfficientNetB0 / CNN |
| Database | MySQL |
| Messaging | Flask-SocketIO |
| Report Generation | ReportLab |

---

## 📜 19. Disclaimer

This project is developed for academic and research purposes. The AI model provides preliminary image-classification results and must not be considered a substitute for professional medical diagnosis.

All AI-generated results must be reviewed by a qualified ophthalmologist. Clinical use requires appropriate dataset validation, model testing, calibration, and regulatory assessment.

---

<p align="center">
  <b>AI-Based Retinal Image Classification for Early Detection of Eye Diseases</b>
  <br/>
  <i>Bringing Artificial Intelligence and Healthcare Together for Early Retinal Disease Screening.</i>
</p>
