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
```sh
sudo yum install git
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