// pipeline{
//     agent any
//     stages{
//         stage('build'){
//             steps{
//                 script{
//                 sh 'pip install flask'
//                 }
//             }
//         }
//         stage('test'){
//             steps{
//                 script{
//                 sh 'pytest test_file.py'
//                 }
//             }
//         }
//     }
// }

// pipeline {
//     agent any
//     environment {
//         WORKSPACE = "/workspace"
//     }
//     stages {
//         stage('build') {
//             steps {
//                 dir("${WORKSPACE}") {
//                     sh 'pip install flask'
//                 }
//             }
//         }
//         stage('test') {
//             steps {
//                 dir("${WORKSPACE}") {
//                     sh 'pytest test_file.py'
//                 }
//             }
//         }
//     }
// }


pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'pip install flask'
            }
        }
        stage('test') {
            steps {
                // Use 'start /B' to run the command in the background on Windows
                sh 'start /B pytest test_file.py'
            }
        }
    }
}
