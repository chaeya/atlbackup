# Overview

Backup script for Atalssian products

## Enviroment 

postgresql with Atlassian Stacks(Jira, Confluence, Bitbucket, Bamboo) and sonarqube

# Howto

## Download

```
$ wget https://raw.githubusercontent.com/chaeya/atlbackup/master/atlbackup
```

## Edit Database User and Password

```
dbuser="DATABASE USER"
dbpasswd="DATABASE PASSWORD"
```

## Copy to cron daily directory

```
$ chmod +x atlbackup
$ sudo cp atlbackup /etc/cron.daily/
$ sudo /etc/init.d/cron restart
```
