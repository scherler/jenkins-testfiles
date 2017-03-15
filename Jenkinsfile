// You need to have https://github.com/scherler/blueocean-shared-library/commit/43d5620a42d7795b43bc829d694c3cae2a3c3919
@Library('test-writer') import writeTest
import longLog
node {
    stage 'fin'
    def xml = writeTest()
    sh "echo '$xml' > TEST-some.xml"
    step([$class: 'JUnitResultArchiver', testResults: 'TEST-*.xml'])
    sh 'echo `date` fin;sleep 3; echo `date` fin;'
    sh 'echo yeah > foo.txt'
    archiveArtifacts 'foo.txt'
    longLog(1000)
    stage 'NoSteps'
}
