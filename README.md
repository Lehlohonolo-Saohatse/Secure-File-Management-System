# Secure File Management System (SFMS)

![SFMS Logo](https://via.placeholder.com/800x400?text=SFMS+Logo) <!-- Placeholder; replace with actual logo image -->

A secure, cloud-based file management platform for the South African Police Service (SAPS), emphasizing security, accountability, and compliance with South African data protection laws.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version: 1.0](https://img.shields.io/badge/Version-1.0-blue.svg)](https://example.com)

## Table of Contents

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

## Overview

The Secure File Management System (SFMS) is a cloud-based solution designed to digitize, manage, and secure files and dockets for the South African Police Service (SAPS). Hosted in the AWS Cape Town region, it complies with the Protection of Personal Information Act (POPIA) and the National Policy on Data and Cloud 2024. This system provides a secure, scalable, and user-friendly platform for law enforcement operations, ensuring data sovereignty and integrity.

## Objectives

- Ensure data sovereignty by restricting all data to the AWS Cape Town region.
- Provide secure file upload, storage, and retrieval with encryption.
- Enable digitization and version control of dockets.
- Support multi-language interfaces (English, Afrikaans, Zulu, Xhosa, Sotho).
- Maintain audit trails and compliance with government standards.

## Features

- Secure file upload/download using HTTPS and client-side AES-256 encryption.
- Digitization integration with scanner hardware via WebUSB API.
- File organization and categorization with metadata tagging.
- Git-like version control for dockets in Spring Boot.
- Association of dockets with individuals/cases via database relations.
- Physical docket location tracking, restricted by RBAC to the original station.
- Integrity verification using SHA-256 hashes.
- Secure sharing requests between stations with notifications.
- Encrypted messaging and email archiving.
- Comprehensive audit logging with ELK Stack.

## System Architecture

SFMS uses a client-server architecture optimized for security and compliance in the South African public sector:

- **Frontend**: React.js with Next.js for mobile-responsive, multi-language support via i18n.
- **Backend**: Spring Boot (Java) with OAuth2 and JWT for authentication.
- **Database**: PostgreSQL for ACID-compliant relational data.
- **Cloud Infrastructure**: AWS Cape Town region, using S3 for encrypted storage and RDS for databases.
- **Security Layer**: MFA via Auth0, WebAuthn for biometrics, TLS 1.3, AES-256 encryption, and ELK Stack for logging.

![Architecture Diagram](https://via.placeholder.com/800x400?text=System+Architecture+Diagram) <!-- Replace with actual diagram from project docs -->

## Technologies Used

| Category      | Technologies/Tools                          |
|---------------|---------------------------------------------|
| **Frontend**  | React.js, Next.js, i18n, WebAuthn, WebUSB  |
| **Backend**   | Spring Boot (Java), OAuth2, JWT             |
| **Database**  | PostgreSQL (with JSONB support)             |
| **Cloud**     | AWS (S3, RDS, Cape Town region)             |
| **Security**  | AES-256, SHA-256, Auth0, ELK Stack          |

## User Interface

A single-page application (SPA) built with React.js, supporting multiple languages and WCAG standards for accessibility on desktops and mobiles.

Key Screens:
- **Login**: Username, password, MFA, biometric prompt.
- **Dashboard**: Recent files, notifications, quick search, analytics charts.
- **File Management**: Upload forms, scanner integration, filtered lists.
- **Docket Details**: Version history timeline, merge button, physical location map.
- **Sharing Requests**: Request form, pending approvals, status tracker.
- **Messaging**: Real-time chat, email archive viewer.
- **Audit Reports**: Report generator, log viewer with filters.

## Installation

The project is currently in the design phase. For setting up a prototype:

1. Clone the repository: `git clone https://github.com/Lehlohonolo-Saohatse/Secure-File-Management-System.git`
2. Frontend: `cd frontend && npm install`
3. Backend: `cd ../backend && mvn install`
4. Configure PostgreSQL database and AWS credentials (Cape Town region only).
5. Run: `npm run dev` (frontend) and `mvn spring-boot:run` (backend).

## Usage

- Log in with credentials and MFA/biometrics.
- Use the dashboard for quick access to files and notifications.
- Upload and digitize files via the File Management screen.
- Manage dockets, share requests, and view audits through dedicated screens.

Refer to the [project documentation](File_Management_System.pdf) for detailed workflows.

## License

MIT License - see [LICENSE](LICENSE) for details.

## Author

L Saohatse  
Date: September 23, 2025  
Version: 1.0  
Individual Project  

Contact: [Email](https://message-ls.streamlit.app/)
