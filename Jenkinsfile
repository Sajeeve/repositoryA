pipeline {
    agent {
       docker {
         image 'maven:3-alpine'
         args '-u root -v /root/.m2:/root/.m2 -v /var/run/docker.sock:/var/run/docker.sock'
       }
    }
    stage('Build Jar'){
        steps {
            sh 'mvn package'
            stash includes: 'target/*.jar', name: 'targetfiles'
        }
    }
    stage('Deploy') {
      steps {
            script{
                sh 'docker build image-name:test'
            }
      }
    }
}