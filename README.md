# 🏥 MEDSUM

> An AI-powered Hospital Management System that simplifies patient management, appointment scheduling, and medical report analysis through intelligent automation.

---

## 📖 Overview

MEDSUM is a full-stack hospital management system developed as a college team project to improve the efficiency of hospital workflows. The application provides separate dashboards for patients, doctors, and administrators, allowing each user to perform tasks specific to their role.

One of the key features of the project is the integration of the Groq AI API, which analyzes uploaded medical reports and generates concise summaries along with important action points. This helps doctors quickly review patient reports while reducing the time spent reading lengthy medical documents.

The project was designed with the objective of combining traditional hospital management features with AI-assisted healthcare support in a simple and user-friendly interface.

---

## ✨ Features

- Secure role-based login system
- Separate dashboards for Patients, Doctors, and Admin
- Online appointment booking
- AI-powered medical report summarization
- Medical report upload (PDF and Images)
- Patient medical history management
- Doctor consultation dashboard
- Appointment approval workflow
- User management for administrators
- Responsive user interface

---

## 👥 User Roles

### Patient

- Register and log in
- Book appointments with doctors
- Upload medical reports
- Maintain medical history
- View appointment status

### Doctor

- View assigned appointments
- Access patient medical history
- Review AI-generated report summaries
- Add consultation notes and diagnosis

### Admin

- Manage users
- Review appointment requests
- Approve or reject appointments
- Monitor hospital activities

---

## 🧠 AI Integration

MEDSUM uses the **Groq API** to process uploaded medical reports.

After a patient uploads a report, the system:

- Extracts relevant medical information
- Generates a concise diagnosis summary
- Identifies important action points
- Makes the summarized report available to both the patient and the assigned doctor

This feature helps improve accessibility to medical information and assists doctors in reviewing reports more efficiently.

---

## 🛠️ Technology Stack

| Category | Technology |
|-----------|------------|
| Frontend | HTML5, CSS3, JavaScript |
| Backend | Node.js, Express.js |
| AI Service | Groq API |
| File Upload | Multer |
| Database | JSON (`data.json`) |
| Version Control | Git & GitHub |

---

## 📂 Project Structure

```
MEDSUM/
│
├── frontend/
├── backend/
├── uploads/
├── data/
├── README.md
└── package.json
```

---

## 🔄 Project Workflow

1. Patient logs into the system.
2. An appointment is requested with a selected doctor.
3. The patient uploads medical reports if required.
4. The report is analyzed using the Groq AI API.
5. The generated summary is stored with the patient's details.
6. The administrator reviews and approves the appointment.
7. The doctor receives the confirmed appointment.
8. The doctor reviews the patient's profile and AI summary before consultation.
9. Consultation notes are recorded for future reference.

---

## 🚀 Future Improvements

The current project represents the MVP (Minimum Viable Product). Future enhancements may include:

- PostgreSQL or MongoDB integration
- JWT-based authentication
- Real-time notifications using Socket.io
- Video consultation using WebRTC
- Email notifications
- Electronic Health Record (EHR) support
- Mobile application

---

## 🤝 Team

This project was developed as a collaborative college project.

Each team member contributed to different parts of the system, including planning, frontend development, backend development, AI integration, testing, and documentation.

---

## 📄 Documentation

Detailed software requirements and system specifications are available in the project documentation.

- Software Requirements Specification (SRS)

---

## 📜 License

This project is intended for educational purposes.
