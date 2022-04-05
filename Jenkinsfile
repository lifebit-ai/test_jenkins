pipeline {
    agent { docker { image 'quay.io/lifebitai/cloudos-py:v0.0.7' } }
    stages {
        stage('git') {
            git url:'https://github.com/lifebit-ai/pcgr-nf', branch:'dev-DEL-3310'
        }
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
    }
}
