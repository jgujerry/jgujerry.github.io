# PostgreSQL


## Installation

How to install postgres on to Ubuntu

```bash
$ sudo apt install postgresql postgresql-contrib
```

Check the postgres service status,

```bash
$ sudo systemctl status postgresql.service
```

If not started, then run

```bash
$ sudo systemctl start postgresql.service
```


## Connection

Installed postgres on Ubuntu, then connect to the default database.

Run the command to switch to the default user `postgres`,

```bash
$ sudo -i -u postgres
```

Then connect to the default database `postgres`,

```bash
$ psql -U postgres
```

## Database

Create a new database,

```bash
$ CREATE DATABASE <dbname>
```


## User Creation

Create a new user,

```bash
$ CREATE USER <username> WITH PASSWORD <password>
```

Grant the user privileges to to the database,

```bash
$ GRANT ALL PRIVILEGES ON DATABASE <dbname> TO <username>;
```