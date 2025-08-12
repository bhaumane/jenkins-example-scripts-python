pipeline {
    agent any

    environment {
        APP_ENV = 'staging'
        REPORT_DIR = 'reports'
    }

    stages {
      stage('build') {
        steps {
            echo '==========BUILD STAGE=========='
        }
      }
      stage('Unit Test') {
            steps {
                echo "===== UNIT TEST STAGE ====="
            }
        }
      stage('Integration Test') {
            steps {
                echo "===== INTEGRATION TEST STAGE ====="
            }
        }
    }
    post {
        always {
            echo '==========POST STAGE=========='            
        }
        success {
            echo 'Build and tests completed successfully!'
        }
        failure {
            echo 'Build or tests failed!'
        }
    }
}

/*pipeline {
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
                '''
            }
        }
    }
}
*/
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