pipeline {
    agent any
    stages {
        stage('Lint') {
            tidy -q -e *.html
        }
        stage('Upload to AWS') {
            steps {
                withAWS(region:"eu-north-1", credentials:"aws-static") {
                    s3Upload(file:"index.html", bucket:"jenkins-oseb-bucket")
                }
            }
        }
    }
}