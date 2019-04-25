pipeline{
    agent any 
    stages{
        stage('compile stage'){
            steps{
                // withMaven(maven: 'MAVEN_HOME') {
                    bat 'mvn clean install'
               // }
            }
        }
         stage('testing stage'){
            steps{
                bat 'cd target'
               bat 'java -jar <project jar file name>.jar'
            }
        }
         stage('deploy stage'){
            steps{
                echo 'Deploy done'
            }
        }
    }
}