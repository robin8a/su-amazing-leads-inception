# AWS cli
```sh
ssh -i "kio-amazing-leads-kp.pem" ubuntu@ec2-34-201-30-214.compute-1.amazonaws.com

curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
sudo apt install unzip
unzip awscliv2.zip
sudo ./aws/install


# You can now run: /usr/local/bin/aws --version
# ubuntu@ip-172-31-1-193:~$ aws

# usage: aws [options] <command> <subcommand> [<subcommand> ...] [parameters]
# To see help text, you can run:

#   aws help
#   aws <command> help
#   aws <command> <subcommand> help

# aws: error: the following arguments are required: command


```


# gcloud

## Install on Ubuntu
[Deb ubuntu](https://cloud.google.com/sdk/docs/install#deb)

```sh
gcloud init
# Welcome! This command will take you through the configuration of gcloud.

# Your current configuration has been set to: [default]

# You can skip diagnostics next time by using the following flag:
#   gcloud init --skip-diagnostics

# Network diagnostic detects and fixes local network connection issues.
# Checking network connection...done.                                                    
# Reachability Check passed.
# Network diagnostic passed (1/1 checks passed).

# You must log in to continue. Would you like to log in (Y/n)?  Y

# Go to the following link in your browser:

#     https://accounts.google.com/o/oauth2/auth?response_type=code&client_id=32555940559.apps.googleusercontent.com&redirect_uri=urn%3Aietf%3Awg%3Aoauth%3A2.0%3Aoob&scope=openid+https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fuserinfo.email+https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fcloud-platform+https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fappengine.admin+https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fcompute+https%3A%2F%2Fwww.googleapis.com%2Fauth%2Faccounts.reauth&state=XK4bjYqhgu3147gTKvOHANHWM1hdD7&prompt=consent&access_type=offline&code_challenge=pPi1oFQqrHFf6d_cKTstGbRPELhFOjgPHfPu2AfFiLU&code_challenge_method=S256

# Enter verification code: 4/1AY0e-g71V7oSl9CFpK2o7ysQ1VLu4Z-BqSHLYkei1BcdAcv3xfCeuFFUq40
# You are logged in as: [robin8a@gmail.com].

# Pick cloud project to use: 
#  [1] kio-sl-emap
#  [2] kl-bbng-aws-identity-pool
#  [3] kl-cambbi-amp
#  [4] lemonwifi-1562249452285
#  [5] prod-enigma-santander
#  [6] stoked-monitor-199921
#  [7] storied-channel-105013
#  [8] su-serverless-ecommerce
#  [9] Create a new project
# Please enter numeric choice or text value (must exactly match list 
# item):  5

# Your current project has been set to: [prod-enigma-santander].

# Do you want to configure a default Compute Region and Zone? (Y/n)?  n

# Created a default .boto configuration file at [/home/ubuntu/.boto]. See this file and
# [https://cloud.google.com/storage/docs/gsutil/commands/config] for more
# information about configuring Google Cloud Storage.
# Your Google Cloud SDK is configured and ready to use!

# * Commands that require authentication will use robin8a@gmail.com by default
# * Commands will reference project `prod-enigma-santander` by default
# Run `gcloud help config` to learn how to change individual settings

# This gcloud configuration is called [default]. You can create additional configurations if you work with multiple accounts and/or projects.
# Run `gcloud topic configurations` to learn more.

# Some things to try next:

# * Run `gcloud --help` to see the Cloud Platform services you can interact with. And run `gcloud help COMMAND` to get help on any gcloud command.
# * Run `gcloud topic --help` to learn about advanced features of the SDK like arg files and output formatting
```


## Configure aws 

```sh
# amazing leads on keeweb
aws configure
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

##
```sh
git restore :/
```