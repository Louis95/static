pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                sh 'echo "Hello World" '
                sh '''
                    echo "Multitiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}
