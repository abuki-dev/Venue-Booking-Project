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


 <h2>2.Staff</h2>

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
