# GitHub Traffic Monitor

## How it works?

This app has two parts

-   One is a python script that you run using some tool similar to CRON.
-   This app's second part is a dashboard that you can easily run on your server. Whenever someone visits your website, a call to your database is made to compute new information to display on graph.

                       on every visit

    GitHub -> DataBase --------------> Dashboard

-   You can add support for new database.
-   Already supported, local JSON file, local SQLlite & MongoDB.

## How to use?

### Install packages

```shell
cd <github-traffic-monitor>
pipenv install
pipenv shell
```

### Setup environment variables

```shell
export MONGODB_URI=""
export GITHUB_TOKEN=""
```

### Set the cron job

```shell
crontab ** ** ** main.py
```

### Start the dashboard app

```shell
# From the root directory of github-traffic-monitor
python -m controllers.server serve
```

```shell
# From the root directory of github-traffic-monitor
yarn run server
```
