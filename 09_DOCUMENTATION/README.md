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


# Data Sample

- [drive: data_sample](https://docs.google.com/spreadsheets/d/1rhHTx-CdESuPudghoKZjgaKIQGzXxAZI43wDBm7OB7Q/edit?usp=sharing)

# AppSync - GraphQL - API


# Testing