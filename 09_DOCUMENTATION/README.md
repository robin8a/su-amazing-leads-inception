# Architecture
  ![Diagram](_images/architecture.png)

# Database ER-Model
  ![ER Model](_images/ER_Model.png)

# Event areas interaction
![Areas Interaction KPIs](_images/questionary_areas.png)
- Blue: questionary area
- Orange: left button
- Green: right button



# Relative Distances
![References Points](_images/reference_points.png)
Three distances are calculated:
1. Green: from pointer to center top Questionary
2. Blue: from pointer to right button
3. Pink: from pointer to left button

# KPI
## PC
Every time that the mouse is over an area is calculated:
- dx: (x2 - x1)
- dy: (y2 - y1)
- dt: (t2 - t1)
- distance: Math.sqrt(Math.pow(dx, 2) + Math.pow(dy, 2))
- speed: distance/dt dt != 0
- speedAverage: average per groupInteractionId
- sumTimeMiliseconds: sum time per groupInteractionId
- sumDistance: sum distance per groupInteractionId
- countOutside: count by in/out any area (blue, orange or green)
- distance_questionary_point
- distance_left_button_point 
- distance_right_button_point
- sumTimeMilisecondsBeforeNextQuestion: sum miliseconds before click next question

## Mobile
Every time that the mouse has a tap action is calculated:
- dx: (x2 - x1)
- dy: (y2 - y1)
- dt: (t2 - t1)
- distance: Math.sqrt(Math.pow(dx, 2) + Math.pow(dy, 2))
- speed: distance/dt dt != 0
- speedAverage: average per groupInteractionId
- sumTimeMiliseconds: sum time per groupInteractionId
- sumDistance: sum distance per groupInteractionId


# AppSync - GraphQL - API

## Using Postman
![Postman example](_images/postman_query_interactions.png)
- Link: https://rop52fode5aqfnb4cfyd2okbza.appsync-api.us-east-1.amazonaws.com/graphql
- api key: shared in email

### Query for ListInteractions
```json
{"query":"query ListInteractions($filter: ModelInteractionFilterInput, $limit: Int, $nextToken: String) {\n  listInteractions(filter: $filter, limit: $limit, nextToken: $nextToken) {\n    items {\n      id\n      groupInteractionId\n      type\n      element\n      epoch\n      isMouseDetected\n      isTouchDetected\n      height\n      width\n      isActive\n      isActiveClick\n      isActiveTouch\n      isPositionOutside\n      x\n      y\n      distance\n      speed\n      speedAverage\n      sumTimeMiliseconds\n      dt\n      sumDistance\n      countOutside\n      distance_questionary_point\n      distance_left_button_point\n      distance_right_button_point\n      sumTimeMilisecondsBeforeNextQuestion\n      questionID\n      question {\n        id\n        question\n        question_start_time\n        question_end_time\n        questionaryID\n      }\n    }\n    nextToken\n  }\n}\n","variables":{"authMode":"API_KEY"}}
```

## Using AWS AppSync Console

- [AWS Console link: ](https://shiftactive.signin.aws.amazon.com/console)
- User: su-amazing-leads
- Password: shared by email
- Services => AWS AppSync => APIs => suamleapi-suamaleapi => Queries
- [Queries examples](./../10_APPSYNC/README.md)

## Using CLI
- [Install and Configure CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)
- [How to configure new profiles](http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html)

### Add new profile
```sh
sudo aws configure --profile new_profile
```


### Using profiles
 - [cli Multiple Profiles](https://docs.aws.amazon.com/cli/latest/userguide/cli-multiple-profiles.html)
```sh
# Single commands
aws ec2 describe-instances --profile new_profile
# or for multiples commands
export AWS_PROFILE=new_profile
# Example
nano ~/.aws/credentials
export AWS_PROFILE=su-amazing-leads-profile
```

### Scan dynamodb Table
- Tab-separated values (.tsv)

# AWS CLI export

<video width="320" height="240" controls>
  <source src="./_videos/Export_and_Download_DataDump.mov" type="video/mp4">
</video>

## Question

1. Export
```sh
aws dynamodb scan \
    --table-name Question-mexfa73ymfc6rmlwqmt6vu4vf4-suamaleapi \
    --query "Items[*].[id.S, isEnable.BOOL, orderNumber.N, question.S, questionaryID.S]" \
    --output text > QuestionDataDump.tsv
```

2. Header for QuestionDataDump.tsv files
```tsv
id.S	isEnable.BOOL	orderNumber.N	question.S	questionaryID.S
```

## Option

1. Export
```sh
aws dynamodb scan \
    --table-name Option-mexfa73ymfc6rmlwqmt6vu4vf4-suamaleapi \
    --query "Items[*].[id.S, orderNumber.N, questionID.S, title.S]" \
    --output text > OptionDataDump.tsv
```

2. Header for OptionDataDump.tsv files
```tsv
id.S	orderNumber.N	questionID.S	title.S
```

## QuestionAnswer

1. Export
```sh
aws dynamodb scan \
    --table-name QuestionAnswer-mexfa73ymfc6rmlwqmt6vu4vf4-suamaleapi \
    --query "Items[*].[id.S, __typename.S, createdAt.S, optionID.S, questionID.S, questionaryInteractionID.S, updatedAt.S]" \
    --output text > QuestionAnswerDataDump.tsv
```


1. Header for QuestionAnswerDataDump.tsv files
```tsv
id.S	orderNumber.N	questionID.S	title.S
```

## QuestionaryInteraction

1. Export
```sh
aws dynamodb scan \
    --table-name QuestionaryInteraction-mexfa73ymfc6rmlwqmt6vu4vf4-suamaleapi \
    --query "Items[*].[id.S, __typename.S, browser.S, clientID.S, createdAt.S, ip.S, isBrowser.BOOL, isMobile.BOOL, questionaryEndTime.N, questionaryID.S, questionaryStartTime.N, state_0.N, state_1.N, state_2.N, updatedAt.S, utm.s]" \
    --output text > QuestionaryInteractionDataDump.tsv
```

2. Header for QuestionaryInteractionDataDump.tsv files
```tsv
id.S	__typename.S	browser.S	clientID.S	createdAt.S	ip.S	isBrowser.BOOL	isMobile.BOOL	questionaryEndTime.N	questionaryID.S	questionaryStartTime.N	state_0.N	state_1.N	state_2.N	updatedAt.S	utm.s
```

```sh
aws dynamodb scan \
    --table-name Interaction-mexfa73ymfc6rmlwqmt6vu4vf4-suamaleapi \
    --query "Items[*].[id.S, __typename.S, countOutside.N, createdAt.S, distance.N, distance_left_button_point.N, distance_questionary_point.N, distance_right_button_point.N, dt.N, element.S, epoch.N, height.N, isMouseDetected.BOOL, isPositionOutside.BOOL, isTouchDetected.BOOL, questionID.S, questionaryInteractionID.S, speed.N, speedAverage.N, sumDistance.N, sumTimeMiliseconds.N, sumTimeMilisecondsBeforeNextQuestion.N, type.S, updatedAt.S, width.N, x.N, y.N]" \
    --output text > InteractionsDataDump.tsv
```

## Interaction

1. Export
```sh
aws dynamodb scan \
    --table-name Interaction-mexfa73ymfc6rmlwqmt6vu4vf4-suamaleapi \
    --query "Items[*].[id.S, __typename.S, countOutside.N, createdAt.S, distance.N, distance_left_button_point.N, distance_questionary_point.N, distance_right_button_point.N, dt.N, element.S, epoch.N, height.N, isActive.BOOL, isMouseDetected.BOOL, isPositionOutside.BOOL, isTouchDetected.BOOL, questionID.S, questionaryInteractionID.S, speed.N, speedAverage.N, sumDistance.N, sumTimeMiliseconds.N, sumTimeMilisecondsBeforeNextQuestion.N, type.S, updatedAt.S, width.N, x.N, y.N]" \
    --output text > InteractionDataDump.tsv
```

2. Header for InteractionDataDump.tsv files
```tsv
id.S	__typename.S	countOutside.N	createdAt.S	distance.N	distance_left_button_point.N	distance_questionary_point.N	distance_right_button_point.N	dt.N	element.S	epoch.N	height.N	isActive.BOOL	isMouseDetected.BOOL	isPositionOutside.BOOL	isTouchDetected.BOOL	questionID.S	questionaryInteractionID.S	speed.N	speedAverage.N	sumDistance.N	sumTimeMiliseconds.N	sumTimeMilisecondsBeforeNextQuestion.N	type.S	updatedAt.S	width.N	x.N	y.N 
```


#### Filter
```sh
aws dynamodb scan \
    --table-name Interaction-mexfa73ymfc6rmlwqmt6vu4vf4-suamaleapi \
    --query "Items[*].[id.S, __typename.S, countOutside.N, createdAt.S, distance.N, distance_left_button_point.N, distance_questionary_point.N, distance_right_button_point.N, dt.N, element.S, epoch.N, height.N, isMouseDetected.BOOL, isPositionOutside.BOOL, isTouchDetected.BOOL, questionID.S, questionaryInteractionID.S, speed.N, speedAverage.N, sumDistance.N, sumTimeMiliseconds.N, sumTimeMilisecondsBeforeNextQuestion.N, type.S, updatedAt.S, width.N, x.N, y.N]" \
    --filter-expression 'questionaryInteractionID = :val' \
    --expression-attribute-values '{":val": {"S": "position"}}' \
    --output text > InteractionsDataDump.tsv
```
- Header for .tsv files
```tsv
  id.S	__typename.S	countOutside.N	createdAt.S	distance.N	distance_left_button_point.N	distance_questionary_point.N	distance_right_button_point.N	dt.N	element.S	epoch.N	height.N	isMouseDetected.BOOL	isPositionOutside.BOOL	isTouchDetected.BOOL	questionID.S	questionaryInteractionID.S	speed.N	speedAverage.N	sumDistance.N	sumTimeMiliseconds.N	sumTimeMilisecondsBeforeNextQuestion.N	type.S	updatedAt.S	width.N	x.N	y.N
```
- [InteractionsDataDump.tsv](../10_APPSYNC/InteractionsDataDump.tsv)  copy - paste (.xlsx or googlesheets)

### Cloud9 Result
![Data dump](./_images/cloud9_exports.png)

### Uploading exported files from Cloud9 to S3 bucket and Downloading 
```sh

aws s3 ls
# 2021-01-13 23:01:31 su-amazing-leads-exports


aws s3 cp InteractionsDataDump.tsv s3://su-amazing-leads-exports/
```

## Using Dynobase
- It use the aws configuration
- [Dynobase](https://dynobase.dev/)
- ![Example](_images/dynobase_example.png)


# Testing
- [Development Link](https://master.ds3q4dungfi7s.amplifyapp.com/)
