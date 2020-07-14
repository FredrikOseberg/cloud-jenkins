pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region:"eu-north-1") {
                    s3Upload(file:"index.hmtl", bucket:"jenkins-oseb-bucket", path:"/")
                }
            }
        }
    }
}