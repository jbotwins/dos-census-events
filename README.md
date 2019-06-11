# Census events and resources

Find census events and resources near you.


## "Goals"

- Events and resources
- Partners can enter event information through forms
- Events are published to google calendar
- Export events via CSV
- Integrate with SwORD via CSV export


## Usage

### Create calendar events

[Create an event](http://localhost:8000/admin/census/event/add/).


## Development


### Prerequisites

- Python 3
- virtualenv

We assume you are installing to a python virtualenv.


### More on Prerequisites

Check your versions:

    $ python --version
    $ python3 --version
    $ pip --version
    $ virtualenv --version

Create a virtual environment for a project:
1. cd into the dos-census-events directory

2. Create a virtual environment for a project:
    $ virtualenv .

3. Activate the virtual environment:
    $ source bin/activate

The name of the current virtual environment will now appear on the left of the prompt and you are ready to proceed to the Setup steps. If you are done working in the virtual environment for the moment, you can deactivate it with:

    $ deactivate

Documentation resource: https://docs.python-guide.org/dev/virtualenvs/

### Setup

Install python dependencies.

    $ pip install -r requirements.txt

Initialize the database.

    $ python manage.py migrate

Create an admin user by following the prompts.

    $ python manage.py createsuperuser


### Working with database migrations

Anytime you make a change to the models, you should try to run makemigrations to
generate a database migration.

    $ python manage.py makemigrations census

### Start the server

    $ python manage.py runserver

Quit the server with CONTROL-C.

### Important pages:
1. http://127.0.0.1:8000/
2. http://127.0.0.1:8000/admin
3. http://127.0.0.1:8000/export/events