pipeline{
    agent any 
    stages{
        stage('compile stage'){
            steps{
                // withMaven(maven: 'MAVEN_HOME') {
                    bat 'mvn clean compile'
                }
           // }
        }
         stage('testing stage'){
            steps{
               echo 'Testing done'
            }
        }
         stage('deploy stage'){
            steps{
                echo 'Deploy done'
            }
        }
    }
}