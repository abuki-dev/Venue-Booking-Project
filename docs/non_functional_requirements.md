# Non-Functional Requirements

## Client

| ID     | Requirement                                                                                                                     |
| ------ | ------------------------------------------------------------------------------------------------------------------------------- |
| NFR-C1 | The system shall store passwords in hashed form, never as plain text.                                                           |
| NFR-C2 | The system shall not store bank account credentials, and shall keep transaction IDs protected over a secure (HTTPS) connection. |
| NFR-C3 | The system shall return the result of an availability check within 3 seconds.                                                   |
| NFR-C4 | The system shall send payment and status notifications to the Client within 1 minute of the event.                              |
| NFR-C5 | The system shall process simultaneous booking requests for the same slot so that no double booking can occur.                   |
| NFR-C6 | The system shall be usable in current versions of common web browsers on desktop and mobile screens.                            |
| NFR-C7 | The system shall reject a transaction ID that has already been used for another booking.                                        |
