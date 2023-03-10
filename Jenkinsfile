pipeline {
    agent any
stages {

           
         stage('Build-Step') {
   
       
             steps {
                     echo 'Build Step '
                 snDevOpsArtifact(artifactsPayload: """{"artifacts":[{"name": "sa-web.jar", "version": "${env.BUILD_NUMBER}", "repositoryName": "services-1031"}, {"name": "sa-db.jar", "version": "${env.BUILD_NUMBER}", "repositoryName": "services-1032"}], "branchName": "${env.BRANCH_NAME}"}""")
                 snDevOpsPackage (name: "testing_package-${env.BUILD_NUMBER}" ,artifactsPayload: """{"artifacts":[{"name": "sa-web.jar", "version": "${env.BUILD_NUMBER}", "repositoryName": "services-1031"}, {"name": "sa-db.jar", "version": "${env.BUILD_NUMBER}", "repositoryName": "services-1032"}], "branchName": "${env.BRANCH_NAME}"}""")
     
             }
         }
     

        stage('Change-Step') {
              steps {
                   echo 'Change Step'
                  // snDevOpsChange()
              }
        }
}
   
}
