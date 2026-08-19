# Anton Boewer

Backend development with Python and Flask. Starting Business Informatics in
September 2026, based in Germany.

## What I build

**[Shiftmates](https://www.shiftmates.org)** — email reminders for your work shifts,
with the weather for the city you commute to. I work rotating shifts and kept checking
the plan on my phone at 11pm, so I built something that mails me instead.

Two processes share a database and never call each other: the Flask app serves requests
and applies migrations on boot, while a separate worker wakes every minute and sends
reminders in each user's own timezone. Passwords are hashed with bcrypt, login locks
after five failed attempts, and the domain is set up with SPF, DKIM and DMARC.

Flask · PostgreSQL · SQLAlchemy · Alembic · APScheduler · Railway

**[fitsize](https://github.com/AntonB1608/fitsize)** — compresses an image to fit under
a target file size. JPEG has a quality setting but no way to ask for a specific number
of kilobytes, so the app binary-searches the quality levels: compress, measure, adjust,
repeat. After about seven passes it has the highest quality that still fits.

Flask · Pillow · Railway

## Tools

Python, Flask, Jinja2, SQLAlchemy, PostgreSQL, SQLite, gunicorn, HTML and CSS, Git

## Contact

antonboewer@icloud.com
