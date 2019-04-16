# Quickstart
Populate google calendar with events from your notepad

## Who is this for
For people who have a lot of events in their notepad and are bored to manually insert them on google calendar (or have way too many events to do it manually)

## How to run this
Note: this tool uses Python3

1. Install Requirements
```
pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib
```

2. To use this tool you need to enable the google calendar API and get your credentials. To do this you can go to [https://developers.google.com/calendar/quickstart/python](https://developers.google.com/calendar/quickstart/python), enable the API and move *credentials.json* to this directory.
Another option is to do it through the google developer console.

3. After getting the credentials open *new_events.txt* and put inside the events you want to include (newline separated).
Example file (found at: *example_new_events.txt*)
```
Birthday John Smith April 18 repeat every year
Groceries from city centre repeat every week on Saturday 10am
Haircut April 25 repeat every month
Dentist appointment April 30 2019 at 15:00
Brush teeth 12:00 - 13:00 repeat every day
```

4. Then just run the script to add the events
```
$ python add_events.py
```
The first time, this will take you through an authentication flow, where you need to authorize the program to add events to your calendar. Your authentication token is saved in *token.pickle*.
