Description
===========
Installs AIDE, the Advanced Intrusion Detection Environment.

Requirements
============
Tested on Ubuntu 12.04

Attributes
==========
* `node['aide']['custom_rules']` - An Array of lines to be included in the custom rules, defaults to empty
* `node['aide']['mail_to']` - email address to mail the daily logs to, defaults to "root"
* `node['aide']['quiet_reports']` - (YES|NO) if yes, will not send daily report if nothing has changed
* `node['aide']['copy_new_db']` - (YES|NO) if yes, will automatically overwrite the existing database with
                                  the new database.  Differences will only be reported once. (DANGEROUS)

Usage
=====
Just setup the attributes and custom rules, if needed, and include the default recipe in a role.

For configuration that doesn't change (if you always install sysstat, for example) add a file in the files directory
and add it to the recipe to have it installed in /etc/aide/aide.conf.d/

