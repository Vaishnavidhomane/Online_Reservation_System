# Online Reservation System (Java)

A console-based train ticket reservation system built during my Java Development Internship at Oasis Infobyte.

## Features
- User registration and login
- Train mapping — select from a list of available train numbers, with train name auto-filled
- Ticket booking with journey details (from, to, date, class) and a booking confirmation step
- PNR generation for each booked ticket
- PNR-based ticket cancellation, with a confirmation step before removal
- View all current bookings

## Design
Split across four classes:
- **`Final.java`** — entry point; handles the top-level menu (sign up / login / exit) and the logged-in user's action menu
- **`User.java`** — represents a registered user and handles login verification
- **`ReservationSystem.java`** — core business logic: booking, cancellation, and viewing tickets; maintains the train number → train name mapping
- **`Ticket.java`** — represents a single booking, with an auto-incrementing PNR assigned on creation

## Tech Stack
Java — collections (`ArrayList`, `HashMap`), `Scanner` for console I/O

## How to Run
```bash
javac *.java
java Final
```

## Known Limitations
- All data (users, bookings) is stored in memory and lost when the program exits — no persistent storage.
- Passwords are stored and compared in plaintext.
