pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "hello world"'
                sh '''echo "Multiline shell steps work too"
                    ls -lah
                '''
            }
        }
    }
}