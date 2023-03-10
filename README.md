# Update-MOTD
Simple instructions for customizing Debian/Ubuntu Message of the Day Content

## Context
On Debian/Ubuntu, the message displayed to the user upon login is built using the scripts in `/etc/update-motd.d`.  You can modify and augment these scripts to customize this behavior.

## Adding a legal disclaimer
To add a legal disclaimer:
1. Download `01-legal` and `01-legal.txt`into the `etc/update-motd.d` (you will need root privileges)
2. `cd /etc/update-motd.d`
3. `sudo chmod 744 01-legal`
4. `sudo chmod 644 01-legal.txt`
5. Edit 01-legal.txt with any customizations you want.

## Removing the standard "help" text
You may not want to display the rather verbose standard "help" text.  Stopping this is as simple as moving the file aside:

1. `cd /etc/update-motd.d`
2. `sudo mv 10-help-text \#10-help-text`

## Removing the standard "motd-news" text
You may not want to display the rather verbose standard "motd-news" text.  Stopping this is as simple as moving the file aside:

1. `cd /etc/update-motd.d`
2. `sudo mv 50-motd-news \#150-motd-news`
