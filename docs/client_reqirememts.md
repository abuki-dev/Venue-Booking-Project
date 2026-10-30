# Client Requirements

## 1. Functional Requirements

### 1.1 Account Management

| ID     | Requirement                                                                                                 |
| ------ | ----------------------------------------------------------------------------------------------------------- |
| CLI-01 | The system shall require a new Client to provide a name, email, phone number and password when registering. |
| CLI-02 | The system shall allow a registered Client to log in with email and password.                               |
| CLI-03 | The system shall allow a logged-in Client to log out.                                                       |
| CLI-04 | The system shall require a visitor to register or log in before sending a booking request.                  |

### 1.2 Browsing and Search

| ID     | Requirement                                                                                                                               |
| ------ | ----------------------------------------------------------------------------------------------------------------------------------------- |
| CLI-05 | The system shall allow any visitor to browse venues without logging in.                                                                   |
| CLI-06 | The system shall allow a visitor to filter venues by category, capacity, location and price.                                              |
| CLI-07 | The system shall display each venue's details: category, capacity, price, location, photos, add-ons, and special offers where applicable. |
| CLI-08 | The system shall display an availability calendar for each venue that shows available and booked dates.                                   |

### 1.3 Booking

| ID     | Requirement                                                                                                                                                                                                                                                    |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CLI-09 | The system shall allow a logged-in Client to submit a booking request containing the venue, date(s), start time, end time, event type, number of guests and selected add-ons.                                                                                  |
| CLI-10 | The system shall check venue availability for the requested date and time before accepting a booking request.                                                                                                                                                  |
| CLI-11 | The system shall re-check availability when the request is submitted and, if two Clients request the same slot at the same time, accept only the first and inform the other that the slot is no longer available and waits 15 min for payment gatwayes result. |
| CLI-12 | The system shall prevent more than one booking for the same venue, date and time.                                                                                                                                                                              |
| CLI-13 | The system shall send booking request details to the Venue Manager for review                                                                                                                                                                                  |

### 1.4 Payment

| ID     | Requirement                                                                                                                                          |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| CLI-14 | The system shall allow the Client intantly pay for a booking using the available payment options (Telebirr, CBE and other banks) .                   |
| CLI-15 | The system shall ask the Client to enter the transaction ID of the payment.                                                                          |
| CLI-16 | The system shall verify the payment by itself using the transaction ID entered by the Client.                                                        |
| CLI-17 | The system shall notify the Client whether the payment was verified or declined.                                                                     |
| CLI-18 | The system shall allow the Client to contact the Venue Manager when the payment was made but verification failed.                                    |
| CLI-19 | The system shall allow the Venue Manager to Review failed payment verifications.                                                                     |
| CLI-20 | The system shall calculate the total amount to pay as the number of days the Client selects for the booking multiplied by the venue's price per day. |
| CLI-20 | The system shall add the price of any selected add-ons to the total amount.                                                                          |
| CLI-22 | The system shall display the calculated total to the Client before the Client pays.                                                                  |
| CLI-23 | The system shall recalculate the total automatically if the Client changes the selected days or add-ons.                                             |
| CLI-24 | The system shall reject a booking request whose end date is before its start date.                                                                   |     |

### 1.5 Refund

| ID     | Requirement                                                                                                                                                     |
| ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CLI-25 | The system shall allow the Venue Manager to mark a confirmed booking as "event not held" (for example, if the venue cancels or the event could not take place). |
| CLI-26 | The system shall create a refund request automatically when a paid booking is marked "event not held".                                                          |
| CLI-27 | The system shall allow the Venue Manager to review the refund request and approve it, after checking the payment record (transaction ID, amount and date).      |
| CLI-28 | The system shall refund the Client the amount paid for the booking, through the same payment method used for the payment.                                       |
| CLI-29 | The system shall record the refund status (requested, approved, completed, rejected) and link it to the booking.                                                |
| CLI-30 | The system shall notify the Client of the refund and each change in its status.                                                                                 |
| CLI-31 | The system shall release the venue slot again for new bookings once the booking is marked "event not held".                                                     |

### 1.6 Status and Notifications

| ID     | Requirement                                                                                                                                              |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CLI-32 | The system shall allow a Client to view the status of their booking request (pending, payment verified, payment failed, confirmed, cancelled, refunded). |
| CLI-34 | The system shall notify the Client when the status of their booking changes.                                                                             |
| CLI-35 | The system shall allow a Client to view their booking history.                                                                                           |

### 1.7 Cancellation

| ID     | Requirement                                                                                    |
| ------ | ---------------------------------------------------------------------------------------------- |
| CLI-36 | The system shall allow the Client to cancel a booking request before the payment is confirmed. |
| CLI-37 | The system shall not allow the Client to cancel a booking after the payment is confirmed.      |

### 1.8 Access Control

| ID     | Requirement                                                                                                             |
| ------ | ----------------------------------------------------------------------------------------------------------------------- |
| CLI-38 | The system shall not allow a Client to view other users' booking data or access administrator and management functions. |
