# Hospital Management System

Hospital Management System is a Java web application for coordinating common hospital workflows between patients, doctors, and administrators. The application is presented as **Medical Home** and provides a simple portal for discovering doctors, requesting appointments, and managing appointment records.

## What the Project Does

- **Patients** can create an account, sign in, request an appointment with a doctor, view their appointment history, and change their password.
- **Doctors** can sign in, view their dashboard, review assigned patients and appointments, update their profile, and change appointment status.
- **Administrators** can sign in, manage doctors and specialists, view patient records, and monitor doctors, users, and appointment totals from a dashboard.
- **Appointment management** stores patient details, selected doctor, appointment date, disease information, contact details, address, and current status.

## Main Workflow

1. A patient registers or signs in.
2. The patient selects a doctor and submits an appointment request.
3. The doctor views appointments assigned to them and updates their status.
4. Administrators maintain doctor and specialist records and monitor overall activity.
5. Patients can return to view the latest status of their appointments.

## Technology Stack

- Java 17
- Maven
- Java Servlets and JSP
- JSTL
- MySQL with JDBC
- Apache Tomcat
- Bootstrap 5 and Font Awesome for the user interface

## Project Structure

```text
src/main/java/
  com/servlet/   Request handling for admin, doctor, and patient actions
  com/dao/      Database access objects
  com/entity/   Domain models such as User, Doctor, and Appointment
  com/db/       Database connection utility
src/main/webapp/
  *.jsp         Public pages, login screens, and patient flows
  admin/        Administrator dashboard and management pages
  doctor/       Doctor dashboard and patient workflows
  component/    Shared navigation, footer, and styling includes
```

## Running Locally

1. Install Java 17, Maven, MySQL, and Apache Tomcat.
2. Create the application's database and configure the connection values in `src/main/java/com/db/DBConnect.java`.
3. Build the WAR file:

   ```bash
   mvn clean package
   ```

4. Deploy `target/Hospital_Management.war` to Tomcat and open the application in a browser.

The database schema and seed data must be available before using appointment, doctor, or user features.

## Portfolio Note

This project demonstrates a role-based hospital portal, server-side Java web development, MVC-style separation through servlets, DAOs and entities, relational database integration, session-based login flows, and CRUD-oriented management screens.

## Current Scope

This is an educational portfolio project. Before production use, authentication credentials, database configuration, authorization, validation, error handling, and security hardening should be reviewed and moved to environment-based configuration.