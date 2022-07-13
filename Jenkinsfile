pipeline {
    agent any
    
    tools {
        maven "maven-3.8.6"
          }
    stages {
           
        stage('Clean and Install') {
            steps {
                 sh 'mvn clean install'
            }
        }
        
         stage('Run') {
            steps {
                dir ("/var/lib/jenkins/workspace/cloned/target"){
               sh 'java -jar demo-0.0.1-SNAPSHOT.jar --server.port=8082'
                }
            }
         }
    }
}
