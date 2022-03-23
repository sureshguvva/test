properties([pipelineTriggers([githubPush()])])
pipeline {
  agent any
  stages {
    stage('Checkout SCM') {
            steps {
                sh 'rm -rf test'
                 sh 'git clone https://github.com/sureshguvva/sample-java-programs.git'
            }
    }
    
    stage('build') {
      steps {
        sh 'mvn -version'
        sh 'mvn clean install'
        }
    }
      stage('docker') {
        steps { 
        sh 'docker pull nginx'
        }
      }
    }
   }
  
