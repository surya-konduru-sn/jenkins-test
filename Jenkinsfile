pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
            }
            
            post { 
                always { 
        script { 
                 def server = Artifactory.server 'JFROG1'
                 def uploadSpec = """{
                    "files": [{
                       "pattern": "/Volumes/E/WORK/code/app-devops-jenkins/target/app-devops-*.jar",
                       "target": "default-docker-virtual/"
                    }]
                 }"""

              def buildInfo = server.upload(uploadSpec) 
              server.publishBuildInfo buildInfo   
        }}
       }
            
        }
        
        stage('Stage2') {
            steps {
                script { 
                 def server2 = Artifactory.server 'JFROG1'
                 def uploadSpec = """{
                    "files": [{
                       "pattern": "/Volumes/E/WORK/code/tmp/*.js",
                       "target": "default-docker-virtual/"
                    }]
                 }"""

              def buildInfo2 = server2.upload(uploadSpec) 
              server2.publishBuildInfo buildInfo2   
        }
            }
        }
    }
    
}
