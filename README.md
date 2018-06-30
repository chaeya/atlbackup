# Overview

Backup script for Atalssian products

## Enviroment 

postgresql with Atlassian Stacks(Jira, Confluence, Bitbucket, Bamboo) and sonarqube

# Howto

## Download

```
$ wget https://raw.githubusercontent.com/chaeya/atlbackup/master/atlbackup
```

## Edit backup settings

```
# BACKUP ENV
backup_dir="/var/atlassian-backup"
duration=30

# TARGET DIRICTORY ENV
jira_backup_dir="/var/atlassian/application-data/jira"
confluence_backup_dir="/var/atlassian/application-data/confluence/backups"
bitbucket_backup_dir="/var/atlassian/application-data/bitbucket"
bamboo_backup_dir="/var/atlassian/application-data/backups"

# DATABASE INFO
dbuser="DATABASE USER"
dbpasswd="DATABASE PASSWORD"
```

## Copy to cron daily directory

```
$ chmod +x atlbackup
$ sudo cp atlbackup /etc/cron.daily/
$ sudo /etc/init.d/cron restart
```
