// pipeline {
//     agent any
//     stages{
//         stage ("build") {
//             steps{
//                 echo "hi"
//             }
//         }
//         stage ("deploy") {
//             steps{
//                 echo "hello"
//             }
//         }
//     }
// }

pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        GREETING = 'Hello jenkins'
    }
    //build
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                sh """
                    echo "Here i wrote shell script"
                    env
                """
            }
        }
    }
    //post build
    post {
        always {
            echo 'I will always say HELLO again'
        }
        failure {
            echo 'This run when pipeline failed'
        }
        success {
            echo 'This ipeline is sucess'
        }
    }
}

