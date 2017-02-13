node() {
   // adds job parameters within jenkinsfile
   properties([
     parameters([[$class: 'TextParameterDefinition', name: 'text', description: "enter something"]])
   ])
   stage("one") {
      echo "Text: ${feedback.text}"
      echo "Submitter: ${feedback.submitter}"
   }
   stage("two"){
 
       Map feedback = input(submitterParameter: 'submitter', message: "tell me something", parameters: [
          [$class: 'TextParameterDefinition', name: 'text', description: "enter something"]
        ])
      echo "Text: ${feedback.text}"
      echo "Submitter: ${feedback.submitter}"
    }
}
