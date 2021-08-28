pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                timeout(time:3, unit:'SECONDS') {
                    retry(3) {     
                    sh '''
                    echo hello there
                    exit 1
                    '''
                    }
                }
            }
        }
    }
    post {
        always {
            echo "This will always run"
        }
        success {
            echo "Runs only when job was successful"
        }
        failure {
            echo "Runs only when job is failed"
        }
        unstable {
            echo "Runs only when pipeline is unstable"
        }
        changed {
            echo "Runs when state has changed"
        }
    }
}
