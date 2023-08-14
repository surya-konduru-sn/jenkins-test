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
                    snDevOpsChange changeRequestDetails: '{ "autoCloseChange": false, "setCloseCode":true, attributes:{"close_notes":"Testing sample close notes"} }'
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
