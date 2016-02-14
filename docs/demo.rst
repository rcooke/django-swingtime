Demo
====

Swingtime comes with its own demo project and application. The demo is themed as 
a Karate studio's website and allows you see and interact with the Swingtime
application.

Within the Swingtime demo is an app named ``karate``, which defines the custom
management command ``loaddemo``. This command will pre-populate your 
initial database with some events and occurrences based upon the current date and
time.

Currently, Swingtime does not include any templates of its own. The demo project
provides some sample templates to use as a guide or starting point.

Running the demo
----------------

Install the ``swingtime`` project as shown in :ref:`full-project-source-install`.
You can set up your environment to run the demo in a ``virtualenv`` by doing the
following from the root ``swingtime`` project directory::

    $ mkvirtualenv swingtime_demo
    $ pip install -r requirements.txt
    $ cd demo
    $ python manage.py loaddemo
    $ python manage.py runserver


``loaddemo`` is just a simple wrapper around ``migrate`` and a short script to load
some data into your new database - by default, a sqlite3 database named
``karate.db`` - in the root directory of the demo.

.. note:: You can optionally run the development server to check for deprecation warnings::

    $ python -Wd manage.py runserver

Now, you are ready to browse to http://127.0.0.1:8000/
