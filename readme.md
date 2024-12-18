# User Management System: Final Project 🚀

## Overview
Welcome to the **User Management System** project, an open-source development initiative guided by Professor Keith Williams at NJIT! This project offers hands-on experience in real-world software development, focusing on user management functionalities with robust testing, QA processes, and new feature implementations.

---

## Goals and Objectives 🎯
1. **Practical Experience**: Collaborate on a production-grade codebase.
2. **Quality Assurance**: Identify and resolve bugs for a robust application.
3. **Test Coverage**: Write 10 new tests to address gaps in existing functionality.
4. **Feature Implementation**: Develop a new feature adhering to best practices.
5. **Industry Readiness**: Mimic real-world development processes and workflows.

---

## Completed Work ✅

### 1. **Feature: Profile Picture Upload with Minio** 🌄  
Enhances user profile management by allowing users to upload and update their profile pictures securely using Minio.

**User Story**:  
_As a user, I want to upload and update my profile picture to personalize my account._

**Implementation**:  
- Created an API endpoint `/upload/{user_id}` to handle file uploads.
- Integrated Minio for object storage to store profile pictures securely.
- Added validation to restrict file types (`.png`, `.jpg`, `.jpeg`) and enforce a maximum file size.
- Resized uploaded images for consistency and optimization.
- Updated user model and response schema to include the profile picture URL.

**Optional Enhancements**:
- Default profile picture for users without an upload.
- Resizing images to a standard format.

**Unit Tests**:  
Implemented unit tests to verify:
- Successful file uploads.
- File type validation.
- File size enforcement.
- Profile picture URL updates in the user model.

---

### **Docker Repository URL** ✅  
https://hub.docker.com/r/varunrahul/user_management

---

### 2. **Quality Assurance (QA): Identified and Fixed 5 Issues** 🐞  
| **Issue**                       | **Status** | **Details**                                                                                     |
|---------------------------------|------------|-------------------------------------------------------------------------------------------------|
| Duplicate email and nickname error during bulk user creation | ✅ Fixed   | Implemented validation checks for duplicate emails and nicknames during user creation.          |
| Role downgrade during email verification for non-anonymous users | ✅ Fixed   | Ensured proper role checks to avoid role downgrades after email verification.                   |
| `list_users` Pagination Validation | ✅ Fixed   | Added input validation for pagination parameters (skip, limit) to prevent invalid behavior.     |
| Missing user-id in email verification | ✅ Fixed   | Resolved issue causing missing user ID during email verification processes.                    |
| Dependency conflicts in Python setup | ✅ Fixed   | Fixed Python dependency conflicts to ensure smooth setup and deployment.                       |

**Closed Issues**:  
- [#14](#) Duplicate email and nickname error during bulk user creation  
- [#10](#) Role downgrade during email verification  
- [#8](#) Pagination validation in list_users  
- [#6](#) Missing user ID in email verification  
- [#3](#) Dependency conflicts in Python setup  

---
https://hub.docker.com/r/varunrahul/user_management

### 3. **Test Coverage Improvement** ✅  
Added **10 new tests** to enhance test coverage:
- Edge case tests for user registration, login, and database updates.
- Tests for the new profile picture upload functionality.
- Validation for invalid file formats and oversized files.

---

## Setup Instructions ⚙️

### Prerequisites  
- Docker & Docker Compose  
- Python 3.12+  
- Minio Server for Object Storage  

### Steps to Run  
1. Clone the repository:  
   ```bash
   git clone git@github.com:killuazoldyck7/user_management.git
   cd user-management
   ```

2. Start all services using Docker Compose:  
   ```bash
   docker-compose up --build -d
   ```

3. Access the application:  
   - **FastAPI**: http://localhost:8000  
   - **Minio**: http://localhost:9000  
   - **PgAdmin**: http://localhost:5050  

4. Run the test suite:  
   ```bash
   docker-compose exec fastapi pytest
   ```

---

## Deployment Status 🚢
The project successfully deploys to DockerHub.  
[DockerHub Repository Link]([https://hub.docker.com/repository/your-link](https://hub.docker.com/r/varunrahul/user_management))

---

## Reflection Document 📄  
- 5 QA issues fixed.  
- 10 additional test cases added.  
- Implemented the **Profile Picture Upload with Minio** feature.  

---

## Commit History 📈  
A consistent commit history has been maintained with clear and descriptive messages:  
- Minimum of **10 commits** achieved.  

---

## Contributors 🤝  
- **killuazoldyck7**  

---

## Conclusion 🎓  
This project demonstrates real-world application development, focusing on high-quality code, robust testing, and collaborative workflows. The new profile picture upload feature enhances user experience, while rigorous testing ensures reliability across the system.  

