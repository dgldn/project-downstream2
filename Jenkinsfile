pipeline {
    agent any
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages {
        stage('Example') {
            steps {
                echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
            }
        }
    }
}

// pipeline {
//     agent {
//         docker { image 'node:14-alpine' }
//     }
//     environment {
//         DISABLE_AUTH = 'true'
//         DB_ENGINE    = 'sqlite'
//     }

//     stages {
//         stage('Build') {
//             steps {
//                 echo 'Database engine is ${DB_ENGINE}'
//                 echo 'DISABLE_AUTH is ${DISABLE_AUTH}'
//                 sh 'printenv'
//             }
//         }
//     }
// }


// pipeline {
//     agent any
//     stages {
//         stage('build') {
//             steps {
//                 timeout(time:3, unit:'SECONDS') {
//                     retry(3) {     
//                     sh '''
//                     echo hello there
//                     exit 1
//                     '''
//                     }
//                 }
//             }
//         }
//     }
//     post {
//         always {
//             echo "This will always run"
//         }
//         success {
//             echo "Runs only when job was successful"
//         }
//         failure {
//             echo "Runs only when job is failed"
//         }
//         unstable {
//             echo "Runs only when pipeline is unstable"
//         }
//         changed {
//             echo "Runs when state has changed"
//         }
//     }
// }
