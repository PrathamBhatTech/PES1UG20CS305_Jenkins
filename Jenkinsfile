
pipeline
{
    agent any
    stages
    {
        stage('Build')
        {
            steps
            {
                sh 'cd main'
                sh 'make -C main'
                sh '/var/jenkins_home/workspace/PES1UG20CS305_Jenkinsfile/main/hello_exec'
                echo 'Build Stage Successful'
            }
        }
        stage('Test')
        {
            steps
            {   
                sh './a.out'
                echo 'Output from cpp file'
            }
        }
        stage('Deploy')
        {
            steps
            {
                echo 'Deploying...'
            }
        }
    }
}
