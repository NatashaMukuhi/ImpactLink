# ImpactLink

A web platform that matches students and young people with volunteer and community service opportunities using skills, interests, availability, location and accessibility preferences. Built for SWE3090A at USIU-Africa.

**Stack:** HTML, CSS, JavaScript, PHP, MySQL (XAMPP for local development).

**Matching weights:** skills 30%, interests 25%, availability 20%, location 15%, accessibility 10%.

**Project documents** are in the `docs/` folder.


Front end (HTML, CSS, JavaScript) plus a PHP and MySQL backend for sign up and login.

## Set up with XAMPP
1. Install XAMPP and start **Apache** and **MySQL** in the XAMPP control panel.
2. Copy this whole `impactlink` folder into `C:\xampp\htdocs\` (Mac/Linux: the `htdocs` folder of XAMPP).
3. Open **http://localhost/phpmyadmin**, click **Import**, choose `database/impactlink.sql`, click **Go**.
4. Open **http://localhost/impactlink/** in your browser.

Database settings are in `api/config.php` (defaults match a fresh XAMPP: user `root`, empty password).

## Demo accounts (password `demo123`)
`volunteer@demo.com`, `org@demo.com` (also `green@`, `hope@`, `afya@`, `bright@demo.com`).

## What is connected to the database so far
- Sign up and login (`api/signup.php`, `api/login.php`, `api/logout.php`, `api/me.php`). Passwords are hashed with `password_hash`.
- The other pages (opportunities, applications, profile, organization dashboard) still use the browser's localStorage and will be connected next.
- If the PHP server is not reachable (for example the page is opened by double-clicking `index.html`), login and sign up fall back to the offline demo mode.

## Folders
- `api/` PHP endpoints
- `database/impactlink.sql` tables and sample data
- `js/app.js`, `css/style.css`, `*.html` front end
