node() {
    // adds job parameters within jenkinsfile
   properties([
     parameters([
       booleanParam(
         defaultValue: false,
         description: 'isFoo should be false',
         name: 'isFoo'
       ),
       booleanParam(
         defaultValue: true,
         description: 'isBar should be true',
         name: 'isBar'
       ),
     ])
   ])
   stage('hello') {
      input message: 'sd', parameters: [
         [$class: 'CredentialsParameterDefinition', credentialType: 'com.cloudbees.plugins.credentials.common.StandardCredentials', defaultValue: '', description: '', name: 'credentials', required: false],
         choice(
           choices: 'master\ndevelopment\nfeatureXYZ\nhotfix69\nrevolution\nrefactor\nuglify',
           description: 'Which branch do you want to build?',
           name: 'Branch'),
       text(defaultValue: 'default', description: 'Long text goes here', name: 'This is a multi line string'),
       string(defaultValue: 'yeah', description: 'string parameter desc', name: 'this is a string parmeter')
      ]

}
}
