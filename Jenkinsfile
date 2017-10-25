pipeline {
  agent any
  stages {
    stage('p1') {
      parallel {
        stage('s1') {
          steps {
            sh 'sleep 1'
          }
        }
        stage('s2') {
          steps {
            sh 'echo 1'
          }
        }
        stage('s3') {
          steps {
            sh 'echo 2'
          }
        }
        stage('s4') {
          steps {
            sh 'echo 3'
          }
        }
      }
    }
    stage('p2') {
      parallel {
        stage('t1') {
          steps {
            sh 'sleep 2'
          }
        }
        stage('t2') {
          steps {
            sh 'ls /usr/local/src'
          }
        }
      }
    }
    stage('p3') {
      parallel {
        stage('u1') {
          steps {
            sh '/usr/local/php/bin/php -v'
          }
        }
        stage('u2') {
          steps {
            sh 'sleep 1'
          }
        }
      }
    }
    stage('p4') {
      steps {
        sh 'pwd'
      }
    }
    stage('p5') {
      steps {
        sh 'pwd'
      }
    }
  }
  environment {
    env = 'dev'
  }
}