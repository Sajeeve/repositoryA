pipeline{
    agent any 
    stages{
        stage('compile stage'){
            steps{
                // withMaven(maven: 'MAVEN_HOME') {
                    bat 'mvn clean package'
               // }
            }
        }
         stage('testing stage'){
            steps{
               archiveArtifacts 'target/*.war'
            }
        }
         stage('deploy stage'){
            steps{
                echo 'Deploy done'
            }
        }
    }
}