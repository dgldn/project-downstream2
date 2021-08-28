pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                timeout(time:3, unit:'SECONDS') {
                    sh '''
                    echo hello
                    sleep 60
                    echo done
                    '''
                }
            }
        }
    }
}
