pipeline {
    agent any
    stages {
      stage('Build') {
        steps {
            build 'PES2UG21CS154-1'
            sh 'g++ main.cpp -o output'
          }
      }
      stage('Test') {
        steps {
            sh './out'
          }
      }
      stage('Deploy') {
        steps {
            echo 'deploy' 
        }
      }
    }
    post {
        failure {
            echo 'Pipeline failed'
            error 'Pipeline failed'
         }
    }
}
