node{
    def mvnHome
    stage('getSCM'){
        git 'https://github.com/Sajeeve/repositoryA.git'
        mvnHome = tool 'Maven'
    }
    stage('build'){
            echo 'this is build mven artifact'
            bat (/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
    }
    stage('artifact'){
        archive 'target/*.jar'
    }
  
    stage('deploy'){
        //hardcoded the jar files name target/*.jar doesn't work
        bat ('java -jar target/demo-0.0.1-SNAPSHOT.jar')
    }
}