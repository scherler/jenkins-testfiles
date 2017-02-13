node() {
   stage('hello') {
  Map feedback = input(submitterParameter: 'submitter', message: "tell me something", parameters: [
    [$class: 'TextParameterDefinition', name: 'text', description: "enter something"]
  ])

  echo "Text: ${feedback.text}"
  echo "Submitter: ${feedback.submitter}"
}
}
