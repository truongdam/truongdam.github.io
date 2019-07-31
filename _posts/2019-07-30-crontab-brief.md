The crontab (CRON TABLE) is a list of commands that you want to run on a regular schedule.  

###### Linux Crontab Format
```
MIN HOUR DOM MON DOW  command
```
MIN: miniute field; 0-59

HOUR: hour field; 0-23

DOM: day of month, 1-31

MON: month field; 1-12

DOW: day of week; 0-6


###### Crontab commands
```
crontab -l
crontab -e
crontab -r
```

###### Crontab example
Create a file rpairdb.sh:
```
#!/bin/bash
mysqlcheck -u{username}  -p{password} --auto-repair --check --all-databases
```
```
crontab -e
*    3    *    *    *    /rpairdb.sh
```
Every day, at 3 am, database's repaired on regular schedule.

###### Crontab file location

- Mac OS X
/usr/lib/cron/tabs/

- BSD Unix
/var/cron/tabs/

- Solaris, HP-UX, Debian, Ubuntu
/var/spool/cron/crontabs/

- AIX, Red Hat Linux, CentOS, Ferdora
/var/spool/cron/

###### Disable Email
By default cron jobs sends a email to the user account executing the cronjob. If this is not needed put the following command At the end of the cron job line .

>/dev/null 2>&1

###### Generate log file
To collect the cron execution execution log in a file :

30 18 * * * rm /home/truongdam/tmp/* > /home/truongdam/cronlogs/clean_tmp_dir.log


Ref: [geeksforgeeks](https://www.geeksforgeeks.org/crontab-in-linux-with-examples/) , [adminschoice](https://www.adminschoice.com/crontab-quick-reference)
