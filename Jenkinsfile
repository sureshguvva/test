properties([pipelineTriggers([githubPush()])])
pipeline {
  agent any
  stages {
    stage('Checkout SCM') {
            steps {
                 sh 'git clone https://github.com/sureshguvva/test.git'
            }
    }
    
    stage('build') {
      steps {
        sh 'mvn -version'
        sh 'mvn clean install'
        }
      stage('docker') {
        sh 'docker pull nginx'
      }
    }
   }
  }
