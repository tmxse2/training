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
   }
 }