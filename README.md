# uni
# 1 Cron job:
Cron allows Linux and Unix users to run commands or scripts at a given date and time. You can schedule scripts to be executed periodically. Cron is one of the most useful tool in a Linux or UNIX like operating systems. It is usually used for sysadmin jobs such as backups or cleaning /tmp/ directories and more. The cron service (daemon) runs in the background and constantly checks the /etc/crontab file, and /etc/cron.*/ directories. It also checks the /var/spool/cron/ directory.

reference:
http://www.cyberciti.biz/faq/how-do-i-add-jobs-to-cron-under-linux-or-unix-oses/ 
http://www.thegeekstuff.com/2009/06/15-practical-crontab-examples/ 
http://www.thegeekstuff.com/2011/07/cron-every-5-minutes/

# 2 To get the nic card details
  /sbin/lspci | grep net



# 3 ubuntu sudo: /etc/sudoers is world writable sudo: no valid sudoers sources found, quitting sudo: unable to initialize policy plugin

Open two ssh sessions to the target server.
In the first session, get the PID of bash by running:

echo $$

In the second session, start the authentication agent with:

pkttyagent --process (pid from step 2)

Back in the first session, run:

pkexec visudo

# To find the disk usage: 

sudo du -cha --max-depth=1 /var/opt/gitlab/git-data/ | grep -E "G"
