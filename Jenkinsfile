pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh '''
                echo "Hello Jenkins!"
                echo "running mulitple commands in a single shell step"
                ls -la
                pwd
                '''
            }
            steps {
                retry(3) {
                    sh 'echo hello'
                }
            }
        }
    }
}
