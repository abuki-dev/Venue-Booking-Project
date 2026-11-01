# Admin Requirements

Actor: Admin

The Admin is the person who manages the whole system, including users, venues and settings, but does not handle bookings or payments directly.

## 1. Functional Requirements

### 1.1 Account Management

| ID     | Requirement                                                                                       |
|--------|---------------------------------------------------------------------------------------------------|
| ADM-01 | The system shall allow the Admin to log in with email and password.                               |
| ADM-02 | The system shall allow a logged-in Admin to log out.                                              |
| ADM-03 | The system shall allow the Admin to change their own password.                                    |
| ADM-04 | The system shall allow the Admin to create accounts for Managers and Staff.                       |
| ADM-05 | The system shall allow the Admin to edit the details of any user account.                         |
| ADM-06 | The system shall allow the Admin to deactivate and reactivate any user account.                   |
| ADM-07 | The system shall not allow a deactivated user to log in.                                          |
| ADM-08 | The system shall allow the Admin to reset the password of any user.                               |
| ADM-09 | The system shall allow the Admin to view the list of all users and filter it by role and status.  |

### 1.2 Venue Management

| ID     | Requirement                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------|
| ADM-10 | The system shall allow the Admin to add a new venue and assign it to a Manager.                               |
| ADM-11 | The system shall allow the Admin to edit venue details.                                                       |
| ADM-12 | The system shall allow the Admin to deactivate a venue so it no longer appears in Client browsing and search. |
| ADM-13 | The system shall warn the Admin before deactivating a venue that has confirmed upcoming bookings.             |
| ADM-14 | The system shall allow the Admin to manage the list of venue categories used for filtering.                   |

### 1.3 System Settings

| ID     | Requirement                                                                                            |
|--------|--------------------------------------------------------------------------------------------------------|
| ADM-15 | The system shall allow the Admin to enable or disable payment options (Telebirr, CBE and other banks). |

### 1.4 Oversight and Reports

| ID     | Requirement                                                                                                      |
|--------|------------------------------------------------------------------------------------------------------------------|
| ADM-16 | The system shall allow the Admin to view all bookings and filter them by venue, date and status.                 |
| ADM-17 | The system shall allow the Admin to view all payment and refund records in read-only mode.                       |
| ADM-18 | The system shall allow the Admin to view system-wide reports: total bookings, total income and income per venue. |
| ADM-19 | The system shall allow the Admin to view an activity log showing who did what and when.                          |

## 2. Use Cases

| Use Case               | Covers                           |
|------------------------|----------------------------------|
| Log In                 | ADM-01, ADM-02, ADM-03, ADM-07   |
| Manage Users           | ADM-04, ADM-05, ADM-06, ADM-09   |
| Reset Password         | ADM-08                           |
| Manage Venues          | ADM-10, ADM-11, ADM-12, ADM-13   |
| Manage Venue Categories| ADM-14                           |
| Manage Payment Options | ADM-15                           |
| View Reports           | ADM-16, ADM-17, ADM-18           |
| View Activity Log      | ADM-19                           |