# College Notes Management System


## 4. Technology Stack
- **Backend**: Core PHP 8.0, 8.1, 8.2, 8.3+
- **Database**: MySQL 8.0+ / MariaDB 10.4+ (InnoDB engine, utf8mb4 encoding)
- **Database Driver**: PHP Data Objects (PDO) with strict parameterized prepared statements
- **Frontend**: HTML5, CSS3, JavaScript (ES6+), Bootstrap 5.3.3, Font Awesome 6.5.2
- **Web Server**: Apache 2.4+ (with `mod_rewrite` and `mod_headers`)

---

## 5. Folder & Directory Structure
```
college-notes/
│
├── assets/
│   ├── css/
│   │   ├── style.css           # Global theme & components
│   │   ├── auth.css            # Split authentication card styling
│   │   ├── dashboard.css       # Student & teacher portal layouts
│   │   └── admin.css           # High-density admin controls & badges
│   │
│   ├── js/
│   │   ├── main.js             # Navigation, alerts, mobile toggler
│   │   ├── auth.js             # Client password toggler & validations
│   │   └── dashboard.js        # File size/type checks, filter submits
│   │
│   ├── img/                    # Logos and graphics
│   ├── icons/                  # Icon resources
│   └── uploads/
│       ├── .htaccess           # Prevents PHP script execution in uploads
│       └── notes/              # Sanitized unique document files
│
├── includes/
│   ├── config.php              # Global configuration & constants
│   ├── db.php                  # PDO Singleton database connection
│   ├── auth.php                # Session timeout, guards (requireRole)
│   ├── functions.php           # XSS escaping, CSRF tokens, rate limiter
│   ├── header.php              # Shared HTML <head> & styling imports
│   ├── footer.php              # Shared HTML footer & script imports
│   ├── navbar.php              # Context-aware top navigation bar
│   └── sidebar.php             # Role-based adaptive sidebar menu
│
├── admin/
│   ├── dashboard.php           # Central administrative control panel
│   ├── login.php               # Separate admin authentication gateway
│   ├── backup.php              # Secure SQL database export utility
│   ├── teachers/
│   │   ├── index.php           # Faculty list, search, and status table
│   │   ├── create.php          # Add verified faculty member
│   │   ├── edit.php            # Edit faculty details & department
│   │   └── delete.php          # Cascade delete faculty member
│   ├── students/
│   │   ├── index.php           # Student roster list & search
│   │   ├── create.php          # Enroll new student account
│   │   ├── edit.php            # Edit student details & semester
│   │   └── delete.php          # Delete student account
│   ├── notes/
│   │   ├── index.php           # Note moderation list & status toggles
│   │   ├── edit.php            # Update note properties & approval
│   │   └── delete.php          # Inappropriate note deletion controller
│   └── subjects/
│       └── index.php           # Academic subjects CRUD
│
├── user/
│   ├── dashboard.php           # Student dashboard with stats & recent notes
│   ├── login.php               # User login form with rate limiting
│   ├── register.php            # Student & teacher tabbed registration
│   ├── logout.php              # Secure session destruction
│   ├── notes.php               # Search, filter, and paginated notes
│   ├── note-view.php           # Embedded PDF viewer & note metadata
│   ├── note-download.php       # Secure stream download & audit recorder
│   ├── profile.php             # Student profile & password update
│   ├── subjects.php            # Subjects directory & note counts
│   └── downloads.php           # Personal student download history
│
├── teacher/
│   ├── dashboard.php           # Teacher dashboard with student engagement
│   ├── notes.php               # Teacher notes management list
│   ├── create-note.php         # Upload new note form with file check
│   ├── edit-note.php           # Edit existing note (strict ownership)
│   ├── delete-note.php         # Delete note & unlink file (ownership check)
│   └── profile.php             # Faculty profile & password management
│
├── index.php                   # Public landing page with features & metrics
├── 404.php                     # Unified 404/403/500 security error handler
├── .htaccess                   # Root security headers & routing
├── database.sql                # Full SQL schema & seed records
└── README.md                   # Comprehensive documentation
```

---

## 6. XAMPP Setup & Installation Guide

### Step 1: Copy Project Files to XAMPP
Copy or move the `college-notes` directory into your XAMPP web root:
```
C:/xampp/htdocs/college-notes/
```

### Step 2: Start Services
1. Open the **XAMPP Control Panel**.
2. Click **Start** for **Apache**.
3. Click **Start** for **MySQL**.

---

## 7. Database Setup & Schema
1. Open your browser and navigate to **phpMyAdmin**:
   ```
   http://localhost/phpmyadmin/
   ```
## 8. System Admin Credentials:

## 9. Student Credentials:

## 10. Faculty Credentials:
