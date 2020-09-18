![](http://media.charlesleifer.com/blog/photos/sqlite-web.png)

`sqlite-web` is a web-based SQLite database browser written in Python.

Project dependencies:

* [flask](http://flask.pocoo.org)
* [peewee](http://docs.peewee-orm.com)
* [pygments](http://pygments.org)
* [pyopenssl](https://www.pyopenssl.org)

### Installation

```sh
$ pip3 install sqlite-web-jmalabanan
```

### Usage

```sh
$ sqlite_web /path/to/database.db /parent/path/to/databases
```

### Features
* Works with your existing SQLite databases, or can be used to create new databases.
* Add or drop:
  * Tables
  * Columns (yes, you can drop and rename columns!)
  * Indexes
* Export data as JSON or CSV.
* Import JSON or CSV files.
* Browse table data.
* Search directories for database files
* Database switching

### Screenshots

https://github.com/jmalab1/sqlite-web/tree/master/screenshots

### Command-line options

The syntax for invoking sqlite-web is:

```console

$ sqlite_web [options] /path/to/database-file.db /parent/path/to/databases
```

The following options are available:

* ``-p``, ``--port``: default is 8080
* ``-H``, ``--host``: default is localhost
* ``-d``, ``--debug``: default is false
* ``-x``, ``--no-browser``: do not open a web-browser when sqlite-web starts.
* ``-P``, ``--password``: prompt for password to access sqlite-web.
  Alternatively, the password can be stored in the "SQLITE_WEB_PASSWORD"
  environment variable, in which case the application will not prompt for a
  password, but will use the value from the environment.
* ``-r``, ``--read-only``: open database in read-only mode.
* ``-u``, ``--url-prefix``: URL prefix for application, e.g. "/sqlite-web".
