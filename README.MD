# Integrated Event Venue Booking and Management System (EVBMS)

## Project Overview

This project involves building a web system that helps event venues handle their bookings in one place[cite: 1]. Currently, many venues still take bookings by phone, write them in a paper diary, and send deposit details through different chat apps[cite: 1]. This causes double-booking issues, which are often only discovered a few days before the event[cite: 1]. The EVBMS fixes this by checking availability automatically so that a taken date cannot be booked again[cite: 1]. Clients can search for a venue, see open dates, and send booking requests[cite: 1]. Owners or managers can approve requests, track deposits, and once a booking is confirmed, the system assigns tasks to the staff (such as equipment, security, and cleaning) so nothing is forgotten[cite: 1].

## Problems Solved

- **Double booking:** Prevents two people from getting the same venue on the same day[cite: 1].
- **Poor communication:** Eliminates constant client calls asking if a weekend is free, what is included, or how much deposit is required by providing one system where everyone sees up-to-date information[cite: 1].

## Main Goals

- **No double bookings:** The system checks the date and time before saving any booking[cite: 1].
- **Less paperwork:** Requests, approvals, and notifications happen inside the system[cite: 1].
- **Clear payments:** Tracks down payments, balances, and overdue payments[cite: 1].
- **Staff tasks:** Confirmed bookings automatically create checklists for the staff[cite: 1].

## Users (Actors) and Main Features

The system includes five types of users[cite: 1]:

- **Client:** Searches venues by capacity, location, and price, views photos, checks the availability calendar, and follows the status of requests[cite: 1].
- **Venue Owner & Manager:** Views a master calendar, approves or rejects requests, changes prices and add-ons, and views simple reports like monthly income[cite: 1].
- **Staff:** Views only the tasks assigned to them[cite: 1].
- **Admin:** Manages overall system administration.

_Note: The project excludes food catering, ticket sales, and social media marketing to keep the scope manageable[cite: 1]._

## Course Connection and Tools

- **Modeling:** Uses Enterprise Architect for Use Case, Activity, Sequence, and Class diagrams (showing association, aggregation, composition, and inheritance for classes like User, Venue, Booking, Payment, and Task)[cite: 1].
- **Code Generation:** Generates Java code from the models[cite: 1].
- **Version Control:** Uses Git and GitHub with branches and pull requests[cite: 1].
- **Testing:** Uses JUnit tests for methods like checking venue availability and calculating deposits, including normal and boundary test cases for the double-booking check[cite: 1].

## Group Members

1. Abubeker Ahmed (ID: 3696/17)[Leader]
2. Abdulhafiz Muhammed (ID: 0303/17)
3. Ahlam Nuru (ID: 0057/17)
4. Selahudin Ali (ID: 1814/17)
5. Zikra Seid (ID: 0714/17)
