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

git clone <your-github-repo-link>
cd <your-repo-folder>


### Step 2: Docker Compose Setup

Create a docker-compose.yml file:

services:
  db:
    image: postgres:13
    environment:
      POSTGRES_DB: odoo
      POSTGRES_USER: odoo
      POSTGRES_PASSWORD: odoo
    volumes:
      - db_data:/var/lib/postgresql/data

  odoo:
    image: odoo:16.0
    depends_on:
      - db
    ports:
      - "8069:8069"
    volumes:
      - ./addons:/mnt/extra-addons
      - ./odoo.conf:/etc/odoo/odoo.conf

volumes:
  db_data:

### Step 3: Start Docker Containers
docker-compose up -d

### Step 4: Access Odoo

Open your browser and go to:

http://localhost:8069


Create a new database or use test_db.

### Step 5: Install Module

Go to Apps → Update Apps List

Search for Student Management

Click Install

##Usage

- **Add Students**: Student Management → Students → Create

- **Add Courses**: Student Management → Courses → Create

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




