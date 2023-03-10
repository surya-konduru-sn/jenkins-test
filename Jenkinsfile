pipeline {
    agent any
stages {

           
         stage('Build-Step') {
   
       
             steps {
                     echo 'Build Step ' 
                 snDevOpsArtifact(artifactsPayload: """{"artifacts":[{"name": "sa-web.jar", "version": "1.9", "repositoryName": "services-1031"}, {"name": "sa-db.jar", "version": "1.3.2", "repositoryName": "services-1032"}], "branchName": "${env.BRANCH_NAME}"}""")
                 snDevOpsPackage (name: "package-${env.BRANCH_NAME}-${env.BUILD_NUMBER}" ,artifactsPayload: """{"artifacts":[{"name": "sa-web.jar", "version": "1.9", "repositoryName": "services-1031"}, {"name": "sa-db.jar", "version": "1.3.2", "repositoryName": "services-1032"}], "branchName": "${env.BRANCH_NAME}"}""")
     
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
