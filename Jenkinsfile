node() {
   // adds job parameters within jenkinsfile
   properties([
     parameters([[$class: 'TextParameterDefinition', name: 'text', description: "enter something"]])
   ])
   stage("one") {
      echo "Text: ${params.text}"
   }
   stage("two"){
       Map feedback = input(submitterParameter: 'submitter', message: "tell me something", parameters: [
          [$class: 'TextParameterDefinition', name: 'text', description: "enter something"],
          choice(
           choices: 'master\ndevelopment\nfeatureXYZ\nhotfix69\nrevolution\nrefactor\nuglify',
           description: 'Which branch do you want to build?',
           name: 'Branch'),
       text(defaultValue: 'default', description: 'Long text goes here', name: 'This is a multi line string'),
       string(defaultValue: 'yeah', description: 'string parameter desc', name: 'this is a string parmeter')
        ])
      echo "Text: ${feedback.text}"
      echo "Submitter: ${feedback.submitter}"
    }
}
