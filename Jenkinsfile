pipeline {
   agent any
   tools {
     maven "Maven1"
   }
   stages {
     stage ('build') {
       steps {
         bat 'mvn clean package'
       }
     }
      
     stage('archive artifacts') {
            steps {
                archiveArtifacts artifacts: 'target/ROOT.war'
            }
        }
   }
 }
