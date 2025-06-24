# Pharmacy_managements

# SCITEX Pharmacy Management System

## Functional Requirements

1. **User Account and Role Management**
   - Users must create an account using a unique username and password.
   - The system must assign roles (Admin or Staff) with different permission levels.
   - Users must log in to access system features appropriate to their role.

2. **Medicine Management**
   - Admin must be able to add new medicine with attributes such as name, brand, category, dosage, and price.
   - Admin must update medicine records if there are changes in information.
   - Admin must delete medicine records when they are discontinued or invalid.

3. **Stock Management**
   - Users must be able to add stock when new inventory arrives.
   - Users must update stock quantities when medicines are sold, returned, or adjusted.

4. **Expiry Management**
   - The system must store expiry dates and automatically classify medicine as **Valid**, **Near Expiry**, or **Expired**.
   - Automatic status updates must occur daily or upon login.

5. **Sales Management**
   - Staff must record every sale transaction with details including medicine, quantity, and unit price.
   - System must calculate the total bill automatically.

6. **Customer Management**
   - System must store customer details including name, phone number, and purchase history.
   - Users must be able to retrieve customer records for support or future transactions.
   - Access to customer data must be restricted and encrypted.

7. **Supplier Management**
   - Users must register supplier information including name and contact details.
   - The system must link medicines to their respective suppliers.
   - Supply history must be stored for auditing and reorder tracking.

8. **Medicine Search and Filter**
   - Users must search for medicines by name, brand, or category.
   - Users must filter search results by expiry status, price range, or availability.

9. **User Activity Logging**
   - System must log all user actions (add, edit, delete).
   - Each log entry must include a timestamp and user ID.
   - Admin must have access to view the activity log.

10. **Validation and Data Integrity**
   - The system must validate that quantities and prices are non-negative.
   - Duplicate medicine entries are not allowed.
   - Medicines with expiry dates in the past cannot be added.

---

## Non-Functional Requirements

1. **Usability**
   - User interface must be intuitive and easy to use for both technical and non-technical users.
   - The system should include form validation and helpful tooltips.

2. **Performance**
   - Page load and actions must be completed within 2 seconds under normal usage.
   - The system must support at least 20 concurrent users without delay.

3. **Security**
   - Authentication (login) and role-based authorization must be implemented.
   - All sensitive data must be encrypted, including passwords and customer details.

4. **Scalability**
   - The architecture must support the addition of new modules (e.g., e-prescription, delivery tracking).
   - Database and backend must be able to scale vertically or horizontally.

5. **Data Backup and Recovery**
   - Automatic daily backups must be enabled.
   - Admins must be able to restore the system to the last known stable backup.

---

## Software Architecture

The system uses a **3-tier architecture**:

### 1. Presentation Layer (Frontend)
- Built using **React.js** or **HTML/CSS/JS** (for simplicity)
- Responsive layout for desktop and tablet
- Handles login, navigation, and all user interfaces

### 2. Application Layer (Backend/API)
- Built using **Node.js with Express**
- Handles all business logic, API endpoints, and session management
- Implements JWT-based authentication for security

### 3. Data Layer (Database)
- **MySQL** or **PostgreSQL** for structured relational data
- Tables: Users, Medicines, Stock, Sales, Customers, Suppliers, ActivityLog

---

## Technology Stack Justification

| Component | Technology     | Justification |
|----------|----------------|---------------|
| Frontend | React.js / HTML/CSS/JS | Popular, component-based, fast rendering |
| Backend  | Node.js with Express | Lightweight, scalable, and widely supported |
| Database | MySQL / PostgreSQL   | Reliable RDBMS with strong data integrity |
| Version Control | Git + GitHub | Supports collaboration and history tracking |
| Security | JWT, bcrypt       | Secure login and password hashing |

---