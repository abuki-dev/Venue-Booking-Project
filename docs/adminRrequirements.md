# Admin Requirements

## 1. Functional Requirements

### 1.1 Account Management

| ID     | Requirement                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| FR-A1  | The system shall allow the Admin to log in with email and password.                                          |
| FR-A2  | The system shall allow a logged-in Admin to log out.                                                         |
| FR-A3  | The system shall allow the Admin to change their own password.                                               |
| FR-A4  | The system shall allow the Admin to create accounts for Venue Owners, Venue Managers and Staff.              |
| FR-A5  | The system shall allow the Admin to edit the details of any user account.                                    |
| FR-A6  | The system shall allow the Admin to deactivate and reactivate any user account.                              |
| FR-A7  | The system shall not allow a deactivated user to log in.                                                     |
| FR-A8  | The system shall allow the Admin to reset the password of any user.                                          |
| FR-A9  | The system shall allow the Admin to view the list of all users and filter it by role and status.             |

### 1.2 Venue Management

| ID      | Requirement                                                                                                     |
|---------|-----------------------------------------------------------------------------------------------------------------|
| FR-A10  | The system shall allow the Admin to add a new venue and assign it to a Venue Owner or Manager.                 |
| FR-A11  | The system shall allow the Admin to edit venue details.                                                         |
| FR-A12  | The system shall allow the Admin to deactivate a venue so it no longer appears in client browsing and search.   |
| FR-A13  | The system shall warn the Admin before deactivating a venue that has confirmed upcoming bookings.               |
| FR-A14  | The system shall allow the Admin to manage the list of venue categories used for filtering.                     |

### 1.3 System Settings

| ID      | Requirement                                                                                            |
|---------|--------------------------------------------------------------------------------------------------------|
| FR-A15  | The system shall allow the Admin to enable or disable payment options (Telebirr, CBE and other banks). |

### 1.4 Oversight and Reports

| ID      | Requirement                                                                                                      |
|---------|------------------------------------------------------------------------------------------------------------------|
| FR-A16  | The system shall allow the Admin to view all bookings and filter them by venue, date and status.                 |
| FR-A17  | The system shall allow the Admin to view all payment and refund records in read-only mode.                       |
| FR-A18  | The system shall allow the Admin to view system-wide reports: total bookings, total income and income per venue. |
| FR-A19  | The system shall allow the Admin to view an activity log showing who did what and when.                          |

## 2. Non-Functional Requirements

| ID      | Requirement                                                                                                                        |
|---------|------------------------------------------------------------------------------------------------------------------------------------|
| NFR-A1  | The system shall allow only users with the Admin role to open admin pages and functions.                                           |
| NFR-A2  | The system shall lock an Admin account for 15 minutes after 5 failed login attempts.                                              |
| NFR-A3  | The system shall log out an Admin automatically after 15 minutes of inactivity.                                                    |
| NFR-A4  | The system shall load admin pages within 3 seconds under normal use.                                                               |
| NFR-A5  | The system shall record every Admin action in the activity log, and no user, including the Admin, can edit or delete log entries.  |
| NFR-A6  | The system shall ask the Admin to confirm before deactivating an account or a venue.                                               |
| NFR-A7  | The system shall make sure no Admin action causes a double booking or deletes confirmed booking data.                              |
| NFR-A8  | The system shall be usable in current versions of common web browsers on desktop and mobile screens.                               |
| NFR-A9  | The system shall back up all data daily so it can be restored after a failure.                                                     |