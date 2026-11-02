# Functional Requirements: EVBMS

This file collects the functional requirements of the Event Venue Booking and Management System (EVBMS) for all actors: Admin, Client, Manager, Staff, and the external Payment Gateway. Every requirement says what the system shall do. IDs run in order inside each actor (ADM, CLI, MGR, STF). The non-functional requirements are in `non_functional_requirements.md`.

## 1. Admin

Actor: Admin

The Admin is the person who manages the whole system, including users, venues and settings, but does not handle bookings or payments directly.

### 1.1 Account Management

| ID | Requirement |
|----|-------------|
| ADM-01 | The system shall allow the Admin to log in with email and password. |
| ADM-02 | The system shall allow a logged-in Admin to log out. |
| ADM-03 | The system shall allow the Admin to change their own password. |
| ADM-04 | The system shall allow the Admin to create accounts for Managers and Staff. |
| ADM-05 | The system shall allow the Admin to edit the details of any user account. |
| ADM-06 | The system shall allow the Admin to deactivate and reactivate any user account. |
| ADM-07 | The system shall not allow a deactivated user to log in. |
| ADM-08 | The system shall allow the Admin to reset the password of any user. |
| ADM-09 | The system shall allow the Admin to view the list of all users and filter it by role and status. |

### 1.2 Venue Management

| ID | Requirement |
|----|-------------|
| ADM-10 | The system shall allow the Admin to add a new venue and assign it to a Manager. |
| ADM-11 | The system shall allow the Admin to edit venue details. |
| ADM-12 | The system shall allow the Admin to deactivate a venue so it no longer appears in Client browsing and search. |
| ADM-13 | The system shall warn the Admin before deactivating a venue that has confirmed upcoming bookings. |
| ADM-14 | The system shall allow the Admin to manage the list of venue categories used for filtering. |

### 1.3 System Settings

| ID | Requirement |
|----|-------------|
| ADM-15 | The system shall allow the Admin to enable or disable payment options (Telebirr, CBE and other banks). |

### 1.4 Oversight and Reports

| ID | Requirement |
|----|-------------|
| ADM-16 | The system shall allow the Admin to view all bookings and filter them by venue, date and status. |
| ADM-17 | The system shall allow the Admin to view all payment and refund records in read-only mode. |
| ADM-18 | The system shall allow the Admin to view system-wide reports: total bookings, total income and income per venue. |
| ADM-19 | The system shall allow the Admin to view an activity log showing who did what and when. |

## 2. Client

Actor: Client

A Client is a person, organization or group that wants to reserve a venue for an event. Anyone can browse venues without an account, but only a registered Client can send a booking request.

### 2.1 Account Management

| ID | Requirement |
|----|-------------|
| CLI-01 | The system shall require a new Client to provide a name, email, phone number and password when registering. |
| CLI-02 | The system shall allow a registered Client to log in with email and password. |
| CLI-03 | The system shall allow a logged-in Client to log out. |
| CLI-04 | The system shall require a visitor to register or log in before sending a booking request. |

### 2.2 Browsing and Search

| ID | Requirement |
|----|-------------|
| CLI-05 | The system shall allow any visitor to browse venues without logging in. |
| CLI-06 | The system shall allow a visitor to filter venues by category, capacity, location and price. |
| CLI-07 | The system shall display each venue's details: category, capacity, price, location, photos, add-ons and special offers where applicable. |
| CLI-08 | The system shall display an availability calendar for each venue that shows available and booked dates. |

### 2.3 Booking

| ID | Requirement |
|----|-------------|
| CLI-09 | The system shall allow a logged-in Client to submit a booking request containing the venue, date(s), start time, end time, event type, number of guests and selected add-ons. |
| CLI-10 | The system shall reject a booking request whose end date is before its start date. |
| CLI-11 | The system shall check venue availability for the requested date and time before accepting a booking request. |
| CLI-12 | The system shall re-check availability when the booking request is submitted. |
| CLI-13 | The system shall accept only the first request when two Clients request the same slot at the same time. |
| CLI-14 | The system shall inform the other Client that the slot is no longer available. |
| CLI-15 | The system shall prevent more than one booking for the same venue, date and time. |
| CLI-16 | The system shall hold the requested slot for 15 minutes while it waits for the payment result. |
| CLI-17 | The system shall send the booking request details to the Manager for review. |

### 2.4 Price Calculation

| ID | Requirement |
|----|-------------|
| CLI-18 | The system shall calculate the total amount to pay as the number of days the Client selects multiplied by the venue's price per day. |
| CLI-19 | The system shall add the price of any selected add-ons to the total amount. |
| CLI-20 | The system shall display the calculated total to the Client before the Client pays. |
| CLI-21 | The system shall recalculate the total automatically if the Client changes the selected days or add-ons. |

### 2.5 Payment

| ID | Requirement |
|----|-------------|
| CLI-22 | The system shall allow the Client to pay for a booking through the Payment Gateway using the available payment options (Telebirr, CBE and other banks). |
| CLI-23 | The system shall ask the Client to enter the transaction ID of the payment. |
| CLI-24 | The system shall verify the payment automatically using the transaction ID entered by the Client. |
| CLI-25 | The system shall notify the Client whether the payment was verified or declined. |
| CLI-26 | The system shall allow the Client to contact the Manager when the payment was made but verification failed. |

### 2.6 Refund

| ID | Requirement |
|----|-------------|
| CLI-27 | The system shall create a refund request automatically when a paid booking is marked "event not held". |
| CLI-28 | The system shall refund the Client the amount paid for the booking, through the same payment method used for the payment. |
| CLI-29 | The system shall record the refund status (requested, approved, completed, rejected) and link it to the booking. |
| CLI-30 | The system shall notify the Client of the refund and each change in its status. |
| CLI-31 | The system shall release the venue slot again for new bookings once the booking is marked "event not held". |

### 2.7 Booking Status and History

| ID | Requirement |
|----|-------------|
| CLI-32 | The system shall allow a Client to view the status of their booking request (pending, payment verified, payment failed, confirmed, cancelled, refunded). |
| CLI-33 | The system shall notify the Client when the status of their booking changes. |
| CLI-34 | The system shall allow a Client to view their booking history. |

### 2.8 Cancellation

| ID | Requirement |
|----|-------------|
| CLI-35 | The system shall allow the Client to cancel a booking request before the payment is confirmed. |
| CLI-36 | The system shall not allow the Client to cancel a booking after the payment is confirmed. |

## 3. Manager

Actor: Manager

The Manager runs the venues assigned to them: reviews booking requests, sets prices, assigns tasks to Staff, follows reports, and handles failed payments, refunds and venue issues.

### 3.1 Account and Access

| ID | Requirement |
|----|-------------|
| MGR-01 | The system shall allow the Manager to log in with email and password. |
| MGR-02 | The system shall allow a logged-in Manager to log out. |
| MGR-03 | The system shall allow the Manager to change their own password. |
| MGR-04 | The system shall allow the Manager to view and update their personal profile information. |
| MGR-05 | The system shall allow the Manager to view the venue or venues assigned to them. |

### 3.2 Booking Management

| ID | Requirement |
|----|-------------|
| MGR-06 | The system shall allow the Manager to view pending booking requests submitted by Clients. |
| MGR-07 | The system shall allow the Manager to view booking details, including Client information, booking date, time, venue and payment status. |
| MGR-08 | The system shall allow the Manager to check venue availability for specific dates and time slots. |
| MGR-09 | The system shall allow the Manager to approve or reject a Client booking request. |
| MGR-10 | The system shall allow the Manager to provide a reason for rejecting a booking request. |
| MGR-11 | The system shall prevent the Manager from approving two bookings for the same venue, date and time. |
| MGR-12 | The system shall allow the Manager to update the status of a booking when necessary. |
| MGR-13 | The system shall notify the Client when a booking request is approved or rejected. |
| MGR-14 | The system shall allow the Manager to filter bookings by date, booking status and payment status. |

### 3.3 Venue Price Management

| ID | Requirement |
|----|-------------|
| MGR-15 | The system shall allow the Manager to define and update the base rental price per day for venues. |
| MGR-16 | The system shall allow the Manager to set different prices based on booking duration, date or time. |
| MGR-17 | The system shall allow the Manager to set special prices for weekends, holidays and special occasions. |
| MGR-18 | The system shall allow the Manager to set prices for add-on services and additional service charges. |
| MGR-19 | The system shall allow the Manager to view the current and previously configured venue prices. |
| MGR-20 | The system shall apply updated prices to new bookings without changing the prices of already confirmed bookings. |

### 3.4 Staff and Task Management

| ID | Requirement |
|----|-------------|
| MGR-21 | The system shall allow the Manager to view the list of Staff assigned to their venue. |
| MGR-22 | The system shall allow the Manager to assign tasks to Staff. |
| MGR-23 | The system shall allow the Manager to provide task descriptions and instructions to Staff. |
| MGR-24 | The system shall allow the Manager to set deadlines and priorities for assigned tasks. |
| MGR-25 | The system shall allow the Manager to view the status of assigned tasks. |
| MGR-26 | The system shall allow the Manager to update or reassign tasks when necessary. |
| MGR-27 | The system shall allow the Manager to review completed and overdue tasks. |

### 3.5 Reports

| ID | Requirement |
|----|-------------|
| MGR-28 | The system shall allow the Manager to view reports for their assigned venue. |
| MGR-29 | The system shall allow the Manager to view the total number of bookings within a selected period. |
| MGR-30 | The system shall allow the Manager to view the total income generated by bookings within a selected period. |
| MGR-31 | The system shall allow the Manager to view income reports by daily, weekly and monthly periods. |
| MGR-32 | The system shall allow the Manager to view booking reports grouped by approved, pending, rejected and cancelled bookings. |
| MGR-33 | The system shall allow the Manager to view payment and refund records related to their venue. |
| MGR-34 | The system shall allow the Manager to view Staff task performance reports. |
| MGR-35 | The system shall allow the Manager to filter reports by date range and booking status. |

### 3.6 Failed Payments and Failed Bookings

| ID | Requirement |
|----|-------------|
| MGR-36 | The system shall allow the Manager to view failed payment transactions related to their venue. |
| MGR-37 | The system shall allow the Manager to review payment failure details, including date, user and failure reason. |
| MGR-38 | The system shall allow the Manager to review the reasons why a booking request failed. |
| MGR-39 | The system shall allow the Manager to contact the Client about a failed booking request or a failed payment. |
| MGR-40 | The system shall allow the Manager to recommend another available time to the Client. |
| MGR-41 | The system shall allow the Manager to track the resolution status of failed booking and payment issues. |

### 3.7 Refunds

| ID | Requirement |
|----|-------------|
| MGR-42 | The system shall allow the Manager to mark a confirmed booking as "event not held" (for example, if the venue cancels or the event cannot take place). |
| MGR-43 | The system shall allow the Manager to review a refund request and approve it after checking the payment record (transaction ID, amount and date). |

### 3.8 Venue Issues Reported by Staff

| ID | Requirement |
|----|-------------|
| MGR-44 | The system shall allow the Manager to view venue issues reported by Staff. |
| MGR-45 | The system shall allow the Manager to respond to a venue issue reported by Staff. |

## 4. Staff

Actor: Staff

Staff do the work on the day of the event: they follow the tasks the Manager assigns, check the event schedule and report venue problems.

### 4.1 Account Management

| ID | Requirement |
|----|-------------|
| STF-01 | The system shall allow registered Staff to log in with email and password. |
| STF-02 | The system shall allow logged-in Staff to log out. |
| STF-03 | The system shall allow Staff to change their account password. |
| STF-04 | The system shall display the basic account information of Staff. |
| STF-05 | The system shall allow Staff to update their phone number and other editable personal information. |

### 4.2 Task Management

| ID | Requirement |
|----|-------------|
| STF-06 | The system shall allow Staff to view the tasks assigned to them. |
| STF-07 | The system shall display the details of each assigned task, including its description and related event. |
| STF-08 | The system shall display the status of each assigned task (pending, in progress, completed). |
| STF-09 | The system shall allow Staff to view the deadline or expected completion time of their assigned tasks. |
| STF-10 | The system shall allow Staff to view their previously completed tasks. |
| STF-11 | The system shall allow Staff to mark an assigned task as completed after finishing the work. |
| STF-12 | The system shall allow Staff to report a task that they cannot complete because of a problem. |

### 4.3 Event Schedule

| ID | Requirement |
|----|-------------|
| STF-13 | The system shall allow Staff to view the event schedule. |
| STF-14 | The system shall display event details, including the event date, start time, end time and venue location. |
| STF-15 | The system shall allow Staff to view the upcoming events they are assigned to work on. |
| STF-16 | The system shall allow Staff to check their assigned tasks based on the event schedule. |
| STF-17 | The system shall display important instructions related to each event. |

### 4.4 Venue Issue Reporting

| ID | Requirement |
|----|-------------|
| STF-18 | The system shall allow Staff to report any issue they find at the venue during event preparation or while the event is taking place. |
| STF-19 | The system shall allow Staff to provide a description of the reported venue issue. |
| STF-20 | The system shall allow Staff to select the type of issue they want to report. |
| STF-21 | The system shall allow Staff to attach photos of the reported venue issue where necessary. |
| STF-22 | The system shall send reported venue issues to the Manager for review and action. |
| STF-23 | The system shall allow Staff to view the status of their reported issues. |
| STF-24 | The system shall notify Staff when the Manager responds to their reported issue. |

### 4.5 Notifications

| ID | Requirement |
|----|-------------|
| STF-25 | The system shall allow Staff to view notifications related to their assigned tasks and events. |
| STF-26 | The system shall notify Staff when a new task is assigned to them or an existing task is updated. |
| STF-27 | The system shall notify Staff when the status of one of their tasks changes. |
| STF-28 | The system shall notify Staff about event updates and schedule changes. |
| STF-29 | The system shall notify Staff when the Manager sends instructions or updates related to their work. |

## 5. Use Case Coverage

Each use case on the Use Case diagram is covered by the requirements below. The Payment Gateway is an outside system, not a person: it checks the transaction ID and sends the result back to the system.

| Use Case | Actor | Requirements |
|----------|-------|--------------|
| Log In | Admin, Client, Manager, Staff | ADM-01 to ADM-03, ADM-07, CLI-02, CLI-03, MGR-01 to MGR-04, STF-01 to STF-05 |
| Register | Client | CLI-01 |
| Search Venue | Client | CLI-05 to CLI-07 |
| Check Availability | Client (included by Book Venue) | CLI-08, CLI-11, CLI-12 |
| Book Venue | Client | CLI-04, CLI-09, CLI-10, CLI-13 to CLI-17 |
| Make Payment | Client | CLI-18 to CLI-23, CLI-26 |
| Verify Payment | Payment Gateway (included by Make Payment) | CLI-24, CLI-25 |
| Cancel Booking | Client | CLI-35, CLI-36 |
| View Booking History | Client | CLI-32 to CLI-34 |
| Manage Users | Admin | ADM-04 to ADM-06, ADM-08, ADM-09 |
| Manage Venues | Admin | ADM-10 to ADM-14 |
| Manage Payment Options | Admin | ADM-15 |
| View Activity Log | Admin | ADM-19 |
| Approve Booking | Manager | MGR-06 to MGR-14 |
| Set Prices | Manager | MGR-15 to MGR-20 |
| Assign Staff Tasks | Manager | MGR-21 to MGR-27, STF-26 |
| Review Failed Payments | Manager | MGR-36 to MGR-41 |
| Process Refund | Manager | CLI-27 to CLI-31, MGR-42, MGR-43 |
| Respond to Venue Issue | Manager | MGR-44, MGR-45, STF-24 |
| View Reports | Admin, Manager | ADM-16 to ADM-18, MGR-28 to MGR-35 |
| View My Tasks | Staff | STF-06 to STF-10, STF-25 to STF-27, STF-29 |
| Mark Task Done | Staff | STF-11, STF-12 |
| View Event Schedule | Staff | STF-13 to STF-17, STF-28 |
| Report Venue Issue | Staff | STF-18 to STF-24 |