# Hospital Management System - EMR Forms Collection

A comprehensive collection of 15 JSON form configurations for a complete Hospital/Electronic Medical Records (EMR) management system.

## Form List

### 1. Patient Registration Form (`01_patient_registration.json`)
**Category:** Registration  
**Purpose:** Initial patient registration with personal information, contact details, emergency contacts, insurance, and basic medical history.

**Key Sections:**
- Personal Information
- Contact Details
- Emergency Contact
- Insurance Information
- Medical History Summary

---

### 2. Appointment Scheduling Form (`02_appointment_scheduling.json`)
**Category:** Scheduling  
**Purpose:** Schedule patient appointments with departments, doctors, and manage visit details.

**Key Sections:**
- Patient Details
- Appointment Information
- Visit Details
- Special Requirements

---

### 3. Emergency Department Triage Form (`03_emergency_triage.json`)
**Category:** Emergency  
**Purpose:** Rapid assessment and prioritization of emergency patients with vital signs and triage level.

**Key Sections:**
- Patient Identification
- Arrival Information
- Vital Signs
- Chief Complaint
- Pain Assessment
- Triage Assessment
- Initial Actions

---

### 4. Medical Consultation Form (`04_medical_consultation.json`)
**Category:** Clinical  
**Purpose:** Document patient consultations, examinations, diagnoses, and treatment plans.

**Key Sections:**
- Patient Information
- Consultation Details
- Chief Complaint
- History (HPI, Past Medical, Family, Social)
- Physical Examination
- Assessment & Diagnosis
- Treatment Plan
- Follow-up

---

### 5. Laboratory Test Request Form (`05_laboratory_test_request.json`)
**Category:** Diagnostics  
**Purpose:** Order laboratory tests with comprehensive test categories and sample information.

**Key Sections:**
- Patient Details
- Requesting Physician
- Test Information (Hematology, Chemistry, Microbiology, Serology, etc.)
- Sample Information
- Clinical Details

---

### 6. Radiology & Imaging Request Form (`06_radiology_imaging_request.json`)
**Category:** Diagnostics  
**Purpose:** Request imaging studies with contrast safety screening and detailed examination specifications.

**Key Sections:**
- Patient Information
- Requesting Physician
- Examination Details (X-Ray, CT, MRI, Ultrasound, etc.)
- Clinical Information
- Contrast & Safety Screening

---

### 7. Prescription Form (`07_prescription.json`)
**Category:** Medication  
**Purpose:** Prescribe medications with dosage, frequency, and patient instructions.

**Key Sections:**
- Patient Information
- Prescriber Information
- Medication Details (supports multiple medications)
- Instructions & Precautions
- Refill & Validity

---

### 8. Hospital Admission Form (`08_hospital_admission.json`)
**Category:** Admission  
**Purpose:** Admit patients to hospital with clinical information, room assignment, and consent tracking.

**Key Sections:**
- Admission Details
- Patient Information
- Admission Source
- Clinical Information
- Room Assignment
- Insurance & Billing
- Consent

---

### 9. Discharge Summary Form (`09_discharge_summary.json`)
**Category:** Discharge  
**Purpose:** Comprehensive discharge documentation including hospital course, treatments, and follow-up plan.

**Key Sections:**
- Patient Information
- Admission Details
- Hospital Course
- Diagnosis (Primary & Secondary)
- Procedures & Investigations
- Treatment Summary
- Discharge Details
- Follow-up Instructions

---

### 10. Nursing Assessment Form (`10_nursing_assessment.json`)
**Category:** Nursing  
**Purpose:** Regular nursing documentation of patient status, vital signs, and care provided.

**Key Sections:**
- Patient Information
- Vital Signs
- Physical Assessment (System-by-system)
- Pain Assessment
- Medication Administration
- Intake & Output
- Nursing Interventions
- Patient Safety (Fall risk, Pressure ulcers)

---

### 11. Surgery & Procedure Consent Form (`11_surgery_consent.json`)
**Category:** Consent  
**Purpose:** Legal consent for surgical procedures with detailed risk disclosure and authorization.

**Key Sections:**
- Patient Information
- Procedure Details
- Physician Information
- Consent Declaration
- Risks & Benefits
- Alternatives
- Anesthesia
- Witness & Signatures

---

### 12. Operative Report Form (`12_operative_report.json`)
**Category:** Surgery  
**Purpose:** Detailed documentation of surgical procedures, findings, and post-operative plan.

**Key Sections:**
- Patient & Procedure Information
- Pre-Operative Diagnosis
- Post-Operative Diagnosis
- Procedure Performed
- Surgical Team
- Anesthesia Details
- Operative Findings
- Procedure Description (detailed step-by-step)
- Specimens
- Complications
- Post-Operative Plan

---

### 13. Death Certificate Form (`13_death_certificate.json`)
**Category:** Legal  
**Purpose:** Legal documentation of death with cause, manner, and certifying physician information.

**Key Sections:**
- Deceased Information
- Death Details
- Cause of Death (with chain of events)
- Medical Certifier
- Disposition

---

### 14. Birth Certificate & Delivery Record (`14_birth_certificate.json`)
**Category:** Obstetrics  
**Purpose:** Document birth details, newborn assessment, and create birth certificate.

**Key Sections:**
- Newborn Information
- Mother Information
- Father Information
- Birth Details
- Delivery Details
- Newborn Assessment (APGAR, interventions)
- Certifier Information

---

### 15. Medical Record Transfer Request Form (`15_medical_record_transfer.json`)
**Category:** Medical Records  
**Purpose:** Request transfer of medical records with proper authorization and security.

**Key Sections:**
- Patient Information
- Requestor Information
- Records Requested
- Destination Information
- Authorization

---

## Form Structure

Each form follows this JSON structure:

```json
{
  "formTitle": "Form Name",
  "formId": "FORM-XXX",
  "category": "Category Name",
  "sections": ["Section 1", "Section 2", ...],
  "fields": [
    {
      "type": "text|textarea|number|checkbox|radio|dropdown|date|display",
      "label": "Field Label",
      "section": "Section Name",
      "priority": "normal|critical|optional",
      "required": false,
      "options": [...] // for radio/dropdown/checkbox
      // Additional field-specific properties
    }
  ]
}
```

## Field Types Supported

- **text**: Single-line text input
- **textarea**: Multi-line text input
- **number**: Numeric input with min/max validation
- **checkbox**: Multiple selection options
- **radio**: Single selection from options
- **dropdown**: Select from dropdown list
- **date**: Date picker
- **display**: Static display text (for instructions/declarations)

## Priority Levels

- **critical**: Must-have fields for form completion
- **normal**: Important but not absolutely critical
- **optional**: Nice-to-have, additional information

## Usage Notes

1. **No Required Fields**: All forms have `required: false` as per your specification - implement validation logic in your frontend as needed
2. **Flexible Structure**: Forms can be easily extended by adding new fields
3. **Section Organization**: Fields are organized into logical sections for better UX
4. **Comprehensive Coverage**: Forms cover the complete patient journey from registration to discharge (and beyond)
5. **Compliance Ready**: Forms include fields commonly required for healthcare compliance and legal requirements

## Implementation Suggestions

1. **Database Schema**: Use form structure to auto-generate database tables
2. **Dynamic Form Rendering**: Parse JSON to dynamically render forms in your UI
3. **Validation**: Implement frontend/backend validation based on field types and priorities
4. **Workflow Integration**: Connect forms based on patient journey (Registration → Appointment → Consultation → Tests → Admission, etc.)
5. **Reporting**: Use standardized field names for consistent reporting across forms
6. **Audit Trail**: Track form submissions and modifications for compliance

## Healthcare Workflow Coverage

This collection covers the complete hospital management workflow:

```
Registration → Appointment → Emergency/Triage → Consultation
     ↓                              ↓                ↓
  Imaging/Lab Tests ← ────────────────────────────────
     ↓
  Prescription
     ↓
  Admission (if needed)
     ↓
  Nursing Care → Surgery (if needed) → Operative Report
     ↓
  Discharge Summary
     ↓
  Follow-up Appointments
     
Special Forms:
- Birth Certificate (Obstetrics)
- Death Certificate (End of Life)
- Medical Record Transfer (Continuity of Care)
- Consent Forms (Legal Requirements)
```

## License & Usage

These form configurations are provided as templates. Adapt them according to your:
- Local healthcare regulations
- Hospital policies
- Jurisdictional requirements
- Specific departmental needs

---

**Total Forms:** 15  
**Total Fields:** 800+  
**Coverage:** Complete EMR/Hospital Management System
