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
Instance summary for i-00c02549094d1e17a (kio-amazing-leads-data-export)


```sh
mkdir amazing-leads
aws configure
mkdir scripts
cd scripts
mkdir conf
mkdir crontab
chmod 400 kio-amazing-leads-kp.pem
# ssh -i "kio-amazing-leads-kp.pem" ec2-user@ec2-3-89-79-109.compute-1.amazonaws.com
# ssh -i <Your.pem> ec2-user@<YourServerIP>
# ssh -i kio-amazing-leads-kp.pem ec2-user@3.231.213.100

ssh -i "kio-amazing-leads-kp.pem" ec2-user@ec2-3-238-222-251.compute-1.amazonaws.com

```
## zsh

```sh
sudo yum update && sudo yum install zsh
```


## git
```sh
sudo yum install git
git clone https://github.com/robin8a/su-amazing-leads-data-dump-scripts.git
```

## 
```sh
cd ~/su-amazing-leads-data-dump-scripts
cd crontab
chmod 777 *.sh
```

## Configure aws 

```sh
aws configure

```
### Change profile
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
- https://stackoverflow.com/questions/25599503/how-to-upload-folder-on-google-cloud-storage-using-python-api
- https://brianli.com/how-to-automate-file-uploads-to-google-cloud-storage-with-python/
- https://superuser.com/questions/594046/how-can-i-upload-folders-to-google-cloud
- https://sametkaradag.medium.com/how-to-upload-files-to-google-cloud-storage-gcs-bucket-70f9599a01e5


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


# GS Util

## Install

-  https://cloud.google.com/storage/docs/gsutil_install#linux  

```sh
curl -O https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/google-cloud-sdk-337.0.0-linux-x86_64.tar.gz
tar -xf google-cloud-sdk-337.0.0-linux-x86_64.tar.gz

./google-cloud-sdk/install.sh


Welcome to the Google Cloud SDK!

To help improve the quality of this product, we collect anonymized usage data
and anonymized stacktraces when crashes are encountered; additional information
is available at <https://cloud.google.com/sdk/usage-statistics>. This data is
handled in accordance with our privacy policy
<https://cloud.google.com/terms/cloud-privacy-notice>. You may choose to opt in this
collection now (by choosing 'Y' at the below prompt), or at any time in the
future by running the following command:

    gcloud config set disable_usage_reporting false

Do you want to help improve the Google Cloud SDK (y/N)?  y


Your current Cloud SDK version is: 331.0.0
The latest available version is: 332.0.0

┌───────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                                   Components                                                  │
├──────────────────┬──────────────────────────────────────────────────────┬──────────────────────────┬──────────┤
│      Status      │                         Name                         │            ID            │   Size   │
├──────────────────┼──────────────────────────────────────────────────────┼──────────────────────────┼──────────┤
│ Update Available │ Cloud SDK Core Libraries                             │ core                     │ 17.6 MiB │
│ Not Installed    │ App Engine Go Extensions                             │ app-engine-go            │  4.9 MiB │
│ Not Installed    │ Appctl                                               │ appctl                   │ 21.0 MiB │
│ Not Installed    │ Cloud Bigtable Command Line Tool                     │ cbt                      │  7.7 MiB │
│ Not Installed    │ Cloud Bigtable Emulator                              │ bigtable                 │  6.6 MiB │
│ Not Installed    │ Cloud Datalab Command Line Tool                      │ datalab                  │  < 1 MiB │
│ Not Installed    │ Cloud Datastore Emulator                             │ cloud-datastore-emulator │ 18.4 MiB │
│ Not Installed    │ Cloud Firestore Emulator                             │ cloud-firestore-emulator │ 41.6 MiB │
│ Not Installed    │ Cloud Pub/Sub Emulator                               │ pubsub-emulator          │ 60.4 MiB │
│ Not Installed    │ Cloud SQL Proxy                                      │ cloud_sql_proxy          │  7.6 MiB │
│ Not Installed    │ Cloud Spanner Emulator                               │ cloud-spanner-emulator   │ 21.8 MiB │
│ Not Installed    │ Emulator Reverse Proxy                               │ emulator-reverse-proxy   │ 14.5 MiB │
│ Not Installed    │ Google Cloud Build Local Builder                     │ cloud-build-local        │  6.3 MiB │
│ Not Installed    │ Google Container Registry's Docker credential helper │ docker-credential-gcr    │  1.8 MiB │
│ Not Installed    │ Kustomize                                            │ kustomize                │ 25.9 MiB │
│ Not Installed    │ Minikube                                             │ minikube                 │ 23.9 MiB │
│ Not Installed    │ Nomos CLI                                            │ nomos                    │ 20.2 MiB │
│ Not Installed    │ On-Demand Scanning API extraction helper             │ local-extract            │ 12.3 MiB │
│ Not Installed    │ Skaffold                                             │ skaffold                 │ 16.1 MiB │
│ Not Installed    │ anthos-auth                                          │ anthos-auth              │ 16.4 MiB │
│ Not Installed    │ config-connector                                     │ config-connector         │ 43.2 MiB │
│ Not Installed    │ gcloud Alpha Commands                                │ alpha                    │  < 1 MiB │
│ Not Installed    │ gcloud Beta Commands                                 │ beta                     │  < 1 MiB │
│ Not Installed    │ gcloud app Java Extensions                           │ app-engine-java          │ 53.1 MiB │
│ Not Installed    │ gcloud app Python Extensions                         │ app-engine-python        │  6.1 MiB │
│ Not Installed    │ gcloud app Python Extensions (Extra Libraries)       │ app-engine-python-extras │ 27.1 MiB │
│ Not Installed    │ kpt                                                  │ kpt                      │ 11.6 MiB │
│ Not Installed    │ kubectl                                              │ kubectl                  │  < 1 MiB │
│ Not Installed    │ kubectl-oidc                                         │ kubectl-oidc             │ 16.4 MiB │
│ Not Installed    │ pkg                                                  │ pkg                      │          │
│ Installed        │ BigQuery Command Line Tool                           │ bq                       │  < 1 MiB │
│ Installed        │ Cloud Storage Command Line Tool                      │ gsutil                   │  3.9 MiB │
└──────────────────┴──────────────────────────────────────────────────────┴──────────────────────────┴──────────┘
To install or remove components at your current SDK version [331.0.0], run:
  $ gcloud components install COMPONENT_ID
  $ gcloud components remove COMPONENT_ID

To update your SDK installation to the latest version [332.0.0], run:
  $ gcloud components update


Modify profile to update your $PATH and enable shell command 
completion?

Do you want to continue (Y/n)?  Y

The Google Cloud SDK installer will now prompt you to update an rc 
file to bring the Google Cloud CLIs into your environment.

Enter a path to an rc file to update, or leave blank to use 
[/home/ec2-user/.bashrc]:  
Backing up [/home/ec2-user/.bashrc] to [/home/ec2-user/.bashrc.backup].
[/home/ec2-user/.bashrc] has been updated.

==> Start a new shell for the changes to take effect.


For more information on how to get started, please visit:
  https://cloud.google.com/sdk/docs/quickstarts
```

## gcloud init

```sh
./google-cloud-sdk/bin/gcloud init
gcloud init
Welcome! This command will take you through the configuration of gcloud.

Your current configuration has been set to: [default]

You can skip diagnostics next time by using the following flag:
  gcloud init --skip-diagnostics

Network diagnostic detects and fixes local network connection issues.
Checking network connection...done.                                                                                                                                               
Reachability Check passed.
Network diagnostic passed (1/1 checks passed).

You must log in to continue. Would you like to log in (Y/n)?  Y

Go to the following link in your browser:

    https://accounts.google.com/o/oauth2/auth?response_type=code&client_id=32555940559.apps.googleusercontent.com&redirect_uri=urn%3Aietf%3Awg%3Aoauth%3A2.0%3Aoob&scope=openid+https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fuserinfo.email+https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fcloud-platform+https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fappengine.admin+https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fcompute+https%3A%2F%2Fwww.googleapis.com%2Fauth%2Faccounts.reauth&state=VFt6WSxIk4B4kfZN2ccJkCAeXra0ke&prompt=consent&access_type=offline&code_challenge=VZ3ElXmkbYwuUPbxPvEsEq2McVA-dFok5jrdHiBztfU&code_challenge_method=S256

Enter verification code: 4/1AY0e-g47uv50VlcLtFTi3mSmJ6YtT5VOMokQPvgOS9kpB1WLJgcvMlLdblI
You are logged in as: [robin8a@gmail.com].

Pick cloud project to use: 
 [1] kio-sl-emap
 [2] kl-bbng-aws-identity-pool
 [3] kl-cambbi-amp
 [4] lemonwifi-1562249452285
 [5] prod-enigma-santander
 [6] stoked-monitor-199921
 [7] storied-channel-105013
 [8] su-serverless-ecommerce
 [9] Create a new project
Please enter numeric choice or text value (must exactly match list 
item):  1

Your current project has been set to: [kio-sl-emap].

Not setting default zone/region (this feature makes it easier to use
[gcloud compute] by setting an appropriate default value for the
--zone and --region flag).
See https://cloud.google.com/compute/docs/gcloud-compute section on how to set
default compute region and zone manually. If you would like [gcloud init] to be
able to do this for you the next time you run it, make sure the
Compute Engine API is enabled for your project on the
https://console.developers.google.com/apis page.

Created a default .boto configuration file at [/home/ec2-user/.boto]. See this file and
[https://cloud.google.com/storage/docs/gsutil/commands/config] for more
information about configuring Google Cloud Storage.
Your Google Cloud SDK is configured and ready to use!

* Commands that require authentication will use robin8a@gmail.com by default
* Commands will reference project `kio-sl-emap` by default
Run `gcloud help config` to learn how to change individual settings

This gcloud configuration is called [default]. You can create additional configurations if you work with multiple accounts and/or projects.
Run `gcloud topic configurations` to learn more.

Some things to try next:

* Run `gcloud --help` to see the Cloud Platform services you can interact with. And run `gcloud help COMMAND` to get help on any gcloud command.
* Run `gcloud topic --help` to learn about advanced features of the SDK like arg files and output formatting
```

### Testing

```sh
gsutil -m cp -r local_dir gs://my-bucket/data/
gsutil -m cp -r local_dir gs://su-amazing-leads/
gsutil -m cp -r 2021-03-16 gs://su-amazing-leads/

```

- https://medium.com/google-cloud/how-to-use-multiple-accounts-with-gcloud-848fdb53a39a
- 
```sh
export GOOGLE_APPLICATION_CREDENTIALS=/home/lorgan_enigma_dev_gcs_bq_svc_acct.json

gsutil -m cp -r "$data_dump_path$data_dump_today_date" gs://su-amazing-leads/

gsutil -m cp -r README.md gs://santander_inbox/amazing_leads/

```


# Shell Scripting

- https://www.shellscript.sh/