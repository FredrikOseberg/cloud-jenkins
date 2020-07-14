pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            withAWS(region:"eu-north-1") {
                steps {
                    s3Upload(file:"index.hmtl", bucket:"jenkins-oseb-bucket", path:"/")
                }
            }
        }
    }
}