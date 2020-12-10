# Architecture
- ![Diagram](_images/architecture.png)
# Event areas interaction
- ![Areas Interaction KPIs](_images/questionary_areas.png)
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

### Query for ListInteractions
```json
{"query":"query ListInteractions($filter: ModelInteractionFilterInput, $limit: Int, $nextToken: String) {\n  listInteractions(filter: $filter, limit: $limit, nextToken: $nextToken) {\n    items {\n      id\n      groupInteractionId\n      type\n      element\n      epoch\n      isMouseDetected\n      isTouchDetected\n      height\n      width\n      isActive\n      isActiveClick\n      isActiveTouch\n      isPositionOutside\n      x\n      y\n      distance\n      speed\n      speedAverage\n      sumTimeMiliseconds\n      dt\n      sumDistance\n      countOutside\n      distance_questionary_point\n      distance_left_button_point\n      distance_right_button_point\n      sumTimeMilisecondsBeforeNextQuestion\n      questionID\n      question {\n        id\n        question\n        question_start_time\n        question_end_time\n        questionaryID\n      }\n    }\n    nextToken\n  }\n}\n","variables":{"authMode":"API_KEY"}}
```

## Using AWS AppSync Console


## Using CLI




# Testing