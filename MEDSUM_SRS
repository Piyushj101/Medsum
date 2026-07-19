# Software Requirements Specification (SRS)
## AI-Driven Hospital Management System (MEDSUM)

---

## 1. Introduction

### 1.1 Purpose
The purpose of this document is to define the full system architecture, functionality, and constraints for the "MEDSUM" AI-Driven Hospital Management System. This document serves as the absolute blueprint for developers, project managers, and stakeholders to understand how the AI analysis, clinical workflow, and appointment scheduling synchronize across diverse medical roles.

### 1.2 Scope
MEDSUM is an MVP healthcare platform that digitizes hospital intake, doctor assignments, and clinical report management. The system employs an integration loop with Groq AI API (LLM analysis) to autonomously scan, summarize, and extract critical action items from dense medical reports (PDFs, images) uploaded by patients. 

### 1.3 Definitions and Acronyms
- **SRS**: Software Requirements Specification
- **LLM**: Large Language Model
- **Groq API**: High-speed AI inference provider powering the automated diagnosis summarization
- **Admin**: Superuser responsible for managing the routing of patients to doctors
- **MVP**: Minimum Viable Product

---

## 2. Overall Description

### 2.1 Product Perspective
The system is built as a highly responsive Vanilla JavaScript single-page application (frontend) communicating autonomously with an Express.js (Node) RESTful backend. Given the MVP status, databases are securely simulated using local `data.json` storage to maintain extremely rapid deployment agility.

### 2.2 User Characteristics
The platform operates on a rigid 3-tier Role-Based Access Control (RBAC) model:

1. **Patient**: Books appointments, enters chronic condition, medication and allergy context, and uploads raw diagnostic files.
2. **Doctor**: Reviews assigned appointments, analyzes LLM-summarized intelligence overviews of the PDFs, reviews historical context via the Full Profile overlay, and submits clinical notes/diagnosis status.
3. **Admin**: Highest level override. Monitors the active queue, manually approves/rejects appointments securely, and handles the registration and deletion of users across all roles natively.

### 2.3 Operating Environment
- **Backend:** Node.js, Express.js, Multer (file parsing).
- **Frontend:** Vanilla HTML5, CSS3 (Custom Vercel-glassmorphism CSS grid architecture), JavaScript (Fetch API).
- **AI Integration:** Groq SDK for seamless LLM context generation.
- **Database:** Flat file JSON database schema (`data.json`) utilizing asynchronous FS read/write locks.

---

## 3. System Features

### 3.1 Role-Based Authentication
**Description:** Centralized secure login gateway.
- Users authenticate via standard credentials.
- The server dynamically routes the user to `/patient`, `/doctor`, or `/admin` endpoints based on the encoded role.

### 3.2 AI Diagnostic Analyzer (Groq Integration)
**Description:** Automated report parsing and contextual extraction.
- Patients securely upload `.pdf`, `.jpg`, or `.png` medical files.
- The Node backend routes the file to the Groq API endpoint for heavy OCR analysis.
- The LLM extracts the core **Diagnosis** and a mapped array of **Action Points**.
- Output is rendered natively into the Patient and Doctor perfectly squared grid matrix.

### 3.3 Dynamic 1:1 Appointment Booking Engine
**Description:** Highly orchestrated scheduling engine.
- Patients dynamically fetch all available registered Doctors from the database via a dropdown.
- Patients formulate a date, time, and specific reason for visit.
- The ticket immediately enters the Admin's "Pending" grid.
- Admin evaluates, sets status to "Confirmed," seamlessly transferring the physical timeline ticket into the respective Doctor's private consultation queue.

### 3.4 Unified Doctor Profiling Modal
**Description:** An ultra-premium UI architectural popup that builds the patient's entire medical timeline.
- Combines the Patient's raw **Conditions, Medications, Allergies, and Notes** dynamically from the database.
- Renders their entire Appointment history (Past visits vs Future visits).
- Exposes historical AI summaries and instant PDF retrieval links inside a single frosted-glass overview overlay.

### 3.5 Administrative Root Management
**Description:** Complete top-down grid management over system data.
- Admins possess a live table capable of instantly spinning up natively categorized users (New Doctors, Patients).
- Rapid user demolition (Deletion tool fully scrubs medical history to preserve database integrity securely).

---

## 4. Non-Functional Requirements

### 4.1 UI / UX Standards & Aesthetics
- **Architecture:** Must adhere to modern Silicon Valley visual standards.
- **Grid Layouts:** Strict 1:1 Aspect Ratio grid mapping for data-heavy sections (like Patient AI Reports and Doctor Report Queues).
- **Aesthetic:** High-friction Glassmorphism (Backdrop filters `blur(20px)`), frosted UI layers, variable mesh background gradients, fluid inline animations.
- **Typography:** Implementation of *Plus Jakarta Sans* to elevate readability.
- **Responsive:** Fluid layout using Flexbox and Grid arrays that adapt efficiently on scale.

### 4.2 Application Performance Parameters
- Fetch API interactions must leverage `async/await` concurrently.
- No page reloads allowed during inter-tab navigation to simulate seamless React-like routing dynamically via vanilla JS manipulation.

### 4.3 Security & Data Integrity
- File uploads are securely firewalled dynamically via standard `Multer` MIME-type filters (blocking binaries apart from verified docs/images).
- JSON flat file commits are wrapped tightly in exception loops guaranteeing atomic integrity.
- Hidden internal User IDs obfuscated behind semantic alias displays securely during profile mapping loops.

---

## 5. Future Engineering Scope
- Transitioning `data.json` natively to PostgreSQL / MongoDB schemas.
- Integrating a WebRTC video-calling layer natively inside the confirmed Doctor Appointment queues.
- Real-time Socket.io updates for instantaneous notification triggers globally between admin verifications and patient queues.
