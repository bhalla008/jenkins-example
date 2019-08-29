pipeline {
  
  agent { label 'linux' }
   
  tools {

     maven 'M3'
      }  
  stages {
         
      stage ('clone the repo') {
           steps {
                  git 'https://github.com/bhalla008/jenkins-example.git'
                }
         }
      stage ('Build') {
           steps {
                  sh 'mvn clean compile'
                }
         }
      stage ('unit test') {
           steps {
                  sh 'mvn test'
                } 
         }
      stage ('package') {
           steps {
                  sh 'mvn package'
                }  
         }

      }
}  
