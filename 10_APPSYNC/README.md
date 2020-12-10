# Queries
```js
query MyQuery {
  getQuestionary(id: "1") {
    questions {
      items {
        id
        question
        options {
          items {
            id
            title
          }
        }
      }
    }
  }
}


query MyQuery {
  listQuestionarys {
    items {
      id
      name
      questions {
        items {
          id
          question
        }
      }
    }
  }
}


query MyQuery {
  getQuestionaryInteraction(id: "be111a9c-9b07-4da4-9051-aea73b12c45f") {
    interactions {
      items {
        countOutside
        distance
        distance_left_button_point
        distance_questionary_point
        dt
        distance_right_button_point
        element
        epoch
        groupInteractionId
        height
        id
        isActive
        isActiveClick
        isActiveTouch
        isMouseDetected
        isPositionOutside
        isTouchDetected
        questionaryInteractionID
        speed
        speedAverage
        sumDistance
        sumTimeMiliseconds
        sumTimeMilisecondsBeforeNextQuestion
        type
        width
        x
        y
      }
    }
  }
}
```


# AWS

```sh

nano ~/.aws/credentials
export AWS_PROFILE=su-amazing-leads-profile

```