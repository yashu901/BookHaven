# 📚 BookHaven

A clean, lightweight web application for managing a **digital catalog of books and literature**. Developed as a practical college assignment demonstrating end-to-end **Git & GitHub Version Control Workflows** and **Software Test Case Design**.

---

## 📌 Project Overview

**BookHaven** is a digital book catalog that helps readers discover and organize their reading lists.

| Page | Description |
|---|---|
| `index.html` | Home page featuring introductory overview and a curated Featured Books collection |
| `about.html` | About page with project mission and Contact & Support details |

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| **HTML5** | Semantic document structure and navigation |
| **Git** | Distributed version control system |
| **GitHub** | Remote repository hosting and collaboration |
| **PowerShell** | Command-line environment for repository administration |

---

## 📁 Project Structure

```text
BookHaven/
├── .git/                 # Git repository metadata (auto-generated)
├── .gitignore            # Ignores *.log files and temp/ directory
├── index.html            # Home page with Featured Books collection
├── about.html            # About page with Contact & Support section
├── git_commands.txt      # Comprehensive documentation of all 14 Git commands
└── README.md             # Project documentation and test case design
```

---

## 🔄 Git Workflow — Step-by-Step

| Step | Action | Command(s) Used |
|---|---|---|
| **1** | Repository Initialization | `git init`, `git branch -M main` |
| **2** | Initial Commit | `git add index.html about.html`, `git commit -m "..."` |
| **3** | Second Commit — Featured Books | Modified `index.html`, `git add`, `git commit` |
| **4** | Feature Branch Creation | `git checkout -b feature` |
| **5** | Feature Commit — Contact Section | Modified `about.html`, `git add`, `git commit` |
| **6** | Merge to Main | `git checkout main`, `git merge feature` |
| **7** | Ignore Rules | Created `.gitignore`, verified with `git status`, then committed |
| **8** | Safe Undo with Revert | `git revert HEAD --no-edit` to undo `temporary.txt` |
| **9** | Documentation | Created and committed `git_commands.txt` |

---

## 📊 Verified Git Commit Graph

```
* 8bfdc9b Add git_commands.txt with all Git commands and explanations
* 24be97c Revert "Add temporary.txt for testing revert"
* 98b2b7d Add temporary.txt for testing revert
* 8b1e62f Add .gitignore to ignore log files and temp directory
* a56aaa9 Add contact section to about.html
* 3b69cb7 Update index.html: add featured books collection
* 0060b02 Initial commit: add index.html and about.html
```

> Generated with: `git log --oneline --graph --all`

---

## 🧪 Question 2 — Test Case Design: Login Authentication System

**Application Under Test:** Login System with Username, Password, and Login Button fields.

**Functional Requirements:**
- Username must not be empty.
- Password must be at least 6 characters long.
- Valid credentials allow successful login.
- Invalid credentials display a specific error message.
- Account locked after 3 consecutive failed login attempts.

| Test Case ID | Test Scenario | Input Data | Expected Output |
|:---:|---|---|---|
| **TC_01** | Valid credentials login | Username: `user1`, Password: `password123` | Login successful; redirected to user dashboard |
| **TC_02** | Boundary: exact 6-character password | Username: `user1`, Password: `pass12` (length = 6) | Login successful; minimum character requirement met |
| **TC_03** | Invalid / unregistered username | Username: `unregistered_user`, Password: `password123` | Login denied; *"Invalid username or password"* |
| **TC_04** | Valid username, wrong password | Username: `user1`, Password: `wrongpassword` | Login denied; *"Invalid username or password"* |
| **TC_05** | Boundary: password below 6 characters | Username: `user1`, Password: `12345` (length = 5) | Form blocked; *"Password must be at least 6 characters long"* |
| **TC_06** | Edge case: empty username field | Username: ` ` (empty), Password: `password123` | Form blocked; *"Username must not be empty"* |
| **TC_07** | Edge case: empty password field | Username: `user1`, Password: ` ` (empty) | Form blocked; *"Password must not be empty"* |
| **TC_08** | Security: account lockout after 3 failed attempts | Username: `user1`, 3 consecutive wrong passwords | Account locked; *"Account locked due to 3 consecutive failed login attempts. Please try again after 15 minutes."* |

---

## 🚀 Push to GitHub — Instructions

After creating a **public** repository named `BookHaven` on [github.com/new](https://github.com/new) *(leave all checkboxes unchecked)*, run:

```powershell
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/BookHaven.git
git push -u origin main
git push origin feature
```

---

## 👤 Author

| Field | Detail |
|---|---|
| **Name** | yashu901 |
| **Email** | somethingroy09@gmail.com |
| **Course** | Software Development Practices — Staff Graded Assessment 2 |
| **Date** | November 2026 |
