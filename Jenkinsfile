
pipeline {
    agent any
    stages {
        stage('Lint HTML'){
            tidy -q -e *.html
            
        }
       stage('Build') {
             steps {
                 withAWS(region:'us-east-2',credentials:'aws-static') {
                 sh 'echo "Uploading content with AWS creds"'
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkins-devops-course')
                 }
             }
        }
    }
}
