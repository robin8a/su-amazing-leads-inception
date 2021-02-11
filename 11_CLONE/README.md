# su-amazing-leads-roisense
- [Amplify Getting Started](https://docs.amplify.aws/start)
# Starting React App
```sh
source ~/.bash_profile
npx create-react-app su-amazing-leads-roisense
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
# Install libraries

```
npm i react-cursor-position
npm i react-device-detect
npm i react-external-link
npm install aws-amplify @aws-amplify/ui-react
yarn add react-router-dom
npm i aws-amplify @aws-amplify/ui-react
npm i aws-amplify-react
yarn add bootstrap
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

## Result
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

# Amplify api/push/
```sh
amplify add api
```

## result
```sh
amplify add api
? Please select from one of the below mentioned services: GraphQL
? Provide API name: suamazingleadsroisen
? Choose the default authorization type for the API API key
? Enter a description for the API key: suamazingleadsroisen
? After how many days from now the API key should expire (1-365): 365
? Do you want to configure advanced settings for the GraphQL API No, I am done.
? Do you have an annotated GraphQL schema? Yes
? Provide your schema file path: 
>> A response is required for this field
➜  su-amazing-leads-roisense git:(master) ✗ amplify add api
? Please select from one of the below mentioned services: GraphQL
? Provide API name: suamazingleadsroisen
? Choose the default authorization type for the API API key
? Enter a description for the API key: suamazingleadsroisen
? After how many days from now the API key should expire (1-365): 365
? Do you want to configure advanced settings for the GraphQL API No, I am done.
? Do you have an annotated GraphQL schema? No
? Do you want a guided schema creation? Yes
? What best describes your project: Single object with fields (e.g., “Todo” with ID, name, description)
? Do you want to edit the schema now? Yes
Please edit the file in your editor: /Users/robin8a/Documents/react_ws/su-amazing-leads-roisense/amplify/backend/api/suamazingleadsroisen/schema.graphql
? Press enter to continue 

The following types do not have '@auth' enabled. Consider using @auth with @model
         - QuestionaryConfig
         - Questionary
         - QuestionaryInteraction
         - Question
         - Option
         - QuestionAnswer
         - Interaction
Learn more about @auth here: https://aws-amplify.github.io/docs/cli-toolchain/graphql#auth 


GraphQL schema compiled successfully.

Edit your schema at /Users/robin8a/Documents/react_ws/su-amazing-leads-roisense/amplify/backend/api/suamazingleadsroisen/schema.graphql or place .graphql files in a directory at /Users/robin8a/Documents/react_ws/su-amazing-leads-roisense/amplify/backend/api/suamazingleadsroisen/schema
Successfully added resource suamazingleadsroisen locally

Some next steps:
"amplify push" will build all your local backend resources and provision it in the cloud
"amplify publish" will build all your local backend and frontend resources (if you have hosting category added) and provision it in the cloud

➜  su-amazing-leads-roisense git:(master) ✗ amplify push
✔ Successfully pulled backend environment sualroiapi from the cloud.

Current Environment: sualroiapi

| Category | Resource name        | Operation | Provider plugin   |
| -------- | -------------------- | --------- | ----------------- |
| Api      | suamazingleadsroisen | Create    | awscloudformation |
| Hosting  | amplifyhosting       | No Change |                   |
? Are you sure you want to continue? Yes

The following types do not have '@auth' enabled. Consider using @auth with @model
         - QuestionaryConfig
         - Questionary
         - QuestionaryInteraction
         - Question
         - Option
         - QuestionAnswer
         - Interaction
Learn more about @auth here: https://aws-amplify.github.io/docs/cli-toolchain/graphql#auth 


GraphQL schema compiled successfully.

Edit your schema at /Users/robin8a/Documents/react_ws/su-amazing-leads-roisense/amplify/backend/api/suamazingleadsroisen/schema.graphql or place .graphql files in a directory at /Users/robin8a/Documents/react_ws/su-amazing-leads-roisense/amplify/backend/api/suamazingleadsroisen/schema
? Do you want to generate code for your newly created GraphQL API Yes
? Choose the code generation language target javascript
? Enter the file name pattern of graphql queries, mutations and subscriptions src/graphql/**/*.js
? Do you want to generate/update all possible GraphQL operations - queries, mutations and subscriptions Yes
? Enter maximum statement depth [increase from default if your schema is deeply nested] 2
⠸ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS apisuamazingleadsroisen                        AWS::CloudFormation::Stack Tue Feb 02 2021 14:55:00 GMT-0500 (Colombia Standard Time)               
UPDATE_IN_PROGRESS amplify-suamazingleadsroisen-sualroiapi-102321 AWS::CloudFormation::Stack Tue Feb 02 2021 14:54:55 GMT-0500 (Colombia Standard Time) User Initiated
⠦ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS apisuamazingleadsroisen AWS::CloudFormation::Stack Tue Feb 02 2021 14:55:02 GMT-0500 (Colombia Standard Time) Resource creation Initiated
⠙ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazingleadsroisen-18HTK7XGWKE5P AWS::CloudFormation::Stack Tue Feb 02 2021 14:55:00 GMT-0500 (Colombia Standard Time) User Initiated
⠦ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS GraphQLAPI AWS::AppSync::GraphQLApi Tue Feb 02 2021 14:55:10 GMT-0500 (Colombia Standard Time) 
⠙ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS GraphQLSchema AWS::AppSync::GraphQLSchema Tue Feb 02 2021 14:55:15 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS GraphQLAPIKey AWS::AppSync::ApiKey        Tue Feb 02 2021 14:55:15 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    GraphQLAPI    AWS::AppSync::GraphQLApi    Tue Feb 02 2021 14:55:12 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS GraphQLAPI    AWS::AppSync::GraphQLApi    Tue Feb 02 2021 14:55:12 GMT-0500 (Colombia Standard Time) Resource creation Initiated
⠧ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS GraphQLSchema AWS::AppSync::GraphQLSchema Tue Feb 02 2021 14:55:17 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    GraphQLAPIKey AWS::AppSync::ApiKey        Tue Feb 02 2021 14:55:17 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS GraphQLAPIKey AWS::AppSync::ApiKey        Tue Feb 02 2021 14:55:17 GMT-0500 (Colombia Standard Time) Resource creation Initiated
⠙ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE GraphQLSchema AWS::AppSync::GraphQLSchema Tue Feb 02 2021 14:56:18 GMT-0500 (Colombia Standard Time) 
⠙ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS QuestionaryConfig AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:21 GMT-0500 (Colombia Standard Time) 
CREATE_IN_PROGRESS Interaction       AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:21 GMT-0500 (Colombia Standard Time) 
⠙ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS QuestionaryInteraction AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:21 GMT-0500 (Colombia Standard Time) 
CREATE_IN_PROGRESS Option                 AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:21 GMT-0500 (Colombia Standard Time) 
CREATE_IN_PROGRESS QuestionAnswer         AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:21 GMT-0500 (Colombia Standard Time) 
⠙ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS Questionary            AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:23 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionaryInteraction AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:22 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS Option                 AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:22 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionAnswer         AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:22 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS Questionary            AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:22 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS Interaction            AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:22 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionaryConfig      AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:22 GMT-0500 (Colombia Standard Time) Resource creation Initiated
⠦ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazingleadsroisen-18H-Questionary-1WQAPZ9MT2QWK AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:23 GMT-0500 (Colombia Standard Time) User Initiated
⠇ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazingleadsroisen-18HTK7XG-Option-1ARBQAOBJIFGE AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:22 GMT-0500 (Colombia Standard Time) User Initiated
⠋ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazingleadsroisen-QuestionAnswer-177A1J8EOZPRY AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:22 GMT-0500 (Colombia Standard Time) User Initiated


CREATE_IN_PROGRESS amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazinglead-QuestionaryInteraction-1DEOHS1HXIU7T AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:22 GMT-0500 (Colombia Standard Time) User Initiated
⠙ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazingleadsroisen-18H-Interaction-FTNFAIAC1IFC AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:21 GMT-0500 (Colombia Standard Time) User Initiated
⠹ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazingleadsrois-QuestionaryConfig-1G5KNTRDJ6RMR AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:21 GMT-0500 (Colombia Standard Time) User Initiated
⠹ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS QuestionaryInteractionIAMRole AWS::IAM::Role       Tue Feb 02 2021 14:56:29 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionaryInteractionTable   AWS::DynamoDB::Table Tue Feb 02 2021 14:56:29 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionaryInteractionIAMRole AWS::IAM::Role       Tue Feb 02 2021 14:56:28 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionaryInteractionTable   AWS::DynamoDB::Table Tue Feb 02 2021 14:56:28 GMT-0500 (Colombia Standard Time)                            
⠴ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS Question AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:31 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS Question AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:30 GMT-0500 (Colombia Standard Time)                            
⠼ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS OptionIAMRole AWS::IAM::Role       Tue Feb 02 2021 14:56:30 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS OptionTable   AWS::DynamoDB::Table Tue Feb 02 2021 14:56:29 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS OptionIAMRole AWS::IAM::Role       Tue Feb 02 2021 14:56:29 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS OptionTable   AWS::DynamoDB::Table Tue Feb 02 2021 14:56:29 GMT-0500 (Colombia Standard Time)                            


CREATE_IN_PROGRESS amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazingleadsroisen-18HTK7-Question-KWCBQOURBAM8 AWS::CloudFormation::Stack Tue Feb 02 2021 14:56:30 GMT-0500 (Colombia Standard Time) User Initiated
⠧ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS QuestionaryIAMRole AWS::IAM::Role       Tue Feb 02 2021 14:56:30 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionaryTable   AWS::DynamoDB::Table Tue Feb 02 2021 14:56:30 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionaryIAMRole AWS::IAM::Role       Tue Feb 02 2021 14:56:30 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionaryTable   AWS::DynamoDB::Table Tue Feb 02 2021 14:56:30 GMT-0500 (Colombia Standard Time)                            


CREATE_IN_PROGRESS QuestionAnswerIAMRole AWS::IAM::Role       Tue Feb 02 2021 14:56:31 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionAnswerTable   AWS::DynamoDB::Table Tue Feb 02 2021 14:56:30 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionAnswerIAMRole AWS::IAM::Role       Tue Feb 02 2021 14:56:30 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionAnswerTable   AWS::DynamoDB::Table Tue Feb 02 2021 14:56:30 GMT-0500 (Colombia Standard Time)                            
⠇ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS InteractionTable   AWS::DynamoDB::Table Tue Feb 02 2021 14:56:30 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS InteractionIAMRole AWS::IAM::Role       Tue Feb 02 2021 14:56:29 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS InteractionTable   AWS::DynamoDB::Table Tue Feb 02 2021 14:56:29 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS InteractionIAMRole AWS::IAM::Role       Tue Feb 02 2021 14:56:29 GMT-0500 (Colombia Standard Time)                            
⠙ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS QuestionaryConfigIAMRole AWS::IAM::Role       Tue Feb 02 2021 14:56:28 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionaryConfigTable   AWS::DynamoDB::Table Tue Feb 02 2021 14:56:28 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionaryConfigTable   AWS::DynamoDB::Table Tue Feb 02 2021 14:56:28 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionaryConfigIAMRole AWS::IAM::Role       Tue Feb 02 2021 14:56:28 GMT-0500 (Colombia Standard Time)                            
⠋ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS QuestionIAMRole AWS::IAM::Role       Tue Feb 02 2021 14:56:37 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionTable   AWS::DynamoDB::Table Tue Feb 02 2021 14:56:37 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionIAMRole AWS::IAM::Role       Tue Feb 02 2021 14:56:37 GMT-0500 (Colombia Standard Time)                            
⠙ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS QuestionTable AWS::DynamoDB::Table Tue Feb 02 2021 14:56:38 GMT-0500 (Colombia Standard Time) Resource creation Initiated
⠏ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE QuestionaryConfigIAMRole AWS::IAM::Role Tue Feb 02 2021 14:56:42 GMT-0500 (Colombia Standard Time) 
⠋ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE QuestionaryInteractionIAMRole AWS::IAM::Role Tue Feb 02 2021 14:56:42 GMT-0500 (Colombia Standard Time) 
⠼ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE OptionIAMRole AWS::IAM::Role Tue Feb 02 2021 14:56:44 GMT-0500 (Colombia Standard Time) 


CREATE_IN_PROGRESS QuestionaryInteractionDataSource AWS::AppSync::DataSource Tue Feb 02 2021 14:56:45 GMT-0500 (Colombia Standard Time) 
⠦ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE QuestionaryIAMRole AWS::IAM::Role Tue Feb 02 2021 14:56:44 GMT-0500 (Colombia Standard Time) 
⠸ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE    QuestionaryConfigDataSource AWS::AppSync::DataSource Tue Feb 02 2021 14:56:47 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionaryConfigDataSource AWS::AppSync::DataSource Tue Feb 02 2021 14:56:47 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionaryConfigDataSource AWS::AppSync::DataSource Tue Feb 02 2021 14:56:45 GMT-0500 (Colombia Standard Time)                            
⠋ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS QuestionAnswerDataSource AWS::AppSync::DataSource Tue Feb 02 2021 14:56:47 GMT-0500 (Colombia Standard Time) 
CREATE_COMPLETE    QuestionAnswerIAMRole    AWS::IAM::Role           Tue Feb 02 2021 14:56:44 GMT-0500 (Colombia Standard Time) 
⠦ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS DeleteQuestionaryInteractionResolver AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:50 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS ListQuestionaryInteractionResolver   AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:49 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS CreateQuestionaryInteractionResolver AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:49 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS UpdateQuestionaryInteractionResolver AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:49 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS GetQuestionaryInteractionResolver    AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:49 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    QuestionaryInteractionDataSource     AWS::AppSync::DataSource Tue Feb 02 2021 14:56:47 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionaryInteractionDataSource     AWS::AppSync::DataSource Tue Feb 02 2021 14:56:47 GMT-0500 (Colombia Standard Time) Resource creation Initiated
⠇ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE    QuestionaryDataSource AWS::AppSync::DataSource Tue Feb 02 2021 14:56:49 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionaryDataSource AWS::AppSync::DataSource Tue Feb 02 2021 14:56:49 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionaryDataSource AWS::AppSync::DataSource Tue Feb 02 2021 14:56:47 GMT-0500 (Colombia Standard Time)                            
⠸ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS GetInteractionResolver    AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS CreateInteractionResolver AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    ListInteractionResolver   AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS ListInteractionResolver   AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS UpdateInteractionResolver AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS DeleteInteractionResolver AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS GetInteractionResolver    AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:50 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS CreateInteractionResolver AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:50 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS ListInteractionResolver   AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:50 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    InteractionDataSource     AWS::AppSync::DataSource Tue Feb 02 2021 14:56:48 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS InteractionDataSource     AWS::AppSync::DataSource Tue Feb 02 2021 14:56:48 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS InteractionDataSource     AWS::AppSync::DataSource Tue Feb 02 2021 14:56:46 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    InteractionIAMRole        AWS::IAM::Role           Tue Feb 02 2021 14:56:43 GMT-0500 (Colombia Standard Time)                            
⠼ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS UpdateQuestionAnswerResolver AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS DeleteQuestionAnswerResolver AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    QuestionAnswerDataSource     AWS::AppSync::DataSource Tue Feb 02 2021 14:56:49 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionAnswerDataSource     AWS::AppSync::DataSource Tue Feb 02 2021 14:56:49 GMT-0500 (Colombia Standard Time) Resource creation Initiated
⠦ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS ListOptionResolver   AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS GetOptionResolver    AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS CreateOptionResolver AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS DeleteOptionResolver AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS UpdateOptionResolver AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS ListOptionResolver   AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    OptionDataSource     AWS::AppSync::DataSource Tue Feb 02 2021 14:56:48 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS OptionDataSource     AWS::AppSync::DataSource Tue Feb 02 2021 14:56:48 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS OptionDataSource     AWS::AppSync::DataSource Tue Feb 02 2021 14:56:46 GMT-0500 (Colombia Standard Time)                            
⠹ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE QuestionIAMRole AWS::IAM::Role Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time) 
⠏ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE    GetQuestionaryConfigResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:56:53 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS GetQuestionaryConfigResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:56:53 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    DeleteQuestionaryConfigResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    CreateQuestionaryConfigResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS DeleteQuestionaryConfigResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS CreateQuestionaryConfigResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    ListQuestionaryConfigResolver   AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    UpdateQuestionaryConfigResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS ListQuestionaryConfigResolver   AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS UpdateQuestionaryConfigResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS GetQuestionaryConfigResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:56:50 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS DeleteQuestionaryConfigResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:49 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS CreateQuestionaryConfigResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:49 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS ListQuestionaryConfigResolver   AWS::AppSync::Resolver Tue Feb 02 2021 14:56:49 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS UpdateQuestionaryConfigResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:49 GMT-0500 (Colombia Standard Time)                            


CREATE_COMPLETE    CreateQuestionaryResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:54 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS CreateQuestionaryResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:54 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    DeleteQuestionaryResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:53 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS DeleteQuestionaryResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:53 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    GetQuestionaryResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:56:53 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    ListQuestionaryResolver   AWS::AppSync::Resolver Tue Feb 02 2021 14:56:53 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS GetQuestionaryResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:56:53 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS ListQuestionaryResolver   AWS::AppSync::Resolver Tue Feb 02 2021 14:56:53 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS UpdateQuestionaryResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS CreateQuestionaryResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS DeleteQuestionaryResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS ListQuestionaryResolver   AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS GetQuestionaryResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
⠋ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE    ListQuestionAnswerResolver   AWS::AppSync::Resolver Tue Feb 02 2021 14:56:54 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS ListQuestionAnswerResolver   AWS::AppSync::Resolver Tue Feb 02 2021 14:56:54 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    UpdateQuestionAnswerResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:54 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    CreateQuestionAnswerResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:54 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    GetQuestionAnswerResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:56:54 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS UpdateQuestionAnswerResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:54 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS CreateQuestionAnswerResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:54 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS GetQuestionAnswerResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:56:54 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS ListQuestionAnswerResolver   AWS::AppSync::Resolver Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS CreateQuestionAnswerResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS GetQuestionAnswerResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time)                            
⠹ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE    UpdateInteractionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:54 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS UpdateInteractionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:54 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    DeleteInteractionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:53 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS DeleteInteractionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    GetInteractionResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    CreateInteractionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time)                            
⠏ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS CreateQuestionResolver AWS::AppSync::Resolver   Tue Feb 02 2021 14:56:58 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    QuestionDataSource     AWS::AppSync::DataSource Tue Feb 02 2021 14:56:56 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionDataSource     AWS::AppSync::DataSource Tue Feb 02 2021 14:56:56 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionDataSource     AWS::AppSync::DataSource Tue Feb 02 2021 14:56:54 GMT-0500 (Colombia Standard Time)                            
⠧ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE    UpdateOptionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:55 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS UpdateOptionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:55 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    CreateOptionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:53 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS CreateOptionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:53 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    GetOptionResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:56:53 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS GetOptionResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:56:53 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    DeleteOptionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:53 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS DeleteOptionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:53 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    ListOptionResolver   AWS::AppSync::Resolver Tue Feb 02 2021 14:56:53 GMT-0500 (Colombia Standard Time)                            
⠇ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE    UpdateQuestionaryResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:55 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS UpdateQuestionaryResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:54 GMT-0500 (Colombia Standard Time) Resource creation Initiated
⠹ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE    QuestionaryInteractionTable          AWS::DynamoDB::Table   Tue Feb 02 2021 14:56:59 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    ListQuestionaryInteractionResolver   AWS::AppSync::Resolver Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS ListQuestionaryInteractionResolver   AWS::AppSync::Resolver Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    DeleteQuestionaryInteractionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:52 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS DeleteQuestionaryInteractionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    CreateQuestionaryInteractionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS CreateQuestionaryInteractionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    GetQuestionaryInteractionResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    UpdateQuestionaryInteractionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS GetQuestionaryInteractionResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS UpdateQuestionaryInteractionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:51 GMT-0500 (Colombia Standard Time) Resource creation Initiated
⠦ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE QuestionaryConfigTable AWS::DynamoDB::Table Tue Feb 02 2021 14:56:59 GMT-0500 (Colombia Standard Time) 
⠦ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE    UpdateQuestionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:57:02 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS UpdateQuestionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:57:02 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    ListQuestionResolver   AWS::AppSync::Resolver Tue Feb 02 2021 14:57:02 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS ListQuestionResolver   AWS::AppSync::Resolver Tue Feb 02 2021 14:57:01 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    DeleteQuestionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:57:01 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS DeleteQuestionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:57:01 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    GetQuestionResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:57:01 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS GetQuestionResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:57:01 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    CreateQuestionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:57:00 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS CreateQuestionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:57:00 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS UpdateQuestionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:59 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS GetQuestionResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:56:59 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS ListQuestionResolver   AWS::AppSync::Resolver Tue Feb 02 2021 14:56:59 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS DeleteQuestionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:56:59 GMT-0500 (Colombia Standard Time)                            
⠇ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE QuestionAnswerTable AWS::DynamoDB::Table Tue Feb 02 2021 14:57:01 GMT-0500 (Colombia Standard Time) 


CREATE_COMPLETE amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazinglead-QuestionaryInteraction-1DEOHS1HXIU7T AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:03 GMT-0500 (Colombia Standard Time) 
⠦ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazingleadsrois-QuestionaryConfig-1G5KNTRDJ6RMR AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:03 GMT-0500 (Colombia Standard Time) 
⠧ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE QuestionaryTable AWS::DynamoDB::Table Tue Feb 02 2021 14:57:01 GMT-0500 (Colombia Standard Time) 
⠼ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazingleadsroisen-18H-Interaction-FTNFAIAC1IFC AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:04 GMT-0500 (Colombia Standard Time) 
CREATE_COMPLETE InteractionTable                                                                                    AWS::DynamoDB::Table       Tue Feb 02 2021 14:57:00 GMT-0500 (Colombia Standard Time) 
⠦ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazingleadsroisen-18HTK7XG-Option-1ARBQAOBJIFGE AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:04 GMT-0500 (Colombia Standard Time) 
CREATE_COMPLETE OptionTable                                                                                          AWS::DynamoDB::Table       Tue Feb 02 2021 14:57:00 GMT-0500 (Colombia Standard Time) 
⠏ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE    DeleteQuestionAnswerResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:57:05 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS DeleteQuestionAnswerResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:57:05 GMT-0500 (Colombia Standard Time) Resource creation Initiated
⠦ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE Questionary            AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:10 GMT-0500 (Colombia Standard Time) 
CREATE_COMPLETE QuestionaryInteraction AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:09 GMT-0500 (Colombia Standard Time) 
CREATE_COMPLETE Option                 AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:09 GMT-0500 (Colombia Standard Time) 
CREATE_COMPLETE QuestionAnswer         AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:09 GMT-0500 (Colombia Standard Time) 
CREATE_COMPLETE QuestionaryConfig      AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:09 GMT-0500 (Colombia Standard Time) 
CREATE_COMPLETE Interaction            AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:09 GMT-0500 (Colombia Standard Time) 
⠴ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazingleadsroisen-18HTK7-Question-KWCBQOURBAM8 AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:11 GMT-0500 (Colombia Standard Time) 
CREATE_COMPLETE QuestionTable                                                                                       AWS::DynamoDB::Table       Tue Feb 02 2021 14:57:08 GMT-0500 (Colombia Standard Time) 
⠹ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS ConnectionStack AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:21 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS ConnectionStack AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:20 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    Question        AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:18 GMT-0500 (Colombia Standard Time)                            
⠹ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazingleadsroisen-ConnectionStack-CCN23T7ZLHIK AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:21 GMT-0500 (Colombia Standard Time) User Initiated
⠸ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE    QuestionAnswerquestionaryInteractionResolver  AWS::AppSync::Resolver Tue Feb 02 2021 14:57:32 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionAnswerquestionaryInteractionResolver  AWS::AppSync::Resolver Tue Feb 02 2021 14:57:32 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    OptionquestionResolver                        AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    QuestionaryquestionaryInteractionsResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionaryquestionaryInteractionsResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS OptionquestionResolver                        AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    InteractionquestionaryInteractionResolver     AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    QuestionAnsweroptionResolver                  AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    QuestionaryquestionsResolver                  AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS InteractionquestionaryInteractionResolver     AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionAnsweroptionResolver                  AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    QuestionquestionAnswersResolver               AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionquestionAnswersResolver               AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionaryquestionsResolver                  AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    QuestionaryInteractionquestionaryResolver     AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    QuestioninteractionsResolver                  AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    QuestionaryInteractioninteractionsResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    QuestionaryInteractionquestionAnswersResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time)                            
CREATE_COMPLETE    QuestionoptionsResolver                       AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestioninteractionsResolver                  AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionaryInteractioninteractionsResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS QuestionaryInteractionquestionaryResolver     AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    InteractionquestionResolver                   AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionaryInteractionquestionAnswersResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    QuestionquestionaryResolver                   AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionoptionsResolver                       AWS::AppSync::Resolver Tue Feb 02 2021 14:57:31 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_COMPLETE    OptionquestionAnswersResolver                 AWS::AppSync::Resolver Tue Feb 02 2021 14:57:30 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionquestionaryResolver                   AWS::AppSync::Resolver Tue Feb 02 2021 14:57:30 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS InteractionquestionResolver                   AWS::AppSync::Resolver Tue Feb 02 2021 14:57:30 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS OptionquestionAnswersResolver                 AWS::AppSync::Resolver Tue Feb 02 2021 14:57:30 GMT-0500 (Colombia Standard Time) Resource creation Initiated
CREATE_IN_PROGRESS OptionquestionResolver                        AWS::AppSync::Resolver Tue Feb 02 2021 14:57:29 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS InteractionquestionaryInteractionResolver     AWS::AppSync::Resolver Tue Feb 02 2021 14:57:29 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionaryInteractionquestionaryResolver     AWS::AppSync::Resolver Tue Feb 02 2021 14:57:29 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionoptionsResolver                       AWS::AppSync::Resolver Tue Feb 02 2021 14:57:29 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionaryquestionsResolver                  AWS::AppSync::Resolver Tue Feb 02 2021 14:57:29 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionAnsweroptionResolver                  AWS::AppSync::Resolver Tue Feb 02 2021 14:57:29 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionaryInteractionquestionAnswersResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:57:29 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionquestionAnswersResolver               AWS::AppSync::Resolver Tue Feb 02 2021 14:57:29 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionAnswerquestionResolver                AWS::AppSync::Resolver Tue Feb 02 2021 14:57:29 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionaryInteractioninteractionsResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:57:29 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionAnswerquestionaryInteractionResolver  AWS::AppSync::Resolver Tue Feb 02 2021 14:57:29 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionaryquestionaryInteractionsResolver    AWS::AppSync::Resolver Tue Feb 02 2021 14:57:28 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestioninteractionsResolver                  AWS::AppSync::Resolver Tue Feb 02 2021 14:57:28 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS OptionquestionAnswersResolver                 AWS::AppSync::Resolver Tue Feb 02 2021 14:57:28 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionquestionaryResolver                   AWS::AppSync::Resolver Tue Feb 02 2021 14:57:28 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS InteractionquestionResolver                   AWS::AppSync::Resolver Tue Feb 02 2021 14:57:28 GMT-0500 (Colombia Standard Time)                            
⠦ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE    QuestionAnswerquestionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:57:32 GMT-0500 (Colombia Standard Time)                            
CREATE_IN_PROGRESS QuestionAnswerquestionResolver AWS::AppSync::Resolver Tue Feb 02 2021 14:57:32 GMT-0500 (Colombia Standard Time) Resource creation Initiated
⠏ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazingleadsroisen-ConnectionStack-CCN23T7ZLHIK AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:34 GMT-0500 (Colombia Standard Time) 
⠸ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS CustomResourcesjson AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:45 GMT-0500 (Colombia Standard Time) 
CREATE_COMPLETE    ConnectionStack     AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:43 GMT-0500 (Colombia Standard Time) 
⠼ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS CustomResourcesjson AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:46 GMT-0500 (Colombia Standard Time) Resource creation Initiated
⠏ Updating resources in the cloud. This may take a few minutes...

CREATE_IN_PROGRESS amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazingleadsro-CustomResourcesjson-1IMV42FP11MG6 AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:46 GMT-0500 (Colombia Standard Time) User Initiated
⠦ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazingleadsro-CustomResourcesjson-1IMV42FP11MG6 AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:50 GMT-0500 (Colombia Standard Time) 
⠸ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE CustomResourcesjson AWS::CloudFormation::Stack Tue Feb 02 2021 14:57:57 GMT-0500 (Colombia Standard Time) 
⠙ Updating resources in the cloud. This may take a few minutes...

CREATE_COMPLETE amplify-suamazingleadsroisen-sualroiapi-102321-apisuamazingleadsroisen-18HTK7XGWKE5P AWS::CloudFormation::Stack Tue Feb 02 2021 14:58:01 GMT-0500 (Colombia Standard Time) 
⠦ Updating resources in the cloud. This may take a few minutes...

UPDATE_COMPLETE                     amplify-suamazingleadsroisen-sualroiapi-102321 AWS::CloudFormation::Stack Tue Feb 02 2021 14:58:10 GMT-0500 (Colombia Standard Time) 
UPDATE_COMPLETE_CLEANUP_IN_PROGRESS amplify-suamazingleadsroisen-sualroiapi-102321 AWS::CloudFormation::Stack Tue Feb 02 2021 14:58:09 GMT-0500 (Colombia Standard Time) 
CREATE_COMPLETE                     apisuamazingleadsroisen                        AWS::CloudFormation::Stack Tue Feb 02 2021 14:58:07 GMT-0500 (Colombia Standard Time) 
✔ Generated GraphQL operations successfully and saved at src/graphql
✔ All resources are updated in the cloud

GraphQL endpoint: https://7vwgjop7w5c23gvex3w4eeof7a.appsync-api.us-east-1.amazonaws.com/graphql
GraphQL API KEY: da2-u2wi3kujrjdfrcju7yvdnmwum4

```

# Questionary Config
```json
{
  "id": "1",
  "isCreateInteractionQuestionary": false,
  "isCreateInteractionQuestionaryButton": false,
  "isShowReactCursorPositionLabel": false,
  "layout": "none"
}
```

# Questionary

```json
{
  "id": "1",
  "isEnable": true,
  "name": "Amazing Leads"
}
```
1.  Complete la siguiente encuesta y maravíllese con Amazing Leads.
Iniciar
2. ¿Desde qué dispositivo estás respondiendo esta encuesta?
Celular
Computador
3. ¿Esta interesado en aumentar las ventas de su empresa?
Si
No
4. ¿Actualmente su empresa invierte en marketing digital?
Si
No
5. ¿Utiliza o ha utilizado procesos de inteligenica Artificial en su empresa?
Si
No
6. ¿Ve en Amazing Leads una manera eficaz de mejorar la calidad de sis leads?
Si
No
7.  Ingresa tus datos
Nombre y Apellido
Edad
Correo
Teléfono


# Questions/Options
```json
// Question 1
{
  "id": "1",
  "isEnable": true,
  "orderNumber": 1,
  "question": "¿Desde qué dispositivo estás respondiendo esta encuesta?",
  "questionaryID": "1"
}
// Question 1 Option 1
{
  "id": "1",
  "orderNumber": 1,
  "questionID": "1",
  "title": "CELULAR"
}
// Question 1 Option 2
{
  "id": "2",
  "orderNumber": 2,
  "questionID": "1",
  "title": "COMPUTADOR"
}
// #########################
// Question 2
{
  "id": "2",
  "isEnable": true,
  "orderNumber": 2,
  "question": "¿Esta interesado en aumentar las ventas de su empresa?",
  "questionaryID": "1"
}
// Question 2 Option 1
{
  "id": "3",
  "orderNumber": 1,
  "questionID": "2",
  "title": "SI"
}
// Question 2 Option 2
{
  "id": "4",
  "orderNumber": 2,
  "questionID": "2",
  "title": "NO"
}

// #########################
// Question 3
{
  "id": "3",
  "isEnable": true,
  "orderNumber": 3,
  "question": "¿Actualmente su empresa invierte en marketing digital?",
  "questionaryID": "1"
}

// Question 3 Option 1
{
  "id": "5",
  "orderNumber": 1,
  "questionID": "3",
  "title": "SI"
}
// Question 3 Option 2
{
  "id": "6",
  "orderNumber": 2,
  "questionID": "3",
  "title": "NO"
}


// #########################
// Question 4
{
  "id": "4",
  "isEnable": true,
  "orderNumber": 4,
  "question": "¿Utiliza o ha utilizado procesos de inteligenica Artificial en su empresa?",
  "questionaryID": "1"
}

// Question 4 Option 1
{
  "id": "7",
  "orderNumber": 1,
  "questionID": "4",
  "title": "SI"
}
// Question 4 Option 2
{
  "id": "8",
  "orderNumber": 2,
  "questionID": "4",
  "title": "NO"
}

// #########################
// Question 5
{
  "id": "5",
  "isEnable": true,
  "orderNumber": 5,
  "question": "¿Ve en Amazing Leads una manera eficaz de mejorar la calidad de sis leads?",
  "questionaryID": "1"
}

// Question 5 Option 1
{
  "id": "9",
  "orderNumber": 1,
  "questionID": "5",
  "title": "SI"
}
// Question 5 Option 2
{
  "id": "10",
  "orderNumber": 2,
  "questionID": "5",
  "title": "NO"
}
```


# Amplify auth

```sh
amplify add auth

Using service: Cognito, provided by: awscloudformation
 
 The current configured provider is Amazon Cognito. 
 
 Do you want to use the default authentication and security configuration? Default confi
guration
 Warning: you will not be able to edit these selections. 
 How do you want users to be able to sign in? Username
 Do you want to configure advanced settings? No, I am done.
Successfully added resource suamazingleadsroisend8665328 locally

Some next steps:
"amplify push" will build all your local backend resources and provision it in the cloud
"amplify publish" will build all your local backend and frontend resources (if you have hosting category added) and provision it in the cloud
```