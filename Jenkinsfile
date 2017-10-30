pipeline {
  agent any
  stages {
    stage('build') {
      agent any
      steps {
        build 'release'
      }
    }
    stage('deploy') {
      parallel {
        stage('step1') {
          agent any
          steps {
            sh 'sleep 1'
          }
        }
        stage('step2') {
          agent any
          steps {
            sh 'sleep 3'
          }
        }
        stage('step3') {
          agent any
          steps {
            sh 'sleep 4'
          }
        }
      }
    }
    stage('test') {
      agent any
      steps {
        echo 'done'
      }
    }
    stage('email') {
      agent any
      steps {
        sh 'sleep 1'
      }
    }
  }
}