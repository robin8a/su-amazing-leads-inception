
{"query":"mutation CreateInteraction($input: CreateInteractionInput!, $condition: ModelInteractionConditionInput) {\n  createInteraction(input: $input, condition: $condition) {\n    id\n    type\n    element\n    epoch\n    isMouseDetected\n    isTouchDetected\n    height\n    width\n    isActive\n    isActiveClick\n    isActiveTouch\n    isPositionOutside\n    x\n    y\n    questionID\n    question {\n      id\n      question\n      question_start_time\n      question_end_time\n      questionaryID\n      questionary {\n        id\n        clientID\n        utm\n        ip\n        browser\n        questionaryStartTime\n        questionaryEndTime\n        isBrowser\n        isMobile\n        state_0\n        state_1\n        state_2\n      }\n      options {\n        nextToken\n      }\n      interactions {\n        nextToken\n      }\n    }\n  }\n}\n","variables":{"input":{"type":"position","element":"questionary","epoch":1605824024585,"isMouseDetected":true,"isTouchDetected":false,"height":461.5625,"width":0,"isActive":true,"isPositionOutside":false,"x":503,"y":407,"questionID":"5426d528-95e8-41a6-b2ec-6fc84fa23c85"}}}


{"query":"query ListInteractions($filter: ModelInteractionFilterInput, $limit: Int, $nextToken: String) {\n  listInteractions(filter: $filter, limit: $limit, nextToken: $nextToken) {\n    items {\n      id\n      type\n      element\n      epoch\n      isMouseDetected\n      isTouchDetected\n      height\n      width\n      isActive\n      isActiveClick\n      isActiveTouch\n      isPositionOutside\n      x\n      y\n      questionID\n      question {\n        id\n        question\n        question_start_time\n        question_end_time\n        questionaryID\n      }\n    }\n    nextToken\n  }\n}\n","variables":{}}



{query: "query ListQuestionaryConfigs($filter: ModelQuestionaryConfigFilterInput, $limit: Int, $nextToken: String) {↵  listQuestionaryConfigs(filter: $filter, limit: $limit, nextToken: $nextToken) {↵    items {↵      id↵      isShowReactCursorPositionLabel↵      isCreateInteractionQuestionary↵      isCreateInteractionQuestionaryButton↵      layout↵    }↵    nextToken↵  }↵}↵"

{query: "query
listInteractions {
    items {
      countOutside
      distance
      distance_left_button_point
      distance_questionary_point
    }
  }"
}


{"query":"query ListInteractions($filter: ModelInteractionFilterInput, $limit: Int, $nextToken: String) {\n  listInteractions(filter: $filter, limit: $limit, nextToken: $nextToken) {\n    items {\n      id\n      groupInteractionId\n      type\n      element\n      epoch\n      isMouseDetected\n      isTouchDetected\n      height\n      width\n      isActive\n      isActiveClick\n      isActiveTouch\n      isPositionOutside\n      x\n      y\n      distance\n      speed\n      speedAverage\n      sumTimeMiliseconds\n      dt\n      sumDistance\n      countOutside\n      distance_questionary_point\n      distance_left_button_point\n      distance_right_button_point\n      sumTimeMilisecondsBeforeNextQuestion\n      questionID\n      question {\n        id\n        question\n        question_start_time\n        question_end_time\n        questionaryID\n      }\n    }\n    nextToken\n  }\n}\n","variables":{"authMode":"API_KEY"}}

