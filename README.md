# Task-Tracker

Task Tracker is a full-stack to-do list web application. Users can set a deadline 
for each task and opt to receive a daily text reminder through Twilio's API by 
inputting their phone number when they register. Users will only be reminded for 
the task(s) that are due in 24 hours.


<img src="/README_gif/web-homepage.png" alt="Task Tracker homepage" />

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

### Contents

* [Tech Stack](#techstack)
* [Installation](#install)
* [To-do List Features](#features)

## <a name=techstack></a>Tech Stack

**Backend |** Python, Flask, SQLAlchemy, PostgreSQL, cron<br>
**Frontend |** React.js, Material-UI<br>
**APIs |** Twilio

## <a name=install></a>Installation

Create a React App 
```
$ npx create-react-app flask-react-app
$ cd flask-react-app
```

Create a file `secrets.sh` to store [Twilio](https://www.twilio.com/docs) API 
key
```
export TWILIO_ACCOUNT_SID='YOUR_KEY'
export TWILIO_AUTH_TOKEN='YOUR_KEY'
export TWILIO_NUMBER='YOUR_NUMBER'
```
Clone Task Tracker repository
```
$ git clone https://github.com/K-S-Samarth-Rao/Task-Tracker.git
```
Create a virtual environment in the directory and activate environment and 
secrets
```
$ virtualenv env
$ source env/bin/activate
$ source secrets.sh
```
Install dependencies
```
$ pip3 install -r requirements.txt
```
Create database
```
$ createdb todo-list
$ python3 model.py
``` 

Run the app
```
$ python3 server.py
$ npm start
```
Set up a cron job and write a script to execute `send_sms.py` at the time interval of your choice.

View to-do list on localhost:3000 on your browser. 


