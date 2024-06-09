Railway Management System
This project is a Railway Management System built using Python, Streamlit, and SQLite. It provides a user-friendly interface for administrators to manage train schedules, book tickets, and view train details. The system allows for adding, deleting, searching, and viewing trains, as well as booking and canceling tickets.
Problem Statement
Managing train schedules, booking tickets, and tracking passenger details can be a cumbersome and error-prone process when done manually. Traditional methods often lead to inefficiencies, such as double-booking, difficulty in tracking train schedules, and errors in passenger information management. This project aims to solve these problems by providing a streamlined, automated, and user-friendly system that ensures accurate and efficient management of railway operations.
Features
•	Add Train: Allows administrators to add new trains to the database.
•	View Trains: Displays a list of all available trains.
•	Search Train: Enables searching for trains by train number or by starting and ending destinations.
•	Delete Train: Allows for the deletion of trains from the database.
•	Book Ticket: Facilitates the booking of tickets for passengers.
•	Cancel Ticket: Enables the cancellation of booked tickets.
•	View Seats: Displays the seating arrangement and booking status of a specific train.
Technologies Used
•	Python: The core programming language used for developing the application.
•	Streamlit: A framework used to create the web interface of the application.
•	SQLite: A lightweight database used to store train and booking information.
Setup and Installation
1.	Clone the Repository:
git clone https://github.com/yourusername/railway-management-system.git
cd railway-management-system
2.	Create and Activate a Virtual Environment:
python -m venv venv
source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
3.	Install Dependencies:
pip install -r requirements.txt
4.	Run the Application:
  streamlit run railway_management.py
Project Structure
•	railway_management.py: The main application file containing the Streamlit interface and database operations.
•	requirements.txt: A file listing all the dependencies required for the project.
Database Schema
•	users: Stores user credentials.
o	username: Text, unique identifier for the user.
o	password: Text, password for the user.
•	employees: Stores employee details.
o	employee_id: Text, unique identifier for the employee.
o	password: Text, password for the employee.
o	designation: Text, designation of the employee.
•	trains: Stores train details.
o	train_number: Text, unique identifier for the train.
o	train_name: Text, name of the train.
o	departure_date: Text, departure date of the train.
o	starting_destination: Text, starting location of the train.
o	ending_destination: Text, ending location of the train.
•	seats_[train_number]: Stores seat details for each train.
o	seat_number: Integer, unique identifier for the seat.
o	seat_type: Text, type of the seat (Window, Aisle, Middle).
o	booked: Integer, booking status (0 for available, 1 for booked).
o	passenger_name: Text, name of the passenger.
o	passenger_age: Integer, age of the passenger.
o	passenger_gender: Text, gender of the passenger.
Usage
Adding a Train
1.	Select "Add Train" from the sidebar.
2.	Fill in the train details (Train Number, Train Name, Departure Date, Starting Destination, Ending Destination).
3.	Click "Add Train" to save the train to the database.
Viewing Trains
1.	Select "View Trains" from the sidebar.
2.	All available trains will be displayed in a table format.
Searching for Trains
1.	Select "Search Train" from the sidebar.
2.	You can search by Train Number or by Starting and Ending Destinations.
3.	Enter the search criteria and click the corresponding button to view the search results.
Deleting a Train
1.	Select "Delete Train" from the sidebar.
2.	Enter the Train Number and Departure Date.
3.	Click "Delete Train" to remove the train from the database.
Booking a Ticket
1.	Select "Book Ticket" from the sidebar.
2.	Enter the train number, passenger details (Name, Age, Gender), and seat type.
3.	Click "Book Ticket" to book the ticket.
Canceling a Ticket
1.	Select "Cancel Ticket" from the sidebar.
2.	Enter the Train Number and Seat Number.
3.	Click "Cancel Ticket" to cancel the booking.
Viewing Seats
1.	Select "View Seats" from the sidebar.
2.	Enter the Train Number.
3.	Click "Submit" to view the seating arrangement and booking status.
Contributing
Contributions are welcome! Please create an issue or submit a pull request for any improvements or bug fixes.
License
This project is licensed under the MIT License. See the LICENSE file for more details.


