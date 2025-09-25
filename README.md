# 🔐 Secure File Management System (SFMS)

<p align="center">
  <img src="https://github.com/Lehlohonolo-Saohatse/Secure-File-Management-System/raw/main/logo.jpg" alt="SFMS Logo" width="200"/>
</p>

<p align="center">
  A secure, cloud-based file management platform for the <b>South African Police Service (SAPS)</b>, emphasizing security, accountability, and compliance with South African data protection laws.
</p>

<p align="center">
  <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"/>
  </a>
  <img src="https://img.shields.io/badge/Version-1.0-blue.svg" alt="Version 1.0"/>
  <img src="https://img.shields.io/badge/Status-Design%20Phase-orange" alt="Status"/>
  <a href="sfms/File_Management_System.pdf">
    <img src="https://img.shields.io/badge/Docs-PDF-blueviolet?logo=adobeacrobatreader&logoColor=white" alt="Documentation"/>
  </a>
</p>


---

## 📑 Table of Contents
- [Overview](#overview)
- [Objectives](#objectives)
- [Features](#features)
- [System Architecture](#system-architecture)
- [Technologies Used](#technologies-used)
- [User Interface](#user-interface)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

---

## 📝 Overview
The **Secure File Management System (SFMS)** is a **cloud-based solution** designed to digitize, manage, and secure files and dockets for the **South African Police Service (SAPS)**.  

- **Hosted in**: AWS Cape Town region 🇿🇦  
- **Compliance**: POPIA & National Policy on Data and Cloud 2024  
- **Core Values**: Security • Accountability • Integrity • Data Sovereignty  

---

## 🎯 Objectives
- ✅ Ensure **data sovereignty** by restricting all data to the AWS Cape Town region.  
- ✅ Provide **secure file upload, storage, and retrieval** with encryption.  
- ✅ Enable **digitization** and version control of dockets.  
- ✅ Support **multi-language interfaces** (English, Afrikaans, Zulu, Xhosa, Sotho).  
- ✅ Maintain **audit trails** and compliance with government standards.  

---

## 🚀 Features
- 🔒 **Secure file upload/download** with HTTPS + AES-256 encryption.  
- 📠 **Digitization integration** with scanner hardware (WebUSB API).  
- 🗂️ **File organization & metadata tagging**.  
- 🔄 **Git-like version control** for dockets in Spring Boot.  
- 👥 **Case linking**: associate dockets with individuals/cases.  
- 📍 **Physical docket tracking** with RBAC (restricted access).  
- 🧾 **Integrity verification** with SHA-256 hashes.  
- 🔗 **Secure sharing requests** with inter-station notifications.  
- 💬 **Encrypted messaging & email archiving**.  
- 📊 **Comprehensive audit logging** with ELK Stack.  

---

## 🏗️ System Architecture
SFMS is built on a **client-server architecture** optimized for security and compliance:  

- **Frontend**: React.js + Next.js, multilingual (i18n) support.  
- **Backend**: Spring Boot (Java) with OAuth2 + JWT authentication.  
- **Database**: PostgreSQL (ACID-compliant with JSONB support).  
- **Cloud**: AWS (Cape Town region) → S3 (storage), RDS (databases).  
- **Security**: MFA (Auth0), WebAuthn (biometrics), TLS 1.3, AES-256, ELK Stack.  

<p align="center">
  <img src="https://via.placeholder.com/800x400?text=System+Architecture+Diagram" alt="System Architecture Diagram"/>
</p>

---

## 🛠️ Technologies Used

| Category      | Technologies/Tools                          |
|---------------|---------------------------------------------|
| **Frontend**  | React.js, Next.js, i18n, WebAuthn, WebUSB   |
| **Backend**   | Spring Boot (Java), OAuth2, JWT             |
| **Database**  | PostgreSQL (JSONB support)                  |
| **Cloud**     | AWS (S3, RDS – Cape Town region)            |
| **Security**  | AES-256, SHA-256, Auth0, ELK Stack          |

---

## 🎨 User Interface
The SFMS is a **single-page application (SPA)** built with React.js:  

- **Login** → Username, password, MFA, biometrics  
- **Dashboard** → Quick access to files, notifications, analytics  
- **File Management** → Uploads, scanner integration, filters  
- **Docket Details** → Version history, merge control, location tracking  
- **Sharing Requests** → Approvals, status tracker  
- **Messaging** → Real-time chat, email archive  
- **Audit Reports** → Log viewer, filters, report generator  

---

## ⚙️ Installation
> The project is currently in the **design phase**. Prototype setup:  

```bash
# Clone the repository
git clone https://github.com/Lehlohonolo-Saohatse/Secure-File-Management-System.git

# Frontend setup
cd frontend
npm install
npm run dev

# Backend setup
cd ../backend
mvn install
mvn spring-boot:run
