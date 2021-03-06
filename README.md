# FHWS Grades Push

[![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE)
[![Status](https://git-badges.sebbo.net/35/master/build)](https://git.sebbo.net/fhws/grades-push/pipelines)

Small script to get notified when there're new grades available on the 
"[FHWS Studenten Portal](https://studentenportal.fhws.de/grades)". Uses 
ugly HTML scraping and there's almost no error handling, deal with it. 
Very untested. Such wow.

### Installation

#### Directly

You'll need [node.js](https://nodejs.org/en/) to run this.

```bash
git clone https://github.com/sebbo2002/fhws-grades-push.git
cd ./fhws-grades-push
npm install
```

I use crontab to run this script regularly.


#### Docker

You can also use the docker container to run this script:

```bash
docker pull sebbo2002/fhws-grade-push
```


### Configuration

Use environment variables to set login credentials and pushover tokens:

<table>
    <tr>
        <th scope="row">FHWS_USERNAME</td>
        <td>Your username for the "FHWS Studenten Portal"</td>
    </tr>
    <tr>
        <th scope="row">FHWS_PASSWORD</td>
        <td>Your password for the "FHWS Studenten Portal"</td>
    </tr>
    <tr>
        <th scope="row">PUSHOVER_TOKEN</td>
        <td>Your pushover token. You can get yours <a href="https://pushover.net/apps">here</a>.</td>
    </tr>
    <tr>
        <th scope="row">PUSHOVER_USER</td>
        <td>Your pushover user token. You can get yours <a href="https://pushover.net/">here</a>.</td>
    </tr>
</table>

### Example

```bash
FHWS_USERNAME="k*****" \
FHWS_PASSWORD="*********" \
PUSHOVER_TOKEN="*********" \
PUSHOVER_USER="*********" node app
```

![Such wow, much awesome](https://i.imgur.com/rSzk8wQ.png)
