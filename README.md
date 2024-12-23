# AllJobs Management System

This project is a **Job Management System** implemented in **C++**. It allows candidates to apply for jobs, employers to post and manage job listings, and provides functionalities for storing and retrieving user and job data from files.

---

## Features

### General
- Data persistence using files:
    - `candidates.txt`
    - `employers.txt`
    - `jobs.txt`
    - `applications.txt`
- Interactive menus for candidates and employers.

### Core Functionalities
- **Candidate Management:**
    - View available jobs and apply.
    - View application history.
    - Edit candidate profile.
    - Save and load candidate data to/from files.
- **Employer Management:**
    - Post, update, or delete jobs.
    - View jobs posted by the employer.
    - Save and load employer data to/from files.
- **Job Listings:**
    - Search jobs based on filters.
    - Save and load job data to/from files.
    - Create job listings interactively.
- **Applications:**
    - Submit applications.
    - Update and view application status.

---

## Project Structure

### Classes Overview

#### 1. **User** (Base Class)
- **Attributes:**
    - `id`: Unique identifier for the user.
    - `password`, `email`, `first_name`, `last_name`.
- **Methods:**
    - `login`: Validates user credentials.
    - Getters and setters for all attributes.

#### 2. **Candidate** (Inherits from `User`)
- **Attributes:**
    - `resume`, `phone_number`, `job_type`, `favorites`.
- **Methods:**
    - `view_jobs_and_apply`, `view_applications`, `edit_profile`.
    - `savetofile` / `loadfromfile`: Save/load candidate data.

#### 3. **Employer** (Inherits from `User`)
- **Methods:**
    - `manage_jobs`: Add, update, or delete jobs.
    - `view_published_jobs`.
    - `savetofile` / `loadfromfile`: Save/load employer data.

#### 4. **Jobs**
- **Attributes:**
    - `location`, `profession`, `job_type`, `jobUID`, `experience`, `employer_id`, `limit`, `app_number`.
- **Methods:**
    - `create_job`, `search_jobs`.
    - `savetofile` / `loadfromfile`.

#### 5. **Application**
- **Attributes:**
    - Candidate and job details (e.g., name, resume, jobUID).
    - `status`: Status of the application (e.g., Pending, Accepted, Rejected).
- **Methods:**
    - `savetofile` / `loadfromfile`.
    - `set_status`: Update the application status.

---

## How to Build and Run

1. **Prerequisites:**
    - C++ compiler (e.g., GCC, Clang, or MSVC).
    - [CMake](https://cmake.org/) for building the project.

2. **Build Instructions:**
   ```bash
   mkdir build
   cd build
   cmake ..
   make
   ```

3. **Run the Application:**
   ```bash
   ./AllJobsManagementSystem
   ```

---

## Contributors
- Elay Levi
- Roi Wishengrad
- Joe Bensimon
---

## License
This project is released under the [MIT License](LICENSE).
