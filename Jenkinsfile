pipeline {
    stages {
        stage('Clone repository') {
            steps {
                git branch: 'main',
                url: 'https://github.com/PrathamBhatTech/PES1UG20CS305_Jenkins.git'
            }
        }
        stage('Build') {
            steps {
                sh 'make -C main'
            }
        }
        stage('Test') {
            steps {
                sh './hello_exec'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
