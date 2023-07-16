## Velero Command

velero install --provider aws --plugins velero/velero-plugin-for-aws:v1.4.1 --bucket cluster-backup --secret-file ./cloud-credentials --use-volume-snapshots=false --backup-location-config region=minio,s3ForcePathStyle="true",s3Url=http://192.168.3.200:9000

## Scheduled backup

velero schedule create daily-backup --schedule="@daily" --ttl 48h0m0s
