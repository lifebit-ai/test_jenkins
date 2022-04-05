pipeline {
    agent { docker { image 'quay.io/lifebitai/cloudos-py:v0.0.7' } }
    stages {
        stage('git') {
            steps {
                git url:'https://github.com/lifebit-ai/pcgr-nf', branch:'dev-DEL-3310'
            }
        }
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
        stage('submit') {
            steps {
                sh 'cloudos job run -k Syv8mRIgdNNFJKvAYF1jVTOXnHMQo6mJLTk1yRno --workspace-id 614af4dc31de9201a5c3ce48 --project-name test --workflow-name pcgr-nf --config pcgr-nf/conf/test.config --resumable --spot --wait-completion'
            }
        }
    }
}
