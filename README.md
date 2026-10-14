# Sivika Studio — E-Commerce Web Application

Sivika Studio is a Flask-based e-commerce web application built with Python, MySQL, HTML, CSS, and JavaScript. It provides customer-facing shopping pages and administrative functionality for managing products, orders, and enquiries.

## Features

### Customer Features
- User registration, login, and logout
- Product listing and product detail pages
- Shopping cart with quantity updates and item removal
- Customer profile and account detail updates
- Checkout and order review pages
- Contact form and custom-order submissions
- Custom-order image uploads

### Order and Payment Features
- Razorpay order creation integration
- Payment-related API endpoints
- Order confirmation page
- PDF invoice generation using ReportLab
- Order and delivery information

### Admin Features
- Admin dashboard
- Product listing, addition, editing, and deletion
- Order management and order status information
- Customer contact enquiry management

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Application logic |
| Flask | Web framework and routing |
| MySQL | Database |
| HTML, CSS, JavaScript | User interface |
| mysql-connector-python | Database connectivity |
| Razorpay Python SDK | Payment gateway integration |
| ReportLab | PDF invoice generation |
| python-dotenv | Environment configuration |

## Project Structure

```text
sivika/
├── certs/                  # Database SSL certificates
├── static/                 # CSS, JavaScript, images and uploads
├── templates/              # HTML templates
├── tests/                  # Test files
├── uploads/custom_orders/  # Custom-order uploads
├── app.py                  # Flask application
├── database.sql            # Database setup script
├── requirements.txt        # Python dependencies
├── .gitignore
└── README.md
```

## Getting Started

### Prerequisites

- Python
- MySQL
- Git
- Razorpay test credentials if testing payment integration

### 1. Clone the repository

```bash
git clone https://github.com/sidddddhi2104/sivika.git
cd sivika
```

### 2. Create and activate a virtual environment

```bash
python -m venv .venv
```

Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file in the project root and configure the values for your local environment.

```dotenv
SECRET_KEY=replace_with_a_random_secret
DB_HOST=localhost
DB_PORT=3306
DB_USER=your_database_user
DB_PASSWORD=your_database_password
DB_NAME=your_database_name
DB_SSL_CA=certs/ca.pem
RAZORPAY_KEY_ID=your_razorpay_test_key_id
RAZORPAY_KEY_SECRET=your_razorpay_test_key_secret
```

Use the database settings appropriate for your environment. Configure SSL according to your database provider and connection requirements.

**Never commit `.env` files or real credentials to GitHub.**

### 5. Set up the database

Review `database.sql` and use it to create the required database and tables, following the instructions in that file.

### 6. Run the application

```bash
python app.py
```

Open the local address displayed by Flask in your terminal.

## Testing

The repository includes a `tests/` directory. Review its test files and setup requirements before running the test suite. Test coverage and execution results should be documented after the tests have been run and verified.

## Security and Development Notes

- Use environment variables for application secrets and database credentials.
- Use secure password hashing and appropriate session configuration.
- Replace hard-coded administrator credentials with a secure authentication mechanism.
- Verify payment signatures on the server before recording an order as paid.
- Configure upload validation and access controls.
- Test database operations and error handling before deployment.

Payment-related code and other application flows require further validation before the application can be considered production-ready.

## Author

Developed by Siddhi Kamble.

GitHub: [sidddddhi2104](https://github.com/sidddddhi2104)
