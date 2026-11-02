# Non-Functional Requirements

## 1.Client

| ID     | Requirement                                                                                                                     |
| ------ | ------------------------------------------------------------------------------------------------------------------------------- |
| NFR-C1 | The system shall store passwords in hashed form, never as plain text.                                                           |
| NFR-C2 | The system shall not store bank account credentials, and shall keep transaction IDs protected over a secure (HTTPS) connection. |
| NFR-C3 | The system shall return the result of an availability check within 3 seconds.                                                   |
| NFR-C4 | The system shall send payment and status notifications to the Client within 1 minute of the event.                              |
| NFR-C5 | The system shall process simultaneous booking requests for the same slot so that no double booking can occur.                   |
| NFR-C6 | The system shall be usable in current versions of common web browsers on desktop and mobile screens.                            |
| NFR-C7 | The system shall reject a transaction ID that has already been used for another booking.                                        |


 ## 2.Staff

 <h3>2.1 Performance</h3>
 
|ID	        |Requirement
|-----------|--------------------------------------------------------------------------------------------------------------|
|STF-NFR-01	|The system shall display the Staff dashboard within 3 seconds and less than under normal network              conditions.                                                                                                                |
|STF-NFR-02	|The system shall load assigned tasks and event schedules without unnecessary delays.                          |
|STF-NFR-03	|The system shall save task completion updates and issue reports without unnecessary delays.                   |
|STF-NFR-04	|The system shall send important task and event notifications as soon as possible.                             |

<h3>2.2 Security</h3>

ID	        |Requirement
|-----------|--------------------------------------------------------------------------------------------------------------|
|STF-NFR-01	|The system shall protect Staff account passwords using secure password hashing.                               |
|STF-NFR-02	|The system shall require Staff members to log in before accessing their assigned tasks and event information. |
|STF-NFR-03	|The system shall protect Staff information from unauthorized access.                                          |
|STF-NFR-04	|The system shall ensure that Staff members can only access information related to their assigned              
responsibilities.                                                                                                          |
|STF-NFR-05	|The system shall automatically end inactive Staff sessions after a specified period.                          |

<h3>2.3 Usability</h3>

|ID	        |Requirement
|-----------|--------------------------------------------------------------------------------------------------------------|
|STF-NFR-01	|The system shall provide a simple and easy-to-understand interface for Staff members.                         |
|STF-NFR-02	|The system shall make it easy for Staff members to find their assigned tasks and event schedules.             |
|STF-NFR-03	|The system shall display task statuses and notifications in a clear and understandable way.                   |
|STF-NFR-04	|The system shall provide clear messages when Staff members successfully.                                      |


# 3. Admin Non-Functional Requirements

Actor: Admin

The Admin is the person who manages the whole system, including users, venues and settings, but does not handle bookings or payments directly.

| ID          | Requirement                                                                                                                       |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ADM-NFR-01  | The system shall allow only users with the Admin role to open admin pages and functions.                                          |
| ADM-NFR-02  | The system shall lock an Admin account for 15 minutes after 5 failed login attempts.                                              |
| ADM-NFR-03  | The system shall log out an Admin automatically after 15 minutes of inactivity.                                                   |
| ADM-NFR-04  | The system shall load admin pages within 3 seconds under normal use.                                                              |
| ADM-NFR-05  | The system shall record every Admin action in the activity log, and no user, including the Admin, can edit or delete log entries. |
| ADM-NFR-06  | The system shall ask the Admin to confirm before deactivating an account or a venue.                                              |
| ADM-NFR-07  | The system shall make sure no Admin action causes a double booking or deletes confirmed booking data.                             |
| ADM-NFR-08  | The system shall be usable in current versions of common web browsers on desktop and mobile screens.                              |
| ADM-NFR-09  | The system shall back up all data daily so it can be restored after a failure.                                                    |

### 4. Manager

| ID | Requirement |
| :--- | :--- |
| NFR-M1 | The system shall allow only authenticated users with the Venue Manager role to access manager pages and functions. |
| NFR-M2 | The system shall restrict Venue Managers from accessing or modifying venues that are not assigned to them. |
| NFR-M3 | The system shall lock a Venue Manager account for 15 minutes after five consecutive failed login attempts. |
| NFR-M4 | The system shall automatically log out a venue manager after 15 minutes of inactivity. |
| NFR-M5 | The system shall load Manager pages within 3 seconds under normal operating conditions. |
| NFR-M6 | The system shall record important Manager activities, including booking approvals, booking rejections, price changes and staff task assignments, in the activity log. |
| NFR-M7 | The system shall ensure that booking approval does not result in double bookings or conflicts in venue availability. |
| NFR-M8 | The system shall ensure that confirmed booking records remain when venue prices are updated. |
| NFR-M9 | The system shall ensure that booking, payment and income reports display accurate and consistent information. |
| NFR-M10 | The system shall protect customer, payment and staff information from unauthorised access. |
| NFR-M11 | The system shall be compatible with current versions of commonly used web browsers on desktop and mobile devices. |
| NFR-M12 | The system shall automatically notify relevant staff members when tasks are assigned or updated. |
