# Meta Backend Capstone Project README

Welcome to the Meta Backend Capstone project! This project focuses on backend development using Django framework along with Django Rest Framework (DRF), Djoser, and MySQL as the database management system.

## Prerequisites
Before getting started with the project, ensure you have the following prerequisites installed on your system:
- Python (version 3.9 or higher)
- Django
- Django Rest Framework (DRF)
- MySQL

## Setting up the Database
To run this project, you need to have a MySQL database named `littlelemon` on your device. Follow the steps below to set up the database:

1. **Create the MySQL Database:**
    ```bash
    mysql -u your_username -p
    ```

2. **Enter your MySQL password when prompted.**
   
3. **Create the `littlelemon` database:**
    ```sql
    CREATE DATABASE littlelemon;
    ```

4. **Create a MySQL User:**
    ```sql
    CREATE USER 'littlelemon_user'@'localhost' IDENTIFIED BY '123456789';
    ```

5. **Grant Privileges to the User:**
    ```sql
    GRANT ALL PRIVILEGES ON littlelemon.* TO 'littlelemon_user'@'localhost';
    ```

6. **Flush Privileges and Exit MySQL:**
    ```sql
    FLUSH PRIVILEGES;
    EXIT;
    ```

## Installation and Setup
Follow these steps to get the project up and running on your local machine:

1. **Clone the Repository:**
    ```bash
    git clone https://github.com/FamALouiz/LittleLemonCapstone.git
    ```

2. **Navigate to the Project Directory:**
    ```bash
    cd littlelemon
    ```

3. **Install Python Dependencies:**
    ```bash
    pip install django
    pip install djoser
    pip install djangorestframework
    pip install mysqlclient
    ```

4. **Apply Database Migrations:**
    ```bash
    python manage.py migrate
    ```

5. **Run the Development Server:**
    ```bash
    python manage.py runserver
    ```

6. **Access the API:**
    Visit `http://127.0.0.1:8000` in your web browser to access the API.

## Project Structure
- `api/`
  - `menu/`
    - `GET/`: Retrieve all menu items.
    - `POST/`: Create a new menu item. Body: `{"title": "Menu 2", "price": "123.00", "inventory": 3}`
    - `menu/{id}/`: Retrieve a specific menu item by ID.
  - `booking/tables/`
    - `GET/`: Retrieve all bookings.
    - `POST/`: Create a new booking. Body: `{"name": "Fam", "no_of_guests": 4, "booking_date": "2024-12-22"}`
  - `api-token-auth/`: Endpoint for authentication token.

## Testing
To run the test scripts, use the following Django testing command:
```bash
python manage.py test
```

## Contributing
Contributions are welcome! Feel free to open issues and pull requests for bug fixes, feature requests, or general improvements.

## License
This project is licensed under the [MIT License](LICENSE).