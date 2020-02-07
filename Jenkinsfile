
pipeline {
    agent any
    stages {
       stage('Build') {
             steps {
                 withAWS(region:'US EAST(Ohio)',credentials:'aws-static') {
                 sh 'echo "Uploading content with AWS creds"'
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkins-devops-course')
                 }
             }
        }
    }
}
