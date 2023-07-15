pipeline {
    agent any
stages {

           
         stage('Build-Step') {
             when {
               branch 'main'                  
             }
             steps {
                     echo 'Build Step '
             }
         }
     

        stage('Change-Step') {
              steps {
                   echo 'Change Step'
                   snDevOpsChange()
              }
        }

        stage('Post-Change-Step') {
             when {
               branch 'main'                  
             }
             steps {
                     echo 'Post-Change-Step Step '
             }
         }
     
}
   
}
