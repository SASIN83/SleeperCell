# SleeperCell

It is a sleep tracking web application which visualizes sleep data on a bar graph, gets daily sleep score based on how many hours you slept and weekly average sleep hours. I also attempted to gamify the application to improve sleep quality of users with a leaderboard to checks how punctual you are about your sleep using a discord bot.

Note: I am a Backend developer so please improvise UI as suggested in Issues and also solve some issues in it.

## Features
- A discord bot that tracks sleep and creates habit with gamification.
- Leaderboard of Discord Users
- Daily Sleep Score
- Weekly Average Sleep Hours
- Clock, Login, Registration

## Docs
### Discord Commands
### $setup <timegoal [HH:MM]> <timezone [+/-HH:MM]>

This is probably the only confusing command. Timegoal represents when you want to wake up in 24 hour time (ie 05:00 would be 5am). Timezone represents your offset relative to UTC. For example, IST is +5.30 ahead of UTC, so the timezone would be +05:30. EST would be -05:00 etc. An example of the full command: **setup 18:00 +05:30**

### $reset

Resets your goal, This will also remove your streak. Once you have reset you will need to use $setup again.

### $leaderboard

View the leaderboard ranked by longest active streak.

### $mystats

View your stats including current streak, current goal, target goal and timezone.

### $site

View a live version of the leaderboards, along with help on: [NeuralWorks Sleep Bot Site](https://nw-sleep-bot.herokuapp.com/)

## Setup

- venv (optional)
- pip install -r "requirements.txt"
- Setup mongoDb
- Setup Discord
- Fill out MongoDB and Discord credentials in env and rename to .env

## How to run SleeperCell
After setting up SleeperCell Discord and Database, open Command Prompt or Terminal

```
git clone https://github.com/SASIN83/SleeperCell.git
```
```
cd SleeperCell
```
```
flask run app.py
```

Now head over to http://127.0.0.1:5000/, and you should see your Dashboard.

## SleeperCell's file Working 
- Static folder has all JavaScript and CSS files
- Templates folder has all HTML Template files
- app.py has main funcions, database setup code and flask program
- bot.py has discord bot program
- timezones.py is used to convert your timezone to GMT timezone for Discord Bot
- env file has configuration for Discord and MongoDB
- Procfile can be used to setup gunicorn and server
- dbscript.py has all code for database which is also included directly into app.py due to concurrent files conflict.

**open to all pull requests!**
