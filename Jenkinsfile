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
      
     stage ('static parsing') {
       steps {
         bat 'mvn jtest:jtest -Djtest.config="builtin://Critical Rules"'
       }
     }
      
     stage('archive artifacts') {
       steps {
         archiveArtifacts artifacts: 'target/ROOT.war'
            }
        }
   }
 }
