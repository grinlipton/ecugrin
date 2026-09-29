<p align="center">
  <img src="https://github.com/grinlipton/ecugrin/blob/v1.0.1-Beta/logo.png?raw=true" alt="ECUGRIN Logo" width="420">
</p>

<h1 align="center">ECUGRIN</h1>

<h3 align="center">ALL ECU SOLUTIONS & DATABASES</h3>

<p align="center">
  <strong>Modern ECU file management, analysis and database platform.</strong>
</p>

<p align="center">
  <a href="https://ecugrin.pl">🌐 Website</a>
  &nbsp;•&nbsp;
  <a href="https://discord.gg/42XubFP6F7">💬 Discord</a>
  &nbsp;•&nbsp;
  <a href="https://github.com/grinlipton/ecugrin">📦 GitHub</a>
</p>

---

## 🚀 About

**ECUGRIN** is a modern ECU file management, analysis and database platform designed for automotive calibration workflows, ECU identification and fast access to structured ECU file databases.

The platform is built around one simple idea:

> **Find the right ECU file faster.**

ECUGRIN combines a modern desktop application with a centralized backend, API services and a continuously expanding ECU database.

The platform is designed to make ECU file analysis, identification, searching and database management faster, cleaner and easier to organize.

From a single ECU file to a database containing thousands of files, ECUGRIN is designed to provide a structured and scalable environment for ECU file management.

---

## 🌐 Official Website & Web App

The official ECUGRIN website is now live:

**https://ecugrin.pl**

The website is the main public landing page for ECUGRIN and now includes the **ECUGRIN Web App**.

The Web App provides its own account and application workflows, including:

- 🔐 User registration and login
- 🚪 Logout and return to the main landing page
- 👤 User account and profile settings
- 🔎 Web ECU Matcher
- 📁 Database file search
- 🗄️ Database overview
- 📝 ECU requests
- 🆕 Updates feed
- 👥 ECUGRIN Team administration

The Web App works alongside the Windows client. It does not require the Windows application to be installed in order to use the web account, search and Matcher workflows.

**Website + Web App:**

**https://ecugrin.pl**

---

## 💬 Discord Community

Join the official ECUGRIN Discord:

**https://discord.gg/42XubFP6F7**

Discord is the main communication channel for the project.

Important information about ECUGRIN is published there, including:

- 📢 Project announcements
- 🆕 Application updates
- 🛠️ Development progress
- 🐛 Bug reports
- 💡 Feature discussions
- 🗄️ Database updates
- 🚀 Future plans
- 💬 Community support
- ⚠️ Maintenance information

**For the latest ECUGRIN news and development information, follow the official Discord server.**

---

# 📸 Screenshots

## First Start

The initial ECUGRIN screen displayed when launching the application.

![ECUGRIN First Start](https://github.com/grinlipton/ecugrin/blob/v1.0.1-Beta/first-start.png?raw=true)

## Loading Screen

The loading screen displayed while ECUGRIN initializes the application and prepares the required components.

![ECUGRIN Loading Screen](https://github.com/grinlipton/ecugrin/blob/v1.0.1-Beta/loading-screeen.png?raw=true)

## Main Menu

The main ECUGRIN interface providing access to the application's core functionality.

![ECUGRIN Main Menu](https://github.com/grinlipton/ecugrin/blob/v1.0.1-Beta/menu.png?raw=true)

---

# ⚡ Features

## 🔍 ECU File Analysis

ECUGRIN can analyze ECU files and extract available identification data such as:

- OEM / ECU numbers
- Bosch numbers
- Software information
- Software versions
- ECU type
- File size
- SHA-256
- ECU family information

The analysis process is designed to provide the information required to identify an ECU and find relevant files in the database.

---

## 🗂️ ECU Database

ECUGRIN provides access to a structured ECU file database organized into solution categories:

- `ORIGINAL`
- `STAGE 1`
- `STAGE 2`
- `STAGE 3`
- `DPF OFF`
- `DPF + EGR OFF`
- `EGR OFF`

The database is continuously expanded and improved as the project develops.

---

## 🔎 Fast File Search

Search through the database using:

- File names
- ECU information
- Hardware numbers
- Software numbers
- ECU identification data

The search system is designed to remain responsive as the database grows.

---

## 📁 Universal File Support

ECUGRIN is designed to work with ECU files regardless of their original filename or extension.

Examples:

```text
.bin
.ori
.original
.stock
.stage1
.stage2
.stage3
.egroff
.dpfoff
.egrdpfoff
```

The original source file is not modified during analysis or export.

---

## 🖥️ Windows Client + 🌐 Web App

ECUGRIN is designed as a connected platform with two application layers:

### Windows Client

The desktop client provides the original ECUGRIN workflow for ECU file analysis and database matching.

### Web App

The Web App provides a browser-based environment for accounts and database workflows directly from:

**https://ecugrin.pl**

The Web App includes:

- Account registration
- Login / logout
- User profiles
- ECU Matcher
- File Search
- Database browsing
- Requests
- Updates
- ECUGRIN Team administration

---

## 🔬 Web ECU Matcher

The Web Matcher follows the same general workflow as the desktop Matcher.

The user first selects one of the supported database categories:

```text
ORIGINAL
STAGE 1
STAGE 2
STAGE 3
DPF OFF
DPF + EGR OFF
EGR OFF
```

The ECU file is then analyzed through the ECUGRIN API.

The Web App filters the displayed candidates using a minimum similarity threshold of **60%** and displays up to **20** highest-scoring qualified results.

The Web App also keeps the analyzed source file available for the contribution/download workflow, so the user does not need to select the same ECU file again.

When downloading a matched database file, the user must explicitly consent to submitting the analyzed ECU file as a pending contribution before the selected approved file is downloaded.

---

## 📤 Database Contributions

ECUGRIN can receive user-submitted ECU files as pending database contributions.

A contribution is not automatically treated as an approved database file. Files can be reviewed and managed by the ECUGRIN Team before becoming part of the approved database.

The contribution workflow is designed to help expand the database while keeping manual verification and moderation in place.

---

## 👥 ECUGRIN Team

The Web App includes a dedicated ECUGRIN Team administration layer.

Team members can manage, depending on their assigned permissions:

- Users
- Roles
- ECU database files
- File metadata
- Categories
- Approvals and rejections
- Disabled / restored files
- Reindexing
- File deletion
- ECU requests
- Updates
- Web App settings

Administrative API access remains server-side and is not exposed to normal browser sessions.

---

## 🤝 Partner Features

Partner functionality is **temporarily disabled in the Web App** while the rest of the platform continues to be developed.

The backend/API routes can remain available for future use, but Partner workflows are currently hidden or disabled from the public Web App interface.

---

# 🏗️ Architecture

The current ECUGRIN architecture is separated into application, API and database layers.

```text
Windows Client
      │
      ▼
 ECUGRIN API
      │
      ├── Matcher
      ├── Database
      ├── File Storage
      └── Metadata / Requests / Updates

Web App (PHP)
      │
      ├── MySQL  ← accounts / web settings
      │
      └── ECUGRIN API  ← ECU database / matcher / files

PostgreSQL
      ▲
      │
   ECUGRIN API / Worker
```

The browser does **not** connect directly to PostgreSQL.

The PHP Web App communicates with MySQL server-side for web accounts and communicates server-side with the existing ECUGRIN API for ECU data, matching and file operations.

---

## 🗄️ Database

The current ECUGRIN Web App uses MySQL for account-related data.

The application creates and manages the following tables:

```text
ecugrin_users
ecugrin_login_events
ecugrin_site_settings
```

The ECU backend database remains separate and is accessed through the ECUGRIN API.

---

## 🔐 Security

The Web App is designed so that sensitive backend credentials remain server-side.

- MySQL is only accessed server-side.
- PostgreSQL is never accessed directly by the browser.
- The API admin key is never sent to JavaScript or rendered into public HTML.
- Team pages require the `ECUGRIN_TEAM` role.
- Passwords are stored using `password_hash()`.
- Forms use CSRF protection.
- Profile images are stored outside the public web root when a private data directory is configured.

---

## 🚀 Web App Status

The **ECUGRIN Web App is now running on the official website:**

**https://ecugrin.pl**

This means the project now has a live public web layer in addition to the Windows desktop application.

The Web App is actively developed and will continue to evolve together with the ECUGRIN API and database.

---

## 🛠️ PHP Requirements

Recommended packages for the Web App server:

```bash
sudo apt update
sudo apt install php-fpm php-mysql php-curl php-sodium -y
```

The avatar upload also uses `getimagesize()` to validate uploaded images.

---

## 🌍 Nginx

Point Nginx/PHP-FPM at the Web App directory, not the landing-only package. Keep `/storage` private.

A simple example:

```nginx
server {
    listen 80;
    server_name ecugrin.pl www.ecugrin.pl;

    root /var/www/ecugrin;
    index index.php;

    location / {
        try_files $uri $uri/ /index.php?$query_string;
    }

    location ^~ /storage/ {
        deny all;
        return 404;
    }

    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/run/php/php-fpm.sock;
    }
}
```

Use the actual PHP-FPM socket configured on the server.

---

## ⚙️ Configuration

The Web App reads its main database and server settings from `includes/config.php`.

Environment variables can override the defaults:

```text
ECUGRIN_DB_HOST
ECUGRIN_DB_PORT
ECUGRIN_DB_NAME
ECUGRIN_DB_USER
ECUGRIN_DB_PASS
ECUGRIN_ADMIN_KEY
ECUGRIN_APP_SECRET
ECUGRIN_DATA_DIR
```

The API admin key must match the key configured on the ECUGRIN API server.

**Never expose the admin key in client-side JavaScript, HTML or public repository content.**

---

## 👤 First ECUGRIN TEAM User

Register an account, then assign the Team role to the correct User ID:

```sql
UPDATE ecugrin_users
SET role = 'ECUGRIN_TEAM', updated_at = UTC_TIMESTAMP(6)
WHERE id = 1;
```

Replace `1` with the correct User ID.

---

# 📡 API Integration

The Web App uses the existing ECUGRIN API rather than connecting directly to the ECU PostgreSQL database.

Main public endpoints used by the Web App include:

```text
GET  /api/files/count
GET  /api/files
GET  /api/files/{id}/download
POST /api/files/contribution
POST /api/matcher/analyze
POST /api/requests
GET  /api/updates
```

The backend also provides server-side administrative endpoints for file management, requests and updates.

Partner API routes may still exist for future use, but Partner functionality is currently disabled in the Web App.

---

# 🗺️ Roadmap

ECUGRIN is currently under active development.

Planned and ongoing work includes:

- Continued ECU database expansion
- Matcher improvements
- More complete ECU metadata coverage
- Web App improvements
- Desktop client improvements
- Additional file management tools
- Performance and indexing improvements
- Community-driven database contributions
- Continued API development
- Preparation for leaving Beta

The project is planned to remain free to use.

---

# ⚠️ Verification

ECUGRIN is a database and matching platform. Matching results should always be manually verified before a file is used in a real ECU workflow.

A high similarity result does not by itself replace manual file verification, identification and checksum/integrity checks where applicable.

---

# 📄 Project Status

**Current state:** Active Beta development

**Web App:** Live

**Official site:**

https://ecugrin.pl

**Discord:**

https://discord.gg/42XubFP6F7

**GitHub:**

https://github.com/grinlipton/ecugrin

The target is to continue development through 2026 and work toward leaving Beta by **December 2026**.

---

# ❤️ Credits

**ECUGRIN by grinlipton**

Built for automotive enthusiasts, ECU file workflows and a growing community around structured ECU databases.

---

<p align="center">
  <strong>ECUGRIN — ALL ECU SOLUTIONS & DATABASES</strong>
</p>

<p align="center">
  <a href="https://ecugrin.pl">Website</a>
  &nbsp;•&nbsp;
  <a href="https://discord.gg/42XubFP6F7">Discord</a>
  &nbsp;•&nbsp;
  <a href="https://github.com/grinlipton/ecugrin">GitHub</a>
</p>
