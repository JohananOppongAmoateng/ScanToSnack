# ScanToSnack

This is a Django-based web application for managing food ticketing at events. Event organizers can create events, issue tickets for food, and attendees can receive and redeem these tickets via QR codes.

## Features
- Event creation and management
- Ticket generation and assignment to attendees
- QR code generation for food tickets
- Ticket validation and scanning for food redemption
- User authentication for both event organizers and attendees

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/food-ticketing-site.git
    cd food-ticketing-site
    ```

2. Create and activate a virtual environment:
    ```bash
    python3 -m venv venv
    source venv/bin/activate

    # On Windows use: venv\Scripts\activate
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Create a `.env` file in the project root and configure your environment variables (e.g., for database settings, secret keys, etc.) based on the `.env.example` provided.

5. Run migrations to set up the database:
    ```bash
    python manage.py migrate
    ```

6. Create a superuser for accessing the admin dashboard:
    ```bash
    python manage.py createsuperuser
    ```

7. Start the development server:
    ```bash
    python manage.py runserver
    ```

8. Open your browser and navigate to:
    ```
    http://127.0.0.1:8000
    ```

## Usage

1. Log in to the admin panel to create events and generate tickets:
   ```
   http://127.0.0.1:8000/admin
   ```

2. Attendees can log in and receive their tickets, which will be displayed as QR codes.

3. Event staff can scan attendees' QR codes to validate their tickets and redeem food.

## QR Code Functionality

- Each ticket is associated with a unique QR code that attendees will use to redeem food at the event.
- QR codes can be scanned using any mobile device or a dedicated QR code scanner.
- The application verifies the QR code and marks the ticket as redeemed.

## Technologies Used

- **Backend**: Django
- **Frontend**: HTML, CSS, JavaScript
- **Database**: SQLite (default), or PostgreSQL/MySQL for production
- **Authentication**: Django Allauth (optional)
- **QR Code Generation**: `django-qr-code` or `qrcode` Python package

## Contributing

1. Fork the repository.
2. Create a new feature branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -m 'Add new feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
