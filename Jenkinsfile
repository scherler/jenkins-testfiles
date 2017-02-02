node() {
   // adds job parameters within jenkinsfile
   properties([
     parameters([
       booleanParam(
         defaultValue: false,
         description: 'Should we start the build?',
         name: 'ShouldBuild'
       ),
       choice(
           choices: 'master\ndevelopment\nfeatureXYZ\nhotfix69\nrevolution\nrefactor\nuglify',
           description: 'Which branch do you want to build?',
           name: 'Branch'),
       text(defaultValue: 'default', description: 'Long text goes here', name: 'This is a multi line string'),
       string(defaultValue: 'yeah', description: 'string parameter desc', name: 'this is a string parmeter'),
       choice(
           choices: 'master\ndevelopment\nuglify',
           description: 'Which next branch do you want you to build?',
           name: 'NextBranch'),
     ])
   ])
   stage("one") {
     if (params.ShouldBuild) { print "We are going to build now the branch " + params.Branch }
     else { print "Not building anything nor branch "+ params.Branch }
   }
   stage("two"){
        def branchInput = input id: 'CustomIdHere', message: 'this is a message to user', ok: 'Go ahead', parameters: [
                booleanParam(defaultValue: true, description: 'yes or no', name: 'thisIsBool'),
                choice(choices: 'radio1\nradio2\nradio3\nradio4', description: 'this is choice Radio description', name: 'This is choice Radio'),
choice(choices: 'drop1\ndrop2\ndrop3\ndrop4\ndrop5\ndrop6\ndrop7', description: 'this is choice Dropdown description', name: 'This is choice dropdown'),
                text(defaultValue: 'default', description: 'Long text goes here', name: 'This is a multi line string'),
                string(defaultValue: 'yeah', description: 'string parameter desc', name: 'this is a string parmeter'),
                password(defaultValue: 'secret', description: 'password param desc', name: 'password param')
            ]
        echo "BRANCH INPUT: ${branchInput}"
    }
}
