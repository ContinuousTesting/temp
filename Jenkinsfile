pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            sh '''pwd
ls
echo %envtest%'''
          }
        }
        stage('parallerbuild') {
          steps {
            sleep 10
          }
        }
      }
    }
    stage('test') {
      steps {
        sh 'echo "in test"'
      }
    }
  }
  environment {
    envtest = 'test123'
  }
}