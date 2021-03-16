# Schedule AWS Lambda function
- https://docs.aws.amazon.com/AmazonCloudWatch/latest/events/RunLambdaSchedule.html

# Export DynamoDB to S3
- https://aws.amazon.com/blogs/aws/new-export-amazon-dynamodb-table-data-to-data-lake-amazon-s3/
- https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DataExport.html

# EC2 cronjobs
- https://docs.aws.amazon.com/opsworks/latest/userguide/workingcookbook-extend-cron.html
- https://www.cumulations.com/blogs/37/How-to-write-Cron-jobs-on-Amazon-Web-ServicesAWS-EC2-server
- https://www.serverless.com/blog/aws-lambda-vs-ec2-for-cron-jobs

# lambda export dynamodb to csv
- https://stackoverflow.com/questions/59988635/exporting-data-from-dynamo-db-to-a-csv-file
- https://docs.aws.amazon.com/textract/latest/dg/examples-export-table-csv.html
- https://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/dynamodb-example-query-scan.html
- https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GettingStarted.NodeJs.04.html
- https://medium.com/@quodlibet_be/an-overview-of-tools-to-export-from-dynamoddb-to-csv-d2707ad992ac

# Datapipeline
- https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBPipeline.html
- https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-importexport-ddb-console-start2.html

# AWS Glue
- https://aws.amazon.com/blogs/database/simplify-amazon-dynamodb-data-extraction-and-analysis-by-using-aws-glue-and-amazon-athena/

# Git
- https://git-scm.com/docs/git-restore
  
```sh
sudo yum install git
git restore :/
```

# Setup
```sh
mkdir amazing-leads
aws configure
mkdir scripts
cd scripts
mkdir conf
mkdir crontab
chmod 400 kio-amazing-leads-kp.pem
ssh -i "kio-amazing-leads-kp.pem" ec2-user@ec2-3-89-79-109.compute-1.amazonaws.com

sudo yum update && sudo yum install zsh

```

#

```sh
aws configure list
nano ~/.aws/credentials
export AWS_PROFILE=dunrok

```

# Upload file to Google Cloud Bucket

- https://console.cloud.google.com/getting-started?authuser=1&project=prod-enigma-santander&folder=
- https://stackoverflow.com/questions/37003862/how-to-upload-a-file-to-google-cloud-storage-on-python-3
- https://cloud.google.com/appengine/docs/standard/python/googlecloudstorageclient/read-write-to-cloud-storage
- https://riptutorial.com/google-cloud-storage/example/28256/upload-files-using-python
- https://dzone.com/articles/upload-files-to-google-cloud

## Service Account assign role
- https://www.youtube.com/watch?v=JP019bx33ko

## Install pip
- https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install-linux.html
- https://stackoverflow.com/questions/50840511/google-cloud-import-storage-cannot-import-storage
  
```sh
sudo yum install python37
python3 --version
curl -O https://bootstrap.pypa.io/get-pip.py

pip install --upgrade google-cloud-speech
pip install google-cloud
pip install --upgrade google-cloud-storage

```

# Grant Google Cloud
```sh
gsutil acl ch -u svc_accoubt@projectname.iam.gserviceaccount.com:W gs://bucket_name


gcloud config set project kio-sl-emap
gsutil acl ch -u su-amazing-leads-service-accou@kio-sl-emap.iam.gserviceaccount.com:W gs://su-amazing-leads
```

# Translate tsv to csv
- https://stackoverflow.com/questions/22419979/how-do-i-convert-a-tab-separated-values-tsv-file-to-a-comma-separated-values
  
```sh
tr '\t' ',' < file.tsv > file.csv

tr '\t' ',' < QuestionAnswerDataDump_2021-03-16.tsv > file.csv


tr '\t' ',' < "$data_dump_path$data_dump_today_date/"QuestionAnswerDataDump_$data_dump_today_date.tsv > "$data_dump_path$data_dump_today_date/"QuestionAnswerDataDump_$data_dump_today_date.csv





```



