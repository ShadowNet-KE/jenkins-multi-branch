timeout(unit: 'SECONDS', time: 50) {
    stage("One"){
        node("dind-1.0.0") {
            sleep 5
            echo 'Hello'
        }
    }
    stage("Two"){
        node("jenkins-agent") {
            sleep 5
            echo 'Hello'
        }
    }
}
