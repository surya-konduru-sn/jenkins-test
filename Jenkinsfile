pipeline {
    agent any
stages {

           
         stage('Build-Step') {
 
             steps {
                     echo 'Build Step 23 '
             }
         }
     

        stage('Change-Step') {
              steps {
                   echo 'Change Step'
                   snDevOpsChange changeRequestDetails: '{ "autoCloseChange": true }'
                  // snDevOpsChange()
              }
        }
}
   
}
