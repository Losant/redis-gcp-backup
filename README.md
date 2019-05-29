# Redis GCP Backup

This repo is used to backup a redis instance to a Cloud Storage bucket.

## Usage

Clone this repo (assumes it is cloned to `/root`)

To run this a cronjob, add this to your `/etc/crontab` file:

```
0  */2  * * *   root    /root/redis-gcp-backup/redis-cloud-backup.sh -b gs://$BUCKET_NAME >> /var/log/redis-backup.log 2>&1
```