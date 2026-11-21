# User Story Template

**Title:**
_As a [user role], I want [feature/goal], so that [reason]._

**Acceptance Criteria:**
1. [Criteria 1]
2. [Criteria 2]
3. [Criteria 3]

**Priority:** [High/Medium/Low]

**Story Points:** [Estimated Effort in Points]

**Notes:**
- [Additional information or edge cases]

---

## Admin User Stories

### User Story 1

**Title:**
_As an admin, I want to log into the portal, so that I can manage the platform securely._

**Acceptance Criteria:**
1. The admin can enter username and password.
2. The system validates credentials.
3. The admin dashboard is displayed after successful login.

**Priority:** High

**Story Points:** 3

**Notes:**
- Authentication must be secure.

---

### User Story 2

**Title:**
_As an admin, I want to log out of the portal, so that I can protect system access._

**Acceptance Criteria:**
1. The admin can click the logout button.
2. The session is terminated.
3. The login page is displayed.

**Priority:** High

**Story Points:** 2

**Notes:**
- The authentication token should be invalidated.

---

### User Story 3

**Title:**
_As an admin, I want to add doctors to the portal, so that doctors can access the system._

**Acceptance Criteria:**
1. The admin can enter doctor information.
2. The doctor profile is saved successfully.
3. The doctor appears in the doctor list.

**Priority:** High

**Story Points:** 5

**Notes:**
- Email addresses must be unique.

---

### User Story 4

**Title:**
_As an admin, I want to delete doctor's profiles from the portal, so that outdated records can be removed._

**Acceptance Criteria:**
1. The admin can select a doctor profile.
2. The system asks for confirmation.
3. The profile is deleted successfully.

**Priority:** Medium

**Story Points:** 3

**Notes:**
- Existing appointments must be handled appropriately.

---

### User Story 5

**Title:**
_As an admin, I want to run a stored procedure in MySQL CLI to get the number of appointments per month, so that I can track usage statistics._

**Acceptance Criteria:**
1. The stored procedure executes successfully.
2. Monthly statistics are returned.
3. Results are displayed correctly.

**Priority:** Medium

**Story Points:** 4

**Notes:**
- Uses MySQL stored procedures.

---

## Patient User Stories

### User Story 1

**Title:**
_As a patient, I want to view a list of doctors without logging in, so that I can explore options before registering._

**Acceptance Criteria:**
1. The doctor list is publicly accessible.
2. Doctor names are displayed.
3. Specializations are displayed.

**Priority:** Medium

**Story Points:** 2

**Notes:**
- No authentication required.

---

### User Story 2

**Title:**
_As a patient, I want to sign up using my email and password, so that I can book appointments._

**Acceptance Criteria:**
1. The patient can enter registration details.
2. Email validation is performed.
3. The account is created successfully.

**Priority:** High

**Story Points:** 5

**Notes:**
- Password requirements must be enforced.

---

### User Story 3

**Title:**
_As a patient, I want to log into the portal, so that I can manage my bookings._

**Acceptance Criteria:**
1. The patient can enter credentials.
2. Credentials are validated.
3. The patient dashboard is displayed.

**Priority:** High

**Story Points:** 3

**Notes:**
- JWT authentication should be used.

---

### User Story 4

**Title:**
_As a patient, I want to log out of the portal, so that I can secure my account._

**Acceptance Criteria:**
1. The patient can click logout.
2. The session is terminated.
3. The login page is displayed.

**Priority:** High

**Story Points:** 2

**Notes:**
- Session data should be cleared.

---

### User Story 5

**Title:**
_As a patient, I want to book an hour-long appointment to consult with a doctor._

**Acceptance Criteria:**
1. Available doctors are displayed.
2. Available appointment slots are shown.
3. The booking is saved successfully.

**Priority:** High

**Story Points:** 5

**Notes:**
- Appointment duration is one hour.

---

### User Story 6

**Title:**
_As a patient, I want to view my upcoming appointments, so that I can prepare accordingly._

**Acceptance Criteria:**
1. Upcoming appointments are listed.
2. Appointment details are displayed.
3. Only future appointments are shown.

**Priority:** Medium

**Story Points:** 3

**Notes:**
- Patients can only view their own appointments.

---

## Doctor User Stories

### User Story 1

**Title:**
_As a doctor, I want to log into the portal, so that I can manage my appointments._

**Acceptance Criteria:**
1. The doctor can enter credentials.
2. Credentials are validated.
3. The doctor dashboard is displayed.

**Priority:** High

**Story Points:** 3

**Notes:**
- Access is role-based.

---

### User Story 2

**Title:**
_As a doctor, I want to log out of the portal, so that I can protect my data._

**Acceptance Criteria:**
1. The doctor can click logout.
2. The session is terminated.
3. The login page is displayed.

**Priority:** High

**Story Points:** 2

**Notes:**
- Session data should be cleared.

---

### User Story 3

**Title:**
_As a doctor, I want to view my appointment calendar, so that I can stay organized._

**Acceptance Criteria:**
1. The calendar displays all appointments.
2. Patient information is visible.
3. Upcoming appointments are highlighted.

**Priority:** High

**Story Points:** 5

**Notes:**
- Calendar view should be easy to navigate.

---

### User Story 4

**Title:**
_As a doctor, I want to mark my unavailability, so that patients can only see available slots._

**Acceptance Criteria:**
1. The doctor can define unavailable dates.
2. Unavailable slots are blocked.
3. Patients cannot book blocked slots.

**Priority:** Medium

**Story Points:** 4

**Notes:**
- Existing appointments remain unaffected.

---

### User Story 5

**Title:**
_As a doctor, I want to update my profile with specialization and contact information, so that patients have up-to-date information._

**Acceptance Criteria:**
1. The doctor can edit profile information.
2. Changes are saved successfully.
3. Updated information is displayed to patients.

**Priority:** Medium

**Story Points:** 3

**Notes:**
- Includes specialization and contact details.

---

### User Story 6

**Title:**
_As a doctor, I want to view patient details for upcoming appointments, so that I can be prepared._

**Acceptance Criteria:**
1. Patient information is accessible before appointments.
2. Appointment details are visible.
3. Access is granted only to authorized doctors.

**Priority:** High

**Story Points:** 4

**Notes:**
- Must comply with patient privacy requirements.
