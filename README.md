# Flask Api Template

This is a simple template to help start a project off on the right foot.

## Setup
- Setup Virtual Environment
```
$ python -m venv venv
$ source venv/bin/activate
(venv) $ _
```

- Install the packages
```
(venv) $ pip install -r requirements.txt
```

## Running The Server
```
(venv) $ flask run
```

## Database Setup

We're using `flask-migrate` with `alembic` to do our database migrations.  You will notice there is already a migrations folder.  This keeps track of our migrations.  For more information read the [flask-migrate docs](https://flask-migrate.readthedocs.io/en/latest/), [alembic](https://alembic.sqlalchemy.org/en/latest/), or [this tutorial](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-iv-database).

- Setting up an initial migration
  - You only need to do this if your starting fresh.  If you already have migration folder you can skip this step.
```
(venv) $ flask db init
```

- After changing a model run the migrate command
```
(venv) $ flask db migrate -m "Message"
```

- After running the migrate command, run the upgrade command
```
(venv) $ flask db updgrade
```

## Python Flask Shell

Sometimes you need to go into a python repl to test some stuff out.  Run the following command to have access to your flask variables.  Go into the `main.py` to add more values.
```
(venv) $ flask shell
```