pipeline {
    agent {
        docker {
            image 'docker:24.0.7-cli'
            args '-v /var/run/docker.sock:/var/run/docker.sock --user root'
        }
    }
    stages {
        stage('Test Docker') {
            steps {
                sh 'docker --version'
            }
        }
        stage('Run Python Latest in Docker') {
            steps {
                // Pull the latest official Python image and run Python inside it
                sh '''
                    echo "Pulling latest Python image..."
                    docker pull python:latest

                    echo "Checking Python version inside container..."
                    docker run --rm python:latest python --version
                '''
            }
        }
    }
}

/*pipeline {
  agent any

  stages {
    stage('version') {
      steps {
        sh 'python3 --version'
        sh 'docker --version'
      }
    }*/    
    /*stage('docker') {
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
    }*/
    /*stage('hello') {
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
}*/