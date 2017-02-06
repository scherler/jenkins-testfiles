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
   stage("one Misisipi") {
     if (params.ShouldBuild) { print "We are going to build now the branch " + params.Branch }
     else { print "Not building anything nor branch "+ params.Branch }
   }
   stage("two"){
        def branchInput = input id: 'CustomIdHere', message: 'this is a message to user', ok: 'Go ahead', parameters: [
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
]
        echo "BRANCH INPUT: ${branchInput}"
    }
}
