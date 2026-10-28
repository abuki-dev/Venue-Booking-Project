#Actors and Use Cases:Event venue booking management system(EVBMS)

Actors are the people or outside systems that work with the system.

## Customer

who: The person or group who wants to book a venue for an event.
Note: Anyone can search venues without an account. Booking needs an account.
Use cases: Register, Log In, Search Venue, Check Availability, Book Venue, Cancel Booking, Make Payment, View Booking History

## Admin

Who: The person who manages user accounts and roles, all over the system.
use cases: Log In , Manage Users, Assign Roles, Reset Password, Manage Venue Categories

## Manager / Owner

Who: The person who runs the venue and reviews bookings.
Use cases: Manage Venues, Set Prices, Approve Booking, Reject Booking, Assign Staff Tasks, View Reports, Review Failed Payment

## Staff

Who: The person who does the work on the day of the event.
Use cases: Log In, View My Tasks, Mark Task Done, View Event Schedule, Report Venue Issue

## External Actors

## Payment Gateway

Who: An outside system, not a person. It checks the payment and send back the result.
Note: Verify payment is part of make payment.
Use cases: Verify Payment

The full requirements are in functional_requirements.md
