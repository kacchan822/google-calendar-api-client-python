===============
python-google-calendar-api
===============

.. image:: https://travis-ci.org/kacchan822/python-google-calendar-api.svg?branch=master
    :target: https://travis-ci.org/kacchan822/python-google-calendar-api
    :alt: Travis CI

.. image:: https://coveralls.io/repos/github/kacchan822/python-google-calendar-api/badge.svg?branch=master
    :target: https://coveralls.io/github/kacchan822/python-google-calendar-api?branch=master
    :alt: COVERALLS

.. image:: https://codeclimate.com/github/kacchan822/python-google-calendar-api/badges/gpa.svg
   :target: https://codeclimate.com/github/kacchan822/python-google-calendar-api
   :alt: Code Climate

.. image:: https://codeclimate.com/github/kacchan822/python-google-calendar-api/badges/issue_count.svg
   :target: https://codeclimate.com/github/kacchan822/python-google-calendar-api
   :alt: Issue Count

.. image:: https://img.shields.io/badge/license-MIT-blue.svg
   :target: https://raw.githubusercontent.com/kacchan822/python-google-calendar-api/master/LICENSE
   :alt: LICENSE MIT


**python-google-calendar-api** is Google Calendar api client for python3.


Requirement
============

* Python >= 3.5


Quick start
============

1. Install by pip ::

    # install from github master branch
    pip install -U https://github.com/kacchan822/python-google-calendar-api/archive/master.tar.gz


2. Usage ::

    import datetime

    from google_calendar_api.client import GoogleCalendarClient

    CALENDAR_ID = 'XXXXXXXXXXXXXXXXX@group.calendar.google.com'

    client = GoogleCalendarClient(calendar_id=CALENDAR_ID, client_secrete_file='/path/to/client_secret.json')

    events = client.get_events()

    for event in events:
        start = event['start'].get('dateTime', event['start'].get('date'))
        print(start, event['summary'])


Acknowledgements
=================
