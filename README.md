# Run a local mysql server

Instructions to run a local server

run docker-compose up -d to get the DB running.

Then run this command.

```shell
 gh-ost \
   --host=127.0.0.1 \
   --user=root \
   --ask-pass \
   --initially-drop-old-table \
   --allow-on-master \
   --database=world \
   --table=city \
   --alter="add description varchar(254) COLLATE utf8_unicode_ci DEFAULT NULL"\
   --execute
```

