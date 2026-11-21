# Smart Clinic Management System Database Design

## MySQL Database Design

### Table: patients

- patient_id: BIGINT, Primary Key, Auto Increment
- first_name: VARCHAR(50), Not Null
- last_name: VARCHAR(50), Not Null
- date_of_birth: DATE, Not Null
- email: VARCHAR(100), Unique, Not Null
- phone: VARCHAR(20), Not Null

Comment:
- Patient records should be retained for appointment history.

---

### Table: doctors

- doctor_id: BIGINT, Primary Key, Auto Increment
- first_name: VARCHAR(50), Not Null
- last_name: VARCHAR(50), Not Null
- specialization: VARCHAR(100), Not Null
- email: VARCHAR(100), Unique, Not Null
- phone: VARCHAR(20), Not Null

Comment:
- Doctors should not have overlapping appointments.

---

### Table: appointments

- appointment_id: BIGINT, Primary Key, Auto Increment
- doctor_id: BIGINT, Foreign Key → doctors(doctor_id)
- patient_id: BIGINT, Foreign Key → patients(patient_id)
- appointment_time: DATETIME, Not Null
- status: INT (0 = Scheduled, 1 = Completed, 2 = Cancelled)

Comment:
- Appointments connect patients and doctors.
- Appointment history should remain available for reporting purposes.

---

### Table: admin

- admin_id: BIGINT, Primary Key, Auto Increment
- username: VARCHAR(50), Unique, Not Null
- password: VARCHAR(255), Not Null
- email: VARCHAR(100), Unique, Not Null

Comment:
- Admin users manage doctors, patients, and appointments.

---

## Relationship Summary

- One patient can have many appointments.
- One doctor can have many appointments.
- Each appointment belongs to one patient.
- Each appointment belongs to one doctor.

---

## MongoDB Collection Design

### Collection: prescriptions

```json
{
  "_id": "ObjectId('64abc123456')",
  "patientId": 101,
  "doctorId": 12,
  "appointmentId": 51,
  "diagnosis": "Seasonal Flu",
  "medications": [
    {
      "name": "Paracetamol",
      "dosage": "500mg",
      "frequency": "Every 6 hours"
    },
    {
      "name": "Vitamin C",
      "dosage": "1000mg",
      "frequency": "Once daily"
    }
  ],
  "doctorNotes": "Drink plenty of water and rest.",
  "refillCount": 2,
  "tags": [
    "flu",
    "follow-up"
  ],
  "metadata": {
    "createdBy": "doctor12",
    "priority": "normal"
  }
}
```

### Design Justification

- MySQL is used for structured data such as patients, doctors, appointments, and administrators.
- Foreign key relationships ensure data integrity.
- MongoDB is used for prescriptions because medication lists and doctor notes can vary significantly between patients.
- Nested documents and arrays make MongoDB suitable for storing prescription details and metadata.
