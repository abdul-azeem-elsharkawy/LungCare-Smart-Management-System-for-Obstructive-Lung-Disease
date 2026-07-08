# LungCare Mobile Application

## Smart Management System for Obstructive Lung Disease

LungCare is a mobile healthcare application designed to support patients with obstructive lung diseases by connecting a smart respiratory device, patients, and doctors in one integrated digital system.

The application provides smart inhaler control, guided spirometry testing, medical report generation, treatment plan updates, device management, and patient-doctor follow-up.

> This repository is a public showcase version of the project.  
> The source code is kept private for security reasons because the system integrates with Firebase services, Bluetooth Low Energy communication, and medical-device-related workflows.

---

## Project Overview

Patients with obstructive lung diseases often need continuous medication tracking, periodic pulmonary function monitoring, and regular follow-up with healthcare providers.

LungCare was developed to make this process more connected and organized by combining:

- A Flutter mobile application
- ESP32 Bluetooth Low Energy communication
- Smart inhaler dose tracking
- Digital spirometry test guidance
- Firebase cloud-based medical data storage
- Doctor dashboard for patient follow-up

The system aims to improve treatment adherence, support remote monitoring, and provide a clearer view of the patient’s respiratory condition over time.

---

## LungCare Smart Device

LungCare is not only a mobile application. It is designed as a complete connected respiratory-care system that combines a smart physical device with a mobile application and cloud-based medical follow-up.

The LungCare device integrates two main modules:

- Smart Inhaler Module
- Smart Spirometer Module

Together, these modules support medication delivery, lung-function testing, digital tracking, and doctor review through one connected platform.

![LungCare Smart Device](assets/screenshots/device/01-lungcare-device.png)

---

## Device Concept

The LungCare smart device was designed to transform respiratory care from manual and disconnected workflows into a smart, guided, and connected experience.

The device supports:

- Automated medication actuation
- Guided spirometry testing
- Digital medication tracking
- Lung-function result visualization
- Patient data sharing with doctors

This allows the patient to use one integrated system for treatment, testing, and medical follow-up.

---

## Product Architecture

The system architecture connects embedded hardware, Bluetooth Low Energy communication, the Flutter mobile application, Firebase services, and clinical follow-up tools.

The hardware layer includes the smart inhaler and smart spirometer device. The mobile app acts as the user interface, while Firebase stores patient data, medication logs, spirometry reports, and treatment updates.

![Product Architecture](assets/screenshots/device/02-product-architecture.png)

The main architecture layers include:

- Embedded hardware
- Bluetooth Low Energy communication
- Flutter mobile application
- Firebase cloud services
- Clinical management layer

---

## Product Design Concept

The LungCare device housing was custom-engineered to integrate the mechanical and electronic components required for portable respiratory care.

The design supports:

- pMDI canister placement
- Mouthpiece interface
- Spirometry airflow path
- Internal electronics placement
- Battery placement
- Servo motor alignment
- Overall mechanical integration

![Product Design Concept](assets/screenshots/device/03-product-design-concept.png)

---

## 3D-Printed Housing

The physical prototype was built using a custom 3D-printed housing.

The housing was designed to support:

- Portable device form
- Stable inhaler positioning
- Integrated airflow path
- Internal electronics housing
- Mechanical actuation alignment

![3D-Printed Housing](assets/screenshots/device/04-3d-printed-housing.png)

---

## Smart Spirometer Module

The LungCare Smart Spirometer brings lung-function assessment closer to the patient’s home.

The spirometer module supports:

- Home-based assessment
- Guided test workflow
- Flow and volume calculation
- Spirometry report generation
- Doctor review through the mobile application

![Smart Spirometer Module](assets/screenshots/device/05-spirometer-module.png)

The spirometer relies on pressure-based airflow sensing to estimate airflow and calculate respiratory values such as FVC, FEV1, FEV1/FVC ratio, PEF, and FET.

---

## Smart Inhaler Module

The Smart Inhaler module replaces manual inhaler pressing with a controlled and sensor-validated medication delivery mechanism.

The module supports:

- Safety validation before actuation
- Correct orientation checking
- Inhalation-based triggering
- Servo-based canister pressing
- Confirmed dose logging to the mobile application

![Smart Inhaler Module](assets/screenshots/device/06-smart-inhaler-module.png)

The goal of this module is to improve dose delivery reliability, reduce incorrect inhaler technique, and provide a clear digital medication history for both patients and doctors.

---

## Main Application Users

### Patient

The patient can:

- Pair and manage a LungCare device
- Take medication using the smart inhaler workflow
- Perform guided spirometry tests
- View spirometry reports
- Receive treatment plan updates
- Receive low-dose and low-battery notifications
- Monitor device status through the My Device page

### Doctor

The doctor can:

- View linked patients
- Review patient profiles
- Monitor medication logs
- Review spirometry reports
- Update treatment plans
- Send medical instructions to patients

---

## Key Features

### Smart Inhaler Workflow

The smart inhaler module allows the patient to start the dose process from the mobile application.

The app communicates with the ESP32 device through Bluetooth Low Energy. The dose is only logged after the app receives a confirmed dose signal from the device.

This helps avoid false dose logging and improves medication tracking accuracy.

---

### Guided Spirometry Test

The application provides a guided spirometry workflow to help the patient perform the test correctly.

The spirometry instructions screen includes:

- Written test steps
- Patient-friendly breathing guidance
- An instructional video guide inside the app
- Start test button leading to the interactive spirometry test screen

The test includes normal breathing followed by forced exhalation trials.

---

### Spirometry Reports

The application stores and displays important pulmonary function parameters, including:

- FVC
- FEV1
- FEV1/FVC Ratio
- PEF
- FET
- Test quality notes
- Flow-volume curve
- Flow-time curve

These reports help doctors evaluate the patient’s respiratory condition and follow disease progression.

---

### My Device Page

The My Device page allows the patient to monitor and manage the paired LungCare device.

It displays:

- Device name
- Device ID
- Connection status
- Last seen time
- Battery percentage
- Unpair device option

The page also supports secure device ownership, ensuring that one physical device can only be paired with one patient at a time.

---

### Notifications and Alerts

The application supports several patient notifications:

- Treatment plan update notification
- Inhaler low-dose notification
- Low battery notification
- Device-related reminders

These alerts help patients stay consistent with treatment and device usage.

---

### Doctor Dashboard

The doctor dashboard allows healthcare providers to follow patients remotely.

Doctors can review medication usage, spirometry reports, and update the patient treatment plan.

When the doctor updates the plan, the patient receives a notification inside the application.

---

## Application Workflow

### Patient Workflow

1. Patient logs into the application.
2. Patient pairs the LungCare device.
3. Patient views device status from the My Device page.
4. Patient takes medication using the Smart Inhaler card.
5. Patient performs a guided spirometry test.
6. Spirometry results are saved and displayed as reports.
7. Patient receives notifications for treatment updates, low dose count, and low battery.

---

### Doctor Workflow

1. Doctor logs into the application.
2. Doctor views linked patients.
3. Doctor opens a patient profile.
4. Doctor reviews medication logs.
5. Doctor reviews spirometry reports.
6. Doctor updates the treatment plan.
7. Patient receives the updated medical instructions.

---

## Technology Stack

- Flutter
- Dart
- Firebase Authentication
- Cloud Firestore
- Firebase Realtime Database
- Firebase Local Notifications
- Bluetooth Low Energy
- ESP32
- Mobile-based spirometry visualization

---

## Screenshots

### Login Screen

![Login Screen](assets/screenshots/01-login.png)

---

### Patient Dashboard

![Patient Dashboard](assets/screenshots/02-patient-dashboard.png)

---

### My Device Page

![My Device Page](assets/screenshots/03-my-device.png)

---

### Smart Inhaler Card

![Smart Inhaler](assets/screenshots/04-smart-inhaler.png)

---

### Spirometry Instructions with Video Guide

![Spirometry Instructions](assets/screenshots/05-spirometry-instructions.png)

---

### Gamified Spirometry Test

![Spirometry Test](assets/screenshots/06-spirometry-test.png)

---

### Spirometry Report

![Spirometry Report](assets/screenshots/07-spirometry-report.png)

---

### Doctor Dashboard

![Doctor Dashboard](assets/screenshots/08-doctor-dashboard.png)

---

### Doctor Patient View

![Doctor Patient View](assets/screenshots/09-patient-details-doctor-view.png)

---

### Treatment Plan Update

![Treatment Plan](assets/screenshots/10-treatment-plan.png)

---

## Security Note

This public repository does not include the application source code, Firebase configuration files, ESP32 firmware, API keys, or any private database structure.

The complete implementation is kept private because the project integrates with:

- Firebase services
- Bluetooth Low Energy device communication
- Patient-related medical data
- Smart device control logic

This public version is intended only to present the project idea, features, workflow, and user interface.

---

## Academic Information

**Project Name:** Smart Management System for Obstructive Lung Disease  
**Application Name:** LungCare  
**University:** Capital University  
**Faculty:** Faculty of Engineering  
**Department:** Biomedical Engineering Department  
**Graduation Year:** 2026  

---

## Team Members

- AbdulAzeem Lotfy AbdulAzeem
- Amr Mohamed Sayed
- Ehab Mokhtar Mohamed
- Mahmoud Ahmed Zaalouk
- Mohamed Farhat Hassan
- Youssef Gamal Hussien

---

## Supervisors

- Dr. Mohamed Ali
- Dr. Yomna Hassan

---

## Project Status

The project is currently developed as a graduation project prototype combining mobile application development, embedded systems, Bluetooth communication, Firebase cloud services, and respiratory healthcare monitoring.

---

## Disclaimer

LungCare is developed for academic and research purposes as a graduation project prototype. It is not intended to replace professional medical diagnosis, clinical spirometry devices, or direct medical supervision.
