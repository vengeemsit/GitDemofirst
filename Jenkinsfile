pipeline {
  agent any
  stages {
    stage('DEV Test') {
      steps {
        bat 'mvn -v'
      }
    }
    stage('SIT Test') {
      parallel {
        stage('SIT Test') {
          steps {
            sh 'docker -v'
          }
        }
        stage('SIT Sanity check') {
          steps {
            sh 'mvn -v'
          }
        }
      }
    }
    stage('UAT') {
      steps {
        echo 'success'
      }
    }
  }
}