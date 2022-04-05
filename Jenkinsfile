pipeline {
    agent { docker { image 'quay.io/lifebitai/cloudos-py:v0.0.7' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
    }
}
