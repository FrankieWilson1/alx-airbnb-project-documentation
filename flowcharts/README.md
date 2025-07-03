# Flowchart - User Registration Backend Process

This document provides a detailed flowchart visualizing the backend processes involved in user registration for the ALX-Airbnb system. It outlines the sequential steps, decision points, and data handling from the moment a registration request is received until a user account is successfully created or an error is returned.

## What is a Flowchart?

A flowchart is a diagram that represents a workflow or process. It uses standardized symbols to depict operations, decisions, and the sequence in which they occur. It's an invaluable tool for understanding, designing, and documenting complex procedures.

## Key Flowchart Symbols Used:

-   **Rounded Rectangle (Terminal):** Indicates the **Start** or **End** of the process.
-   **Parallelogram (Input/Output):** Represents data **received** by the system or **sent** out by the system.
-   **Rectangle (Process):** Denotes a specific **action** or step carried out by the backend.
-   **Diamond (Decision):** Represents a point where a **decision** is made, leading to different paths (typically "Yes" or "No").
-   **Arrows:** Show the **direction** of the flow through the diagram.

## Process Overview:

The flowchart for user registration (`data-flow-diagram.png`) covers the following backend logic:

1.  **Initiation & Data Reception**: The process begins, and user registration data (email, password, role) is received from the client-side.
2.  **Input Validation**: The received data undergoes validation for format, strength (for passwords), and completeness of required fields.
3.  **Error Handling (Validation)**: If the input data is found to be invalid, a specific validation error is generated, and a "400 Bad Request" error response is sent back to the user.
4.  **Email Uniqueness Check**: If the data is valid, the database is queried to ensure the provided email address does not already exist.
5.  **Error Handling (Email Conflict)**: If the email is found to be already registered, an "Email Exists" error is generated, and a "409 Conflict" error response is sent to the user.
6.  **Password Hashing**: For valid and unique email addresses, the user's plain-text password is securely hashed.
7.  **User Record Storage**: The new user's record, including the hashed password, is then saved to the `User` table in the database.
8.  **Authentication Token Generation**: An authentication token (e.g., JWT) is generated for the newly registered user, allowing for immediate login.
9.  **Success Response**: A success response ("201 Created") containing the authentication token is sent back to the user, indicating successful registration.
10. **Process Termination**: The backend registration process concludes.

## Purpose and Importance:

This flowchart is essential for:
-   Clearly illustrating the **sequential logic** of the user registration process.
-   Aiding **developers** in implementing and debugging the backend logic.
-   Ensuring **consistency** in how user registration is handled.
-   Serving as documentation for future modifications or extensions of the process.

---
[Back to Main Project README](../README.md)