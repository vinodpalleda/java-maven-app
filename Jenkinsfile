pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn -B -Dskiptests clean install'
      }
    }
    stage('Test') {
          steps {
            sh 'mvn test'
          }
          post {
            always {
              junit 'target/surefire-reports/*.xml'
            }
          }
          }
          stage('Deliver') {
            steps {
              sh './scripts/deliver.sh'
            }
          }
          }
          }
          
              
              
              
           
          
    
      
                  
