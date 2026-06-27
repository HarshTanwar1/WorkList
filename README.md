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

## 🌟 Key Highlights

- 🔐 **Secure multi-user system** powered by Django's built-in authentication and session management.
- 🗄️ **Full CRUD functionality** — create, read, update, and delete tasks, all persisted per user.
- ⚙️ **End-to-end Django workflow** — models, migrations, views, URL routing, and templates working together.
- 🪶 **Lightweight & dependency-free** — runs out of the box on Django + SQLite with no extra setup.
- 📖 **Clean, readable codebase** — a compact project that's easy to follow and build upon.

<br>

## 🛠️ Tech Stack

| Layer         | Technologies                                                                    |
| ------------- | ------------------------------------------------------------------------------- |
| **Language**  | Python 3.10.10                                                                  |
| **Framework** | Django 4.1.6 (function-based views, URL routing, template engine)               |
| **Database**  | SQLite3 with the Django ORM (uses a `JSONField` to store each user's tasks)     |
| **Auth**      | Django Auth (`django.contrib.auth`) for registration, authentication & sessions |
| **Frontend**  | HTML, Django Templates, CSS, and vanilla JavaScript                             |

<br>

## ✨ Features & Functionality

- 👤 **User Registration** — sign up with a user ID and password, with input validation and duplicate-ID protection.
- 🔐 **Authentication** — secure login backed by Django's built-in auth system and sessions.
- ➕ **Add Tasks** — create one or many tasks at once, adding/removing input fields dynamically before submitting.
- 📋 **View Tasks** — all of a user's tasks displayed in a clean table after login.
- ✅ **Toggle Status** — mark tasks complete or incomplete (completed tasks shown with strikethrough).
- ✏️ **Edit Tasks** — update a task's description in place.
- 🗑️ **Delete Tasks** — remove tasks you no longer need.
- 💾 **Per-User Persistence** — each user's task list is stored in the database and tied to their account.

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
