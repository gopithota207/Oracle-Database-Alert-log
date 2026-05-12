# Oracle Alert Log ORA Error Monitoring Script

## Overview
This shell script monitors Oracle database alert logs for ORA errors using the `V$DIAG_ALERT_EXT` view.  
If ORA errors are detected within the configured time interval, the script sends an email notification with the report attached.

---

## Features
- Monitors Oracle alert log for `ORA-` errors
- Checks errors generated in the last 480 minutes
- Sends automated email notifications
- Attaches error report when issues are found
- Suitable for cron job scheduling

---

## Prerequisites

### Oracle Requirements
- Oracle Database installed
- SQL*Plus available
- OS authentication enabled for `/ as sysdba`

### Linux Package
Install `mailx` package.

For Oracle Linux / RHEL:
```bash
yum install mailx -y
