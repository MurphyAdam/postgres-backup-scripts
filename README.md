# postgres-backup-scripts

Automated PostgreSQL database Backup on Linux.

1. - `pg_backup.config` - The main configuration file. This should be the only file which needs user modifications.
2. - `pg_backup.sh` - The normal backup script which will go through each database and save a gzipped and/or a custom format copy of the backup into a date-based directory.
3. - `pg_backup_rotated.sh` - The same as above except it will delete expired backups based on the configuration.
4. - Simple crontab job that runs the backup script at 00:00 on every day-of-week from Sunday through Friday.
5. - Simple pg_dump db, needs manual config

Files 1, 2 and 3 copied from https://wiki.postgresql.org/wiki/Automated_Backup_on_Linux