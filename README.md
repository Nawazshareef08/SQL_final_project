# ✈️ Airline Reservation System using SQL

This project simulates an airline seat booking system using SQL. It includes a complete relational database schema, sample data, and a stored procedure that manages bookings and prevents seat duplication.

---

## 📌 Features

- Book seats for passengers on specific flights
- Prevent double booking using a stored procedure
- Track reservations and payments
- Display confirmed bookings
- Scalable schema for real-world use

---

## 🧱 Database Structure

The system includes the following tables:

- `Airports` – Stores airport information
- `Aircrafts` – Aircraft model and capacity
- `Flights` – Flight details and schedule
- `Passengers` – Passenger info
- `Reservations` – Seat bookings
- `Payments` – Payment for bookings

---

## ⚙️ Technologies Used

- SQL (DDL, DML, Stored Procedures)
- MySQL 
- MySQL Workbench 

---

## 📥 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/airline-reservation-system-sql.git
   cd airline-reservation-system-sql
Open airline_reservation_system.sql in your SQL client (MySQL or SQLite).

Execute the file to create tables and insert sample data.

Call the booking procedure:

sql
Copy
Edit
CALL BookSeat(101, 201, '12A', 5500.00, @status);
SELECT @status;
🧠 Stored Procedure Logic
Procedure: BookSeat

Checks if a seat is already booked on a flight.

If available:

Inserts booking into Reservations

Adds payment entry

Returns "Booking successful"

If already booked:

Returns "Seat already booked"

📊 Sample Queries
sql
Copy
Edit
-- View confirmed seats
SELECT seat_number FROM Reservations WHERE flight_id = 101 AND status = 'confirmed';

-- Try booking
CALL BookSeat(101, 202, '12A', 5500.00, @status);
SELECT @status;
📄 Project Report
A detailed 2-page project report is included in the repository:

Airline_Reservation_System_Project_Report.docx

🛠 Future Enhancements
Add booking cancellation

Create a web frontend (PHP/Flask)

Deploy database to AWS or Railway

📚 Author

Name: Nawaz shareef Shaik

GitHub: https://github.com/Nawazshareef08
