stage "Checkout"
node('docker') {
    sh "echo never going to give you up"
}


stage "Build"
node {
    sh "echo never going to let you down"
}

stage "Test"
parallel (
    "Firefox" : { echo "Never run around" },
    "Edge" : { echo "Never desert you" }
)    
    
stage "Staging" 
echo "Make you cry (never)"

stage "Production"
echo "Tell a lie and hurt you (never)"

 
