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
                echo 'Deploying....'
            }
        }
    }
}

