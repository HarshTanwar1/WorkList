<div align="center">

# 📝 WorkList

A clean, multi-user TODO & task management web app built with Django

<p>
  <img src="https://img.shields.io/badge/Python-3.10.10-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Django-4.1.6-092E20?style=for-the-badge&logo=django&logoColor=white" alt="Django" />
  <img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
</p>

</div>

<br>

## 🚀 Overview

**WorkList** is a multi-user task manager where each user registers an account, logs in, and maintains their own personal TODO list. Users can add tasks, edit them, mark them complete or incomplete, and delete them — with everything persisted per user in the database so their list is always there when they return.

The project showcases a full request-to-database flow in Django: **authentication, session management, the ORM, server-side rendering, and a touch of client-side JavaScript** — all wired together in a small, readable codebase.

<br>

## ✨ Features

| Feature                     | Description                                                                              |
| --------------------------- | ---------------------------------------------------------------------------------------- |
| 👤 **User Registration**    | Sign up with a user ID and password, with input validation and duplicate-ID protection   |
| 🔐 **Authentication**       | Secure login backed by Django's built-in auth system and sessions                        |
| ➕ **Add Tasks**            | Create one or many tasks at once — add/remove input fields dynamically before submitting |
| 📋 **View Tasks**           | All of a user's tasks displayed in a clean table after login                             |
| ✅ **Toggle Status**        | Mark tasks complete or incomplete (completed tasks show with strikethrough)              |
| ✏️ **Edit Tasks**           | Update a task's description in place                                                     |
| 🗑️ **Delete Tasks**         | Remove tasks you no longer need                                                          |
| 💾 **Per-User Persistence** | Each user's task list is stored in the database and tied to their account                |

<br>

## 🛠️ Tech Stack

- **Python 3.10.10**
- **Django 4.1.6** — web framework (function-based views, URL routing, template engine)
- **SQLite3** — default database (`db.sqlite3`)
- **Django ORM** — data persistence, including a `JSONField` for storing each user's tasks
- **Django Auth** (`django.contrib.auth`) — registration, authentication & sessions
- **HTML + Django Templates** — server-side rendered UI
- **Vanilla JavaScript** — dynamic add/remove of task fields on the "Add Task" page
- **CSS** — lightweight styling on the task list

<br>

## ⚡ Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/HarshTanwar1/WorkList.git
cd WorkList

# 2. (Recommended) Create and activate a virtual environment
python -m venv venv
source venv/bin/activate          # On Windows: venv\Scripts\activate

# 3. Install Django
pip install django==4.1.6

# 4. Apply database migrations
python manage.py migrate

# 5. Run the development server
python manage.py runserver
```

Then open your browser at **http://127.0.0.1:8000/**, register an account, and start managing your tasks! 🎉

<br>

## 📚 What I Learned

- Setting up a **Django project from scratch** — project vs. app structure, settings, and URL configuration.
- Writing **function-based views** and routing requests with `urls.py`.
- Using Django's built-in **authentication system** (`create_user`, `authenticate`, `login`) and sessions.
- Working with the **Django ORM** and modeling data, including structured storage via a `JSONField`.
- Managing schema changes through **migrations** (see the `TODO/migrations/` history).
- Rendering dynamic UI with the **Django Template Language** (loops, conditionals, `{% csrf_token %}`, `{% url %}`).
- Handling **form submissions** and reading `POST` data (including multiple values via `getlist`).
- Combining **server-side rendering with client-side JavaScript** to build dynamic forms.
- Applying basic **input validation** with regular expressions.

<br>

## 🔮 Future Improvements

- 🔒 **Config:** set `DEBUG = False` and proper `ALLOWED_HOSTS` for production.
- 🛡️ **Access control:** protect views (`add`, `create`, `update`, `save`) with `@login_required`.
- 🧰 **Django Forms / ModelForms:** replace raw `request.POST` handling for cleaner, safer validation.
- 🎨 **UI/UX:** modernize the interface with a CSS framework and replace `alert()` messaging with Django's messages framework.
- 🚪 **Logout & PRG pattern:** add logout and redirect-after-POST to prevent duplicate submissions on refresh.

<br>

---

<div align="center">

⭐ _If you found this project helpful or interesting, consider giving it a star!_ ⭐

</div>
