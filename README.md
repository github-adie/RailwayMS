# Railway Reservation System

This project is a simple Railway Reservation System implemented using Streamlit and SQLite. It allows administrators to add and delete trains, view trains, search for trains, book tickets, cancel tickets, and view seats.

## Features

- **Add Train**: Add a new train to the database.
- **View Trains**: View all trains available in the database.
- **Search Train**: Search for a train by train number or by starting and ending destinations.
- **Delete Train**: Delete a train from the database.
- **Book Ticket**: Book a ticket for a specific train.
- **Cancel Ticket**: Cancel a booked ticket.
- **View Seats**: View the seating arrangement of a specific train.

## Setup and Installation

1. **Clone the repository**:
    ```sh
    git clone https://github.com/github-adie/RailwayMS.git
    cd RailwayMS
    ```

2. **Install the required packages**:
    ```sh
    pip install -r requirements.txt
    ```

3. **Run the Streamlit app**:
    ```sh
    streamlit run main.py
    ```

## Database Schema

- **Users Table**: Stores user credentials.
    ```sql
    CREATE TABLE IF NOT EXISTS users (
        username TEXT,
        password TEXT
    );
    ```

- **Employees Table**: Stores employee credentials and designations.
    ```sql
    CREATE TABLE IF NOT EXISTS employees (
        employee_id TEXT,
        password TEXT,
        designation TEXT
    );
    ```

- **Trains Table**: Stores train details.
    ```sql
    CREATE TABLE IF NOT EXISTS trains (
        train_number TEXT,
        train_name TEXT,
        departure_date TEXT,
        starting_destination TEXT,
        ending_destination TEXT
    );
    ```

- **Seats Table**: Dynamic table for each train to store seat information.
    ```sql
    CREATE TABLE IF NOT EXISTS seats_<train_number> (
        seat_number INTEGER PRIMARY KEY,
        seat_type TEXT,
        booked INTEGER,
        passenger_name TEXT,
        passenger_age INTEGER,
        passenger_gender TEXT
    );
    ```

## Functions

- **create_DB_if_Not_available()**: Creates the required database tables if they do not exist.
- **add_train()**: Adds a new train to the database and creates a seat table for it.
- **delete_train()**: Deletes a train from the database.
- **create_seat_table()**: Creates a seat table for a train.
- **categorize_seat()**: Categorizes seats into window, aisle, or middle.
- **allocate_next_available_seat()**: Allocates the next available seat of a specified type.
- **book_ticket()**: Books a ticket for a specific train.
- **cancel_tickets()**: Cancels a booked ticket.
- **search_train_by_train_number()**: Searches for a train by train number.
- **search_trains_by_destinations()**: Searches for trains by starting and ending destinations.
- **view_seats()**: Views the seating arrangement of a specific train.
- **train_functions()**: Streamlit interface for managing train functions.

## Usage

Open the Streamlit app in your web browser and use the sidebar to navigate between different functionalities. Follow the prompts to add trains, book tickets, view trains, and more.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Streamlit for providing an easy-to-use web framework.
- SQLite for the lightweight database.

