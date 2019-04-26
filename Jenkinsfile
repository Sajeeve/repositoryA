node{
    def mvnHome
    stage('getSCM'){
        git 'https://github.com/Sajeeve/repositoryA.git'
        mvnHome = tool 'Maven'
    }
    stage('build'){
       // if(isUnix()){
         //   sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
       // }else{
            echo 'this is build mven artifact'
            bat (/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
       // }
    }
    stage('artifact'){
        archive 'target/*war'
    }
    stage('deploy'){
        echo 'deploy started'
       // bat '''copy C:\\Program Files (x86)\\Jenkins\\workspace\\Pipeline1\\target\\*.jar E:\\'''
        bat ("copy C:\\Program Files (x86)\\Jenkins\\workspace\\Pipeline1\\target\\*.war E:\\")
    }
}