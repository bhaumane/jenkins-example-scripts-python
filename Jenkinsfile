pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        sh 'python3 --version'
        sh 'docker --version'
      }
    }    
    stage('docker') {
      agent {
        docker {
          image 'python:latest'
          //args '-u root:root'
        }
      }
      steps {
                sh 'python --version'
                sh 'docker --version'
            }
    }
    stage('hello') {
      steps {
        sh 'python3 hello.py'
      }
    }
    stage('Build') {
      steps {
        echo 'New Building the project...'
      }
    }
    stage('Test') {
      steps {
        echo 'New Running tests...'
      }
    }
    
  }
}