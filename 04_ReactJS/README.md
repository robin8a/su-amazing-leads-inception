# kio-sl-lms-inception

# Starting React App
```sh
source ~/.bash_profile
npx create-react-app su-amazing-leads
```
# Amplify
```sh
amplify configure

```
## Init

```sh
amplify init
? Enter a name for the project su-amazing-leads
? Enter a name for the environment suamaleapi
? Choose your default editor: Visual Studio Code
? Choose the type of app that you're building javascript
Please tell us about your project
? What javascript framework are you using react
? Source Directory Path:  src
? Distribution Directory Path: build
? Build Command:  npm run-script build
? Start Command: npm run-script start
Using default provider  awscloudformation
```

## Install Amplify libraries


# Bootstrap
https://create-react-app.dev/docs/adding-bootstrap/
https://react-bootstrap.github.io/getting-started/introduction/


# git

```sh
ssh-keygen
/Users/robin8a/.ssh/su_amazing_leads_inception_rsa

cat ~/.ssh/su_amazing_leads_inception_rsa.pub

```


```sh
cd ~/.ssh
ls
nano config

# Add

# CodeCommit hosts
Host su_amazing_leads_inception_rsa
   HostName git-codecommit.us-east-1.amazonaws.com
   User APKASWPUM4U3QFO7WQG2
   IdentityFile ~/.ssh/su_amazing_leads_inception_rsa

```

```sh
# git remote add origin ssh://git-codecommit.us-east-1.amazonaws.com/v1/repos/su-amazing-leads

# git remote rm origin

git remote add origin ssh://su_amazing_leads_inception_rsa/v1/repos/su-amazing-leads

git push --set-upstream origin master



```

# Amplify
- https://docs.amplify.aws/cli/start/install#option-2-follow-the-instructions
- [Getting started Auth with style](https://github.com/aws-amplify/amplify-js/tree/e56aba642acc7eb3482f0e69454a530409d1b3ac)

```sh
amplify init
Note: It is recommended to run this command from the root of your app directory
? Enter a name for the project kio-sl-lms
? Enter a name for the environment kiosllms
? Choose your default editor: Visual Studio Code
? Choose the type of app that you're building javascript
Please tell us about your project
? What javascript framework are you using react
? Source Directory Path:  src
? Distribution Directory Path: build
? Build Command:  npm run-script build
? Start Command: npm run-script start
amplify publish

```

```sh
amplify add hosting

kio-sl-lms robin8a$ amplify add hosting
? Select the plugin module to execute Amazon CloudFront and S3
? Select the environment setup: DEV (S3 only with HTTP)
? hosting bucket name kio-sl-lms-20200907192030-hostingbucket
? index doc for the website index.html
? error doc for the website index.html
```

```sh
amplify publish
http://kio-sl-lms-20200907192030-hostingbucket-kiosllmsev.s3-website-us-east-1.amazonaws.com


```

# React Drag & Drop
https://www.youtube.com/watch?v=-MfTv5VRM0A
https://github.com/atlassian/react-beautiful-dnd
https://github.com/react-dnd/react-dnd
https://www.smashingmagazine.com/2020/02/html-drag-drop-api-react/



 
