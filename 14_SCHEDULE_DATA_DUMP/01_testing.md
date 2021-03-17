# Data Dump
## Terminal 1 (update and execute)
```sh
cd /home/ec2-user/su-amazing-leads-data-dump-scripts/crontab
git restore :/
git pull
chmod 777 *.sh
./data_dump.sh
```

## Terminal 2 (logs)
```sh
cd /home/ec2-user/su-amazing-leads-data-dump-scripts/logs
ls
tail -f data_dump_11-03-2021.log 
```

## Terminal 3 (data dump folder)
```sh
cd /home/ec2-user/su-amazing-leads-data-dump-scripts/data_dump/
ls
## today folder
cd 2021-03-16
ls

```

# Google Cloud Upload File with python

