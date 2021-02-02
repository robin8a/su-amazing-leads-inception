# su-amazing-leads-roisense

# Starting React App
```sh
source ~/.bash_profile
npx create-react-app su-amazing-leads-roisense
```
# Bootstrap
```sh
yarn add bootstrap
```

# Amplify

## configure

```sh
amplify configure
```

```sh
amplify configure
Scanning for plugins...
Plugin scan successful
Follow these steps to set up access to your AWS account:

Sign in to your AWS administrator account:
https://console.aws.amazon.com/
Press Enter to continue

Specify the AWS Region
? region:  us-east-1
Specify the username of the new IAM user:
? user name:  su-amazing-leads-roisense-amplify
Complete the user creation using the AWS console
https://console.aws.amazon.com/iam/home?region=undefined#/users$new?step=final&accessKey&userNames=su-amazing-leads-roisense-amplify&permissionType=policies&policies=arn:aws:iam::aws:policy%2FAdministratorAccess
Press Enter to continue

Enter the access key of the newly created user:
? accessKeyId:  AKIASWPUM4**********
? secretAccessKey:  FoJrLzZoKmsLTdq4pQ22********************
This would update/create the AWS Profile in your local machine
? Profile Name:  su-amazing-leads-roisense-amplify

Successfully set up the new user.
```

## init

```sh
amplify init
Note: It is recommended to run this command from the root of your app directory
? Enter a name for the project suamazingleadsroisen
? Enter a name for the environment sualroiapi
? Choose your default editor: Visual Studio Code
? Choose the type of app that you're building javascript
Please tell us about your project
? What javascript framework are you using react
? Source Directory Path:  src
? Distribution Directory Path: build
? Build Command:  npm run-script build
? Start Command: npm run-script start
Using default provider  awscloudformation

For more information on AWS Profiles, see:
https://docs.aws.amazon.com/cli/latest/userguide/cli-multiple-profiles.html

? Do you want to use an AWS profile? Yes
? Please choose the profile you want to use su-amazing-leads-roisense-amplify
Adding backend environment sualroiapi to AWS Amplify Console app: d24zy8rtrv5tqt
⠴ Initializing project in the cloud...

CREATE_IN_PROGRESS UnauthRole                                     AWS::IAM::Role             Tue Feb 02 2021 10:23:34 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS DeploymentBucket                               AWS::S3::Bucket            Tue Feb 02 2021 10:23:34 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS UnauthRole                                     AWS::IAM::Role             Tue Feb 02 2021 10:23:34 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS AuthRole                                       AWS::IAM::Role             Tue Feb 02 2021 10:23:33 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS DeploymentBucket                               AWS::S3::Bucket            Tue Feb 02 2021 10:23:33 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS AuthRole                                       AWS::IAM::Role             Tue Feb 02 2021 10:23:33 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS amplify-suamazingleadsroisen-sualroiapi-102321 AWS::CloudFormation::Stack Tue Feb 02 2021 10:23:29 GMT-0500 (Colombia Standard Time) User Initiated             
⠴ Initializing project in the cloud...

CREATE_COMPLETE UnauthRole AWS::IAM::Role Tue Feb 02 2021 10:23:48 GMT-0500 (Colombia Standard Time) 
CREATE_COMPLETE AuthRole   AWS::IAM::Role Tue Feb 02 2021 10:23:48 GMT-0500 (Colombia Standard Time) 
⠴ Initializing project in the cloud...

CREATE_COMPLETE amplify-suamazingleadsroisen-sualroiapi-102321 AWS::CloudFormation::Stack Tue Feb 02 2021 10:23:57 GMT-0500 (Colombia Standard Time) 
CREATE_COMPLETE DeploymentBucket                               AWS::S3::Bucket            Tue Feb 02 2021 10:23:55 GMT-0500 (Colombia Standard Time) 
✔ Successfully created initial AWS cloud resources for deployments.
✔ Initialized provider successfully.
Initialized your environment successfully.

Your project has been successfully initialized and connected to the cloud!

Some next steps:
"amplify status" will show you what you've added already and if it's locally configured or deployed
"amplify add <category>" will allow you to add features like user login or a backend API
"amplify push" will build all your local backend resources and provision it in the cloud
“amplify console” to open the Amplify Console and view your project status
"amplify publish" will build all your local backend and frontend resources (if you have hosting category added) and provision it in the cloud

Pro tip:
Try "amplify add api" to create a backend API and then "amplify publish" to deploy everything
```

# Codecommit

[Create repo](https://docs.aws.amazon.com/cli/latest/reference/codecommit/create-repository.html)
```sh
nano ~/.aws/credentials
export PATH=~/Library/Python/3.7/bin:$PATH
source ~/.bash_profile
# test
aws s3 ls --profile su-amazing-leads-roisense-amplify
export AWS_PROFILE=su-amazing-leads-roisense-amplify

# aws codecommit create-repository --repository-name MyDemoRepo --repository-description "My demonstration repository" --tags Team=Saanvi
aws codecommit create-repository --repository-name su-amazing-leads-roisense --repository-description "Amazing Leads for Roisense" --tags Team=kio --region us-east-1 

```
<!-- result -->
```json
{
    "repositoryMetadata": {
        "accountId": "185733014839",
        "repositoryId": "bb952eb2-48e2-40d0-b517-90be08cbe0b6",
        "repositoryName": "su-amazing-leads-roisense",
        "repositoryDescription": "Amazing Leads for Roisense",
        "lastModifiedDate": "2021-02-02T10:45:36.787000-05:00",
        "creationDate": "2021-02-02T10:45:36.787000-05:00",
        "cloneUrlHttp": "https://git-codecommit.us-east-1.amazonaws.com/v1/repos/su-amazing-leads-roisense",
        "cloneUrlSsh": "ssh://git-codecommit.us-east-1.amazonaws.com/v1/repos/su-amazing-leads-roisense",
        "Arn": "arn:aws:codecommit:us-east-1:185733014839:su-amazing-leads-roisense"
    }
}
```

# git

```sh
ssh-keygen
/Users/robin8a/.ssh/su_amazing_leads_roisense_rsa

cat ~/.ssh/su_amazing_leads_roisense_rsa.pub

```


```sh
cd ~/.ssh
ls
nano config

# Add

# CodeCommit hosts
Host su_amazing_leads_roisense_rsa
   HostName git-codecommit.us-east-1.amazonaws.com
   User APKASWPUM4U3UL2YM5EG
   IdentityFile ~/.ssh/su_amazing_leads_roisense_rsa

```

https://xiaolishen.medium.com/use-multiple-ssh-keys-for-different-github-accounts-on-the-same-computer-7d7103ca8693

```sh
# git remote -v
# git remote rm origin

git remote add origin ssh://su_amazing_leads_inception_rsa/v1/repos/su-amazing-leads-roisense
git push
```


# Amplify hosting
```sh
amplify add hosting
```

# Navegation

```sh
yarn add react-router-dom
```