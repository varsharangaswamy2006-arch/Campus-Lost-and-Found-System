# 🎒 Campus Lost & Found System

A simple web app where students and staff can report lost items, post found items, search the listings, and mark items as resolved. Built with **Flask** and **SQLite**.

## Features

- User registration and login (hashed passwords)
- Report a lost or found item with category, location, date, contact info and an optional photo
- Search and filter by keyword, type (lost/found), category and status
- Item detail page with contact info
- Owners (and admins) can mark items as resolved/reopened or delete them
- "My Reports" page for each user
- Responsive layout, no JavaScript framework needed

## Tech stack

- Python 3.9+
- Flask
- SQLite (created automatically on first run)

## Getting started

```bash
# 1. Clone your repo and enter it
git clone <your-repo-url>
cd campus-lost-and-found

# 2. (Optional) create a virtual environment
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the app
python app.py
```

Open http://127.0.0.1:5000 in your browser.

## Default admin account

| Email | Password |
|-------|----------|
| `admin@campus.edu` | `admin123` |

**Change this password (or remove the account) before deploying anywhere public.** Also set a real secret key:

```bash
export SECRET_KEY="a-long-random-string"
```

## Project structure

```
campus-lost-and-found/
├── app.py              # Flask app: routes, DB setup
├── requirements.txt
├── templates/          # Jinja2 HTML templates
├── static/style.css    # Styling
└── uploads/            # Uploaded item photos (git-ignored)
```

## Possible improvements

- Email notifications when a matching item is posted
- Pagination for long listings
- Admin dashboard
- Switch to PostgreSQL for production

## License

MIT – use it freely for your coursework or campus.
