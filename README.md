#FastAPI Appointment Scheduler 📄

# 🚀 Overview

This is a FastAPI-based appointment scheduling API that allows users to:

- 📌 Create new appointments
- 📄 Generate PDF confirmations
- 🔍 Retrieve appointment details
- 📜 List all scheduled appointments

# 🛠 Features

- ✅ RESTful API with FastAPI
- 📂 PDF appointment confirmation
- 🔢 Unique reference ID for each appointment
- 📞 Phone number validation (India: +91 format)
- 🗂 In-memory storage (can be replaced with a database)

# 📦 Installation

```sh
pip install -r requirements.txt
```

# ▶️ Running the API

```sh
uvicorn api:app --reload
```

# 🔗 API Endpoints

### 1️⃣ Create an Appointment

**POST /appointments/**

```json
{
  "patient_name": "John Doe",
  "contact_number": "+911234567890"
}
```

*Response:*

```json
{
  "reference_id": "APT-0001",
  "status": "confirmed",
  "message": "Appointment scheduled successfully",
  "pdf_path": "appointment_pdfs/appointment_APT-0001.pdf"
}
```

### 2️⃣ Get Appointment by Reference ID

**GET /appointments/{reference\_id}**

### 3️⃣ List All Appointments

**GET /appointments/**

## 📜 Requirements

Create a `requirements.txt` file with the following dependencies:

```txt
fastapi
uvicorn
pydantic
reportlab
```

## 🏁 License

This project is licensed under the Apache 2.0 License. 🚀

