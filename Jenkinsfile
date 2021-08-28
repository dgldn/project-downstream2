pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                timeout(time:3, unit:'SECONDS') {
                    retry(3) {     
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
}
