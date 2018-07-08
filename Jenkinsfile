pipeline {
    agent any
    stages {
        stage('Example') {
            input {
                message "Should we continue?"
                ok "Yes, we should."
              
            }
            steps {
                echo "Hello,"$BUILD_USER", nice to meet you."
            }
        }
    }
}
