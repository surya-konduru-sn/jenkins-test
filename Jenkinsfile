pipeline {
    agent any
stages {

           
         stage('Build-Step') {
   
       
             steps {
                     echo 'Build Step '
                 snDevOpsArtifact artifactsPayload: '{"artifacts":[{"name": "sa-web.jar", "version": "1.9", "repositoryName": "services-1031"}, {"name": "sa-db.jar", "version": "1.3.2", "repositoryName": "services-1032"}], "branchName": ${env.BRANCH_NAME}}'
                 snDevOpsPackage artifactsPayload: '{"artifacts":[{"name": "sa-web.jar", "version": "1.9", "repositoryName": "services-1031"}, {"name": "sa-db.jar", "version": "1.3.2", "repositoryName": "services-1032"}], "branchName": ${env.BRANCH_NAME}}', name: 'packageName'
     
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
