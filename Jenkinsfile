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
                  snDevOpsChange()
              }
        }
}
   
}
                   //snDevOpsChange changeRequestDetails: '{attributes:{"close_notes":"Testing sample close notes"} }'
                   // snDevOpsChange changeRequestDetails: '{ "autoCloseChange": false, attributes:{"close_notes":"Testing sample close notes"} }'
