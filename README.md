
# Doctor Appointment Booking App

## Frameworks and Language Used

- Database: PostgreSQL
- Language: Java

## Data Flow

### Controller
The controller layer of our application is responsible for handling incoming HTTP requests, processing them, and sending appropriate responses. It utilizes the following functions:

- `createAppointment`: Handles the creation of new appointment bookings.
- `getAppointment`: Retrieves information about a specific appointment.
- `updateAppointment`: Allows for updating appointment details.
- `deleteAppointment`: Deletes an appointment from the system.
- `getAllAppointments`: Fetches a list of all appointments.

### Services
The services layer acts as an intermediary between the controller and the repository. It encapsulates the business logic and performs data validation. It includes the following functions:

- `validateAppointmentData`: Validates the appointment data before saving it.
- `checkDoctorAvailability`: Ensures that the selected doctor is available at the requested time.
- `sendAppointmentConfirmation`: Sends a confirmation message to the patient after a successful appointment booking.

### Repository
The repository layer handles database operations and interactions with our PostgreSQL database. It provides the following functions:

- `createAppointment`: Saves appointment data to the database.
- `findAppointmentById`: Retrieves an appointment by its unique ID.
- `updateAppointmentData`: Updates appointment details in the database.
- `deleteAppointmentById`: Deletes an appointment from the database.
- `findAllAppointments`: Retrieves all appointments from the database.

## Database Design

We use a PostgreSQL database to store data for our doctor appointment booking application. It includes the following tables:

1. `doctors`: Contains information about doctors, including their name, specialization, and availability schedule.
2. `patients`: Stores patient information, such as name, contact details, and medical history.
3. `appointments`: Records appointment details, such as the chosen doctor, appointment time, and patient information.

## Data Structures Used


- Relational Database: We employ a relational database system to efficiently manage and query data in a structured manner.

## Project Summary

This doctor appointment booking application relies on a PostgreSQL database to store doctor, patient, and appointment information. The system provides a set of APIs for creating, managing, and querying doctor appointments, ensuring that patients can easily book appointments with available doctors. The application prioritizes data integrity and incorporates features like appointment confirmation for an improved patient experience.
