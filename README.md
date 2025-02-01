# 🏥 **FASTAPI APPOINTMENT SCHEDULER 📄**

## 🚀 **OVERVIEW**

This is a **FastAPI-based** appointment scheduling API that allows users to:

- 📌 **Create new appointments**
- 📄 **Generate PDF confirmations**
- 🔍 **Retrieve appointment details**
- 📜 **List all scheduled appointments**

## 🛠 **FEATURES**

- ✅ **RESTful API with FastAPI**
- 📂 **PDF appointment confirmation**
- 🔢 **Unique reference ID for each appointment**
- 📞 **Phone number validation (India: +91 format)**
- 🗂 **In-memory storage (can be replaced with a database)**

## 📦 **INSTALLATION**

```sh
pip install -r requirements.txt
```

## ▶️ **RUNNING THE API**

```sh
uvicorn api:app --reload
```

## 🔗 **API ENDPOINTS**

### 1️⃣ **CREATE AN APPOINTMENT**

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

### 2️⃣ **GET APPOINTMENT BY REFERENCE ID**

**GET /appointments/{reference_id}**

### 3️⃣ **LIST ALL APPOINTMENTS**

**GET /appointments/**

## 📜 **REQUIREMENTS**

Create a `requirements.txt` file with the following dependencies:

```txt
fastapi
uvicorn
pydantic
reportlab
```

## 🏁 **LICENSE**

This project is licensed under the **Apache 2.0 License**. 🚀
