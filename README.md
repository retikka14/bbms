# Blood Bank Management System (BBMS)

A web-based Software Engineering project developed to manage blood donors, donations, blood inventory, recipients, blood requests, and administrative operations.

The **Blood Bank Management System (BBMS)** aims to centralize blood-bank records and streamline essential workflows, including donor registration, donation recording, inventory tracking, blood request management, blood allocation, and fulfillment.

## Project Modules

1. **Donor Management**
2. **Blood Donation & Inventory Management**
3. **Recipient & Blood Request Management**
4. **Admin & Authentication Management**

## Key Features

### 1. Donor Management
- Register donors with personal details and blood-group information.
- View and update donor profiles.
- Maintain donor eligibility information.
- Track donation history for individual donors.

### 2. Blood Donation & Inventory Management
- Record donations with donor details, donation date, blood group, quantity, and status.
- Update inventory based on valid donations.
- View available blood units by blood group and status.
- Search and filter blood inventory records.
- Track blood-unit expiry dates.
- Identify expired units and prevent them from being marked as available.

### 3. Recipient & Blood Request Management
- Register recipients and maintain their records.
- Create blood requests with blood group, quantity, priority, and other required details.
- Validate blood request information.
- Track request statuses: Pending, Approved, Rejected, Allocated, Fulfilled, and Cancelled.
- Allocate compatible available blood units to approved requests.
- Record blood issuance and fulfillment while updating related statuses.

### 4. Admin & Authentication Management
- Provide secure user authentication.
- Implement Role-Based Access Control (RBAC).
- Restrict administrative functions to authorized users.
- Manage user accounts and roles.
- Generate basic reports covering donations, inventory, requests, and fulfillment.
- Maintain audit records for significant administrative and operational activities.

## Team Members & Responsibilities

| Team Member | SRN | Module / Responsibility |
|---|---|---|
| G S Retikka Prasad | PES2UG24AM057 | Admin & Authentication Management |
| Gaganashree R | PES2UG24AM058 | Blood Donation & Inventory Management |
| Jyothika M | PES2UG24AM070 | Recipient & Blood Request Management |
| Durugesh B | PES2UG24AM056 | Donor Management |

Each team member is responsible for developing and maintaining their assigned module in a separate Git branch. Individual modules will be integrated into the main project through Git-based collaboration.

## Technology Stack

| Component | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Backend | Python, Django |
| Database | SQLite (current local development configuration) |
| Version Control | Git, GitHub |

## Security Requirements

The system aims to incorporate the following security measures:

- HTTPS/TLS for secure communication in deployment.
- Secure password hashing.
- Role-Based Access Control (RBAC).
- Input validation and safe database operations.
- Audit logging for significant administrative and operational actions.

## Non-Functional Requirements

The following are the project's target non-functional requirements:

- **Performance:** Common dashboard and search operations should respond within 2 seconds for 90% of requests under the defined test load.
- **Availability:** Target availability of at least 99% during planned operational periods.
- **Usability:** Responsive and understandable interfaces across supported modern browsers.
- **Reliability:** Consistent and recoverable records during validation failures and transaction errors.
- **Maintainability:** Modular code structure that supports testing, debugging, and future enhancements.

## Project Documentation

The project documentation includes:

- Software Requirements Specification (SRS)
- UML Use-Case Diagrams
- Requirements Traceability Matrix (RTM)
- Test Cases and Acceptance Tests

## Project Status

**Currently under development.**

## Getting Started

### Prerequisites

- Python installed
- Git
- pip (Python package manager)

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd Blood-Bank-Management-System
```

### 2. Create and activate a virtual environment

**macOS / Linux**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

**Windows**

```bash
python -m venv .venv
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Apply database migrations

```bash
python manage.py migrate
```

### 5. Create an administrator account

```bash
python manage.py createsuperuser
```

Follow the prompts to configure the administrator credentials.

### 6. Start the development server

```bash
python manage.py runserver
```

### 7. Open the application

Visit:

- **Main application:** http://127.0.0.1:8000/
- **Login:** http://127.0.0.1:8000/accounts/login/
- **Django Admin:** http://127.0.0.1:8000/admin/

The application uses the `config` Django settings module and a local SQLite database (`db_local.sqlite3`).

The integrated application includes pages for donor management, blood inventory, and blood requests. Administrative features are available to appropriately authorized users.

Existing API endpoints are available under `/api/`.

> **Note:** The Django development server is intended for local development and testing, not production deployment.

