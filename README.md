# Student Management Module for Odoo 16

## Overview
This is a custom Odoo 16 module called **Student Management** developed as part of a fresher assignment at NN Services & Engineering Ltd.  
It allows you to manage students, courses, and enroll students in multiple courses.

---

## Features
- **Student Model**: Fields – `name`, `email`, `roll_no`, `department`
- **Course Model**: Fields – `name`, `code`, `credit`
- **Many-to-Many Relation**: Students can enroll in multiple courses
- **Views**:
  - Form view for adding students and courses
  - Tree (list) view for displaying students
- **Reports**: View students enrolled in a specific course
- **Bonus Features (Optional)**:
  - Button on student form → "Show Enrolled Courses"
  - Menu in Odoo: `Student Management → Students / Courses`

---

## Prerequisites
Before running this module, make sure you have:
- Docker & Docker Desktop (Mac)
- Docker Compose
- VS Code (or any code editor)
- Git & GitHub account
- Basic understanding of Python and PostgreSQL

---

## Tools & Technology
- **Programming Language:** Python
- **Database:** PostgreSQL 13
- **ERP Framework:** Odoo 16
- **Views & UI:** XML (Odoo)
- **Containerization:** Docker, Docker Compose
- **Version Control:** Git, GitHub

---

## Folder Structure
<img width="490" height="560" alt="image" src="https://github.com/user-attachments/assets/f924c96a-4c2a-4886-aa62-70a844442b46" />





## Setup Instructions

### Step 1: Clone Repository

-**Open Terminal / Command Prompt and run**: cd ~/Documents (or any preferred directory)

-**Clone the repository**: git clone https://github.com/MdFoysalMahmud372/odoo-student-management.git

-**Go inside the project folder**: cd odoo-student-management

### Step 2: Start Docker Containers
docker-compose up -d

### Step 3: Access Odoo

-**Open your browser and go to**: http://localhost:8069

--**Create a new database or use test_db.**

### Step 5: Install Module

-**Go to Apps → Update Apps List**

-**Search for type**: student_management

-**Click Install**

##Usage

- **Students**: Student Management → Students → Create

- **Courses**: Student Management → Courses → Create

- **Enroll Students**: Open student form → select multiple courses

- **Generate Reports**: Filter students by course

- **Bonus Button**: "Show Enrolled Courses" in student form

- **Menu Navigation**: Student Management → Students / Courses

## Challenges Faced & Solutions

- **Docker setup issues: Fixed by proper ports and volumes configuration in docker-compose.yml

- **Odoo 16 compatibility**: Used correct Docker image odoo:16.0

- **Database connection errors**: Configured PostgreSQL environment variables correctly

- **Master password errors**: Reset master password in odoo.conf



GitHub Repository: <your-github-repo-link>


##Notes

- **Ensure Docker Desktop is running before starting Odoo**

- **Update odoo.conf with correct database credentials if needed**

- **Clean, understandable Python and XML code is used for all module features**

##License

This project is open for educational purposes and demo assignment submissions.




