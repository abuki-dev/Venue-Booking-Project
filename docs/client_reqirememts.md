# Client Requirements

## 1. Functional Requirements

### 1.1 Account Management

| ID    | Requirement                                                                                                 |
| ----- | ----------------------------------------------------------------------------------------------------------- |
| FR-C1 | The system shall require a new Client to provide a name, email, phone number and password when registering. |
| FR-C2 | The system shall allow a registered Client to log in with email and password.                               |
| FR-C3 | The system shall allow a logged-in Client to log out.                                                       |
| FR-C4 | The system shall require a visitor to register or log in before sending a booking request.                  |

### 1.2 Browsing and Search

| ID    | Requirement                                                                                                                                             |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FR-C5 | The system shall allow any visitor to browse venues without logging in.                                                                                 |
| FR-C6 | The system shall allow a visitor to filter venues by category, capacity, location and price.                                                            |
| FR-C7 | The system shall display each venue's details: category, capacity, price, location, photos, add-ons, and special offers where applicable. **(updated)** |
| FR-C8 | The system shall display an availability calendar for each venue that shows available and booked dates.                                                 |

### 1.3 Booking

| ID     | Requirement                                                                                                                                                                                                                                                    |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FR-C9  | The system shall allow a logged-in Client to submit a booking request containing the venue, date(s), start time, end time, event type, number of guests and selected add-ons.                                                                                  |
| FR-C10 | The system shall check venue availability for the requested date and time before accepting a booking request.                                                                                                                                                  |
| FR-C11 | The system shall re-check availability when the request is submitted and, if two Clients request the same slot at the same time, accept only the first and inform the other that the slot is no longer available and waits 15 min for payment gatwayes result. |
| FR-C12 | The system shall prevent more than one booking for the same venue, date and time.                                                                                                                                                                              |
| FR-C13 | The system shall send booking request details to the Venue Manager for review. _(TBD: does the Manager approve after payment?)_                                                                                                                                |

### 1.4 Payment

| ID      | Requirement                                                                                                                                          |
| ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| FR-C14  | The system shall allow the Client intantly pay for a booking using the available payment options (Telebirr, CBE and other banks) .                   |
| FR-C15  | The system shall ask the Client to enter the transaction ID of the payment.                                                                          |
| FR-C16  | The system shall verify the payment by itself using the transaction ID entered by the Client.                                                        |
| FR-C17  | The system shall notify the Client whether the payment was verified or declined.                                                                     |
| FR-C18  | The system shall allow the Client to contact the Venue Manager when the payment was made but verification failed. **(updated)**                      |
| FR-C19  | The system shall allow the Venue Manager to handle failed payment verifications.                                                                     |
| FR-C20  | The system shall calculate the total amount to pay as the number of days the Client selects for the booking multiplied by the venue's price per day. |
| FR-C20a | The system shall add the price of any selected add-ons to the total amount.                                                                          |
| FR-C20b | The system shall display the calculated total to the Client before the Client pays.                                                                  |
| FR-C20c | The system shall recalculate the total automatically if the Client changes the selected days or add-ons.                                             |
| FR-C20d | The system shall reject a booking request whose end date is before its start date.                                                                   |     |

### 1.5 Refund

| ID     | Requirement                                                                                                                                                     |
| ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FR-C21 | The system shall allow the Venue Manager to mark a confirmed booking as "event not held" (for example, if the venue cancels or the event could not take place). |
| FR-C22 | The system shall create a refund request automatically when a paid booking is marked "event not held".                                                          |
| FR-C23 | The system shall allow the Venue Manager to review the refund request and approve it, after checking the payment record (transaction ID, amount and date).      |
| FR-C24 | The system shall refund the Client the amount paid for the booking, through the same payment method used for the payment.                                       |
| FR-C25 | The system shall record the refund status (requested, approved, completed, rejected) and link it to the booking.                                                |
| FR-C26 | The system shall notify the Client of the refund and each change in its status.                                                                                 |
| FR-C27 | The system shall release the venue slot again for new bookings once the booking is marked "event not held".                                                     |

### 1.6 Status and Notifications

| ID     | Requirement                                                                                                                                              |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FR-C23 | The system shall allow a Client to view the status of their booking request (pending, payment verified, payment failed, confirmed, cancelled, refunded). |
| FR-C24 | The system shall notify the Client when the status of their booking changes.                                                                             |
| FR-C25 | The system shall allow a Client to view their booking history. _(optional)_                                                                              |

### 1.7 Cancellation

| ID     | Requirement                                                                                    |
| ------ | ---------------------------------------------------------------------------------------------- |
| FR-C26 | The system shall allow the Client to cancel a booking request before the payment is confirmed. |
| FR-C27 | The system shall not allow the Client to cancel a booking after the payment is confirmed.      |

### 1.8 Access Control

| ID     | Requirement                                                                                                             |
| ------ | ----------------------------------------------------------------------------------------------------------------------- |
| FR-C28 | The system shall not allow a Client to view other users' booking data or access administrator and management functions. |

## 2. Non-Functional Requirements

| ID     | Requirement                                                                                                                     |
| ------ | ------------------------------------------------------------------------------------------------------------------------------- |
| NFR-C1 | The system shall store passwords in hashed form, never as plain text.                                                           |
| NFR-C2 | The system shall not store bank account credentials, and shall keep transaction IDs protected over a secure (HTTPS) connection. |
| NFR-C3 | The system shall return the result of an availability check within 3 seconds.                                                   |
| NFR-C4 | The system shall send payment and status notifications to the Client within 1 minute of the event.                              |
| NFR-C5 | The system shall process simultaneous booking requests for the same slot so that no double booking can occur.                   |
| NFR-C6 | The system shall be usable in current versions of common web browsers on desktop and mobile screens.                            |
| NFR-C7 | The system shall reject a transaction ID that has already been used for another booking.                                        |
