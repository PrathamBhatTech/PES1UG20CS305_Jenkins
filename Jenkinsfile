pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o ${env.BUILD_ID} hello.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './${env.BUILD_ID}'
            }
        }
    }
    post {
        always {
            echo "Pipeline complete"
        }
        failure {
            echo "Pipeline failed"
        }
    }
}
