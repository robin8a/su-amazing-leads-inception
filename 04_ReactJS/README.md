# kio-sl-lms-inception

# Starting React App
```sh
source ~/.bash_profile
npx create-react-app su-amazing-leads
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
# git remote -v
# git remote rm origin

git remote add origin ssh://su_amazing_leads_inception_rsa/v1/repos/su-amazing-leads

git push --set-upstream origin master

```

# Amplify
- https://docs.amplify.aws/cli/start/install#option-2-follow-the-instructions
- [Getting started Auth with style](https://github.com/aws-amplify/amplify-js/tree/e56aba642acc7eb3482f0e69454a530409d1b3ac)

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

```sh
amplify add hosting

kio-sl-lms robin8a$ amplify add hosting
? Select the plugin module to execute Amazon CloudFront and S3
? Select the environment setup: DEV (S3 only with HTTP)
? hosting bucket name kio-sl-lms-20200907192030-hostingbucket
? index doc for the website index.html
? error doc for the website index.html


https://master.ds3q4dungfi7s.amplifyapp.com

```

```sh
amplify publish

```


# Navegation

```sh
yarn add react-router-dom

```

# Cloud 9 config

https://github.com/dowjones/react-tutorial/blob/master/AWS.Cloud9.Instructions.md


# To Do
- Agregar relacion QuestionaryInteraction to Answer (OK)
- Guardar respuesta (OK)
- utm Table enrichment ()
- al finalizar el nuevo schema actualizar questionary
- Auth => Admin
- UI QuestionaryConfig
- UI Questionary
- UI Option
- utm query
- Actualizar lead con archivo .csv



# Historios de usuario
- http://www.projectadmin.org/guia-aplicada-de-historias-de-usuarios-en-scrum-agil-practicas-recomendadas-de-historia-de-usuario-yodiz-project-management-blog/


# Ordering object array
- https://flaviocopes.com/how-to-sort-array-of-objects-by-property-javascript/

# Is it possible to customize default Sign Up, Sign In screens of aws-amplify-react-native package?
- https://aws-amplify.github.io/amplify-js/api/classes/authenticatorcomponentcore.html
- https://blog.kylegalbraith.com/2018/11/29/how-to-easily-customize-the-aws-amplify-authentication-ui/
- https://medium.com/@coryschimmoeller/customizing-the-authentication-experience-of-amplifys-withauthenticator-e6f2089ff469
- https://stackoverflow.com/questions/50859539/is-it-possible-to-customize-default-sign-up-sign-in-screens-of-aws-amplify-reac
- https://docs.amplify.aws/lib/auth/customui/q/platform/js#customize-ui-theme
- https://medium.com/@jordan.eckowitz/aws-amplify-custom-authentication-3876fb3f6712
- https://pandeysoni.medium.com/how-to-setup-customize-amplify-authentication-ui-using-hooks-36442f5fdc


# Create Question with options
- https://docs.amplify.aws/cli/graphql-transformer/overview#test-the-api
- https://geekyants.com/blog/many-to-many-relations-in-aws-amplify-using-react-321


```js
createQuestion(input: $input, condition: $condition) {
      id
      question
      questionaryID
      isEnable
      orderNumber
      questionary {
        id
        name
        isEnable
        questions {
          nextToken
        }
        questionaryInteractions {
          nextToken
        }
      }
      options {
        items {
          id
          title
          orderNumber
          questionID
        }
        nextToken
      }
}

mutation MyMutation {
  createQuestion(input: 
    {
      id: "id-borrar", 
      isEnable: false, 
      orderNumber: 10, 
      question: "test", 
      questionaryID: "1",
    }) {
    id
    isEnable
    orderNumber
    question
    questionaryID
    options {
      items {
        id
        orderNumber
        title
      }
    }
  }
}

```