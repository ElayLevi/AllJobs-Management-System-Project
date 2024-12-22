This project is a Job Management System implemented in C++. The system allows candidates to apply for jobs, employers to post and manage job listings, and provides functionalities for storing and retrieving user and job data from files.

Project Structure

Classes Overview

1. User

Base class for common attributes and methods shared by Candidate and Employer.

Attributes:

id: Unique identifier for the user.

password: User's password.

email: User's email address.

first_name: User's first name.

last_name: User's last name.

Methods:

login: Validates user credentials.

Getters and setters for all attributes.

2. Candidate (Inherits from User)

Represents a job candidate.

Attributes:

resume: Candidate's resume content.

phone_number: Candidate's contact number.

job_type: Type of job the candidate is seeking (e.g., full-time, part-time).

favorites: List of favorite job IDs.

Methods:

login: Validates credentials for a candidate.

savetofile/loadfromfile: Save/load candidate data to/from a file.

view_jobs_and_apply: View available jobs and apply.

view_applications: View application history.

edit_profile: Modify candidate profile information.

3. Employer (Inherits from User)

Represents an employer posting and managing jobs.

Methods:

login: Validates credentials for an employer.

savetofile/loadfromfile: Save/load employer data to/from a file.

manage_jobs: Add, update, or delete jobs.

view_published_jobs: Display jobs posted by the employer.

4. Jobs

Represents a job listing.

Attributes:

location: Location of the job.

profession: Job title or profession.

job_type: Type of job (e.g., full-time, part-time).

jobUID: Unique identifier for the job.

experience: Required years of experience.

employer_id: ID of the employer posting the job.

limit: Limit on the number of applications.

app_number: Current number of applications.

Methods:

savetofile/loadfromfile: Save/load job data to/from a file.

create_job: Interactive method to create a job.

search_jobs: Search for jobs based on filters.

5. Application

Represents a job application.

Attributes:

Candidate and job details (e.g., name, resume, jobUID).

status: Status of the application (e.g., Pending, Accepted, Rejected).

Methods:

savetofile/loadfromfile: Save/load application data to/from a file.

set_status: Update the application status.

General Features

Data persistence using files:

Candidates: candidates.txt

Employers: employers.txt

Jobs: jobs.txt

Applications: applications.txt

Interactive menus for candidates and employers.

Author's:
Elay Levi
Roi Wishengrad
Joe Bensimon
Or Farkash
Shira Boros
Nikita Kimelblat
