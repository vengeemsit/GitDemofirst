pipeline {
  agent any
  stages {
    stage('DEV Test') {
      steps {
        bat 'mvn -v'
      }
    }
    stage('SIT Test') {
      steps {
        sh 'docker -v'
      }
    }
  }
}