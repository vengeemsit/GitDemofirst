pipeline {
  agent any
  stages {
    stage('DEV Unit Test') {
      parallel {
        stage('DEV Unit Test') {
          steps {
            bat 'mvn -v'
          }
        }
        stage('Code Analysis') {
          steps {
            sh 'mvn --version'
          }
        }
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