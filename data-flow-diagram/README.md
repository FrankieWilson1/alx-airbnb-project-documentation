# Data Flow Diagram (DFD) - Context Level (Level 0)

This document provides an overview of the Data Flow Diagram (DFD) for the ALX-Airbnb system, specifically at the Context Level (Level 0). This diagram visually represents the high-level exchange of data between the entire system and its external interacting entities.

## What is a Data Flow Diagram (DFD)?

A DFD illustrates the flow of information through a system. It shows how data is input, processed, and output, using specific symbols:
-   **External Entity (Rectangle):** A source or destination of data outside the system boundary.
-   **Process (Circle):** A function that transforms incoming data into outgoing data.
-   **Data Flow (Arrow):** The movement of data from one component to another.

## Diagram Overview

The diagram `data-flow.png` presents the **ALX_Airbnb-system** as a single central process, interacting with four main external entities:

-   **Guest:** The user who searches, books, pays, and reviews.
-   **Host:** The user who lists properties and manages bookings.
-   **Admin:** The internal user who manages the overall platform.
-   **Payment Gateway:** An external system responsible for processing financial transactions.

## Summary of Data Flows:

The DFD highlights the key categories of data exchanged:

-   **With Guest:**
    -   **Inputs to System:** User credentials (for login/registration), and various Booking & Service Requests (encompassing search criteria, booking details, review submissions, messages).
    -   **Outputs from System:** Authentication & Profile Data, and Service Responses & Notifications (including search results, booking confirmations, payment confirmations, and general messages).
-   **With Host:**
    -   **Inputs to System:** Property Management Data (for adding/editing listings), Booking Management Actions (for confirming/canceling bookings), and Host Communications (messages).
    -   **Outputs from System:** Property Listing Status, Booking Requests & Updates, Payout Notifications, and Host Responses & Communications.
-   **With Admin:**
    -   **Inputs to System:** Admin Credentials and Admin Management Commands (for system oversight and moderation).
    -   **Outputs from System:** System Status Reports, Management Data Responses, and Admin Confirmations & Notifications.
-   **With Payment Gateway:**
    -   **Inputs to System:** Payment Transaction Status (success/failure) and Refund Confirmation.
    -   **Outputs from System:** Payment Transaction Request and Refund Request.

## Purpose and Importance:

This Level 0 DFD is crucial for:
-   Defining the **scope** and boundaries of the ALX-Airbnb system.
-   Providing a **high-level understanding** of how the system interacts with its external environment.
-   Serving as a foundational document for more detailed DFD levels (Level 1, etc.) if needed.

---
[Back to Main Project README](../README.md)
