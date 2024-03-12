node {
    stage "hey"
    sh 'echo `date` Stage 1;sleep 1; echo a1; sleep 1;echo a2;sleep 1; echo a3;sleep 4'

    stage "parallel"

    parallel firstBranch: {
        sh 'echo `date` Stage 2 - firstBranch www.spiegel.de'
        sh 'ping -c 4 -i 3 www.spiegel.de || true'
        sh 'echo `date` Stage 2 mirror out;sleep 1; echo a1; sleep 1;echo a2;sleep 1; echo a3;sleep 4'

    }, secondBranch: {
        sh 'echo `date` Stage 2 - secondBranch www.stern.de'
        sh 'ping -c 6 -i 2 www.stern.de || true'
        sh 'echo `date` Stage 2 star out;sleep 1; echo a1; sleep 1;echo a2;sleep 1; echo a3;sleep 1'
    }

    stage "ho"
    sh 'echo done;sleep 1; echo a1; sleep 1;echo a2;sleep 1; echo a3;sleep 4'
}
