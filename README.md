# Flask URL-Shortener

## Features

- Shortens URLs to a default 3-digit prefix using a random character and letter combination.
- All data is stored in a single MySQL table.
- Case-sensitive. The database distinguishes between upper- and lower-case characters.
- A Stats page lists all the shortened URLs, and shows how many times a target link has been redirected.
- There is a button to automatically copy the shortened URL to clipboard.
- Please refer the screenshots for results in screenshots directory
- Make use of the correct python version for pip and python during the setup as per your installation
## Setup

- Create a virtualenv
- Install the requirements `pip3 install -r requirements.txt`
- Update settings.py with your own MySQL credentials
- Create the database in MySQL `CREATE DATABASE shortener;`
- Run `python3 create_db.py` to setup the table
- Lastly, alter the MySQL table to allow case-sensitive characters:

`ALTER TABLE url CONVERT TO CHARACTER SET utf8 COLLATE utf8_bin;`

Run the app with `python3 main.py`
