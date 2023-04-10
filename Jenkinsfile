pipeline {
  agent any
   stages {
     stage('Hello') {
        steps {
          echo "This is the first step in Jenkins pipeline demo to say hello"
        }
      }

     stage('CheckoutGitRepo') {
        steps {
          checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/omnitechSol/java-helloworld.git']])
        }
     }

     stage('install') {
        steps {
          sh 'touch /tmp/jenkinsfile.txt'
        }
     }
   }
}
