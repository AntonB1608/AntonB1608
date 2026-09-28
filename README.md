# Anton Boewer

Backend development with Python and Flask. Business Informatics student, based
in Germany. I build small tools that solve problems I actually have, and I run
them in production.

## Projects

### [Shiftmates](https://www.shiftmates.org) · [code](https://github.com/AntonB1608/schichtplan-online)

Email reminders for work shifts: one the evening before, one shortly before
the shift starts. I worked rotating shifts and kept checking the plan on my
phone at 11pm, so I built something that mails me instead.

Two processes share a Postgres database and never call each other: the Flask
app serves requests and applies migrations on boot, a separate worker checks
every minute which reminders are due — in each user's own timezone, deduplicated
so nobody gets the same mail twice. Passwords are hashed with bcrypt, login
locks after five failed attempts, and mails go out over a domain with SPF,
DKIM and DMARC.

`Flask` `PostgreSQL` `SQLAlchemy` `Alembic` `Railway`

### [fitsize](https://www.fitsize.org) · [code](https://github.com/AntonB1608/fitsize)

Compresses an image to fit under a target file size. JPEG has a quality
setting but no way to ask for a specific number of kilobytes, so the app
binary-searches the quality levels: compress, measure, adjust, repeat. After
about seven passes it has the highest quality that still fits. Files are
processed in memory and never stored.

`Flask` `Pillow` `Railway`

## Tools

Python · Flask · Jinja2 · SQLAlchemy · PostgreSQL · SQLite · gunicorn · Git · HTML & CSS

## Contact

antonboewer@icloud.com
