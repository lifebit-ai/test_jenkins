pipeline {
    agent { docker { image 'quay.io/lifebitai/cloudos-py:v0.0.7' } }
    stages {
        stage('git') {
            steps {
                git url:'https://github.com/lifebit-ai/bi-metagwas-nf', branch:'dev'
            }
        }
        stage('build') {
            steps {
                sh 'pwd'
                sh 'ls -lah'
                sh 'python --version'
            }
        }
        stage('submit') {
            steps {
                sh 'cloudos job run -k GXfwBP2eujWJlGUzibgbQh1hSVBelNh1WJzHII80 --workspace-id 614af4dc31de9201a5c3ce48 --project-name test --workflow-name bi-metagwas-nf --job-config conf/basic_test.config --resumable --spot --wait-completion'
            }
        }
    }
}
