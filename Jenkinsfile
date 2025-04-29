pipeline {
    agent {
        label 'AGENT-1'
    }   
    stages {
        stage('Build') {
            steps {
                sh 'echo This is Build'
            }
        }
        stage('Test') {
            steps {
                sh 'echo This is Test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo This is Deploy'
            }
        }
    }

    post {
        always{
            echo "this section runs always"
        }
        success{
            echo "This section run when pipeline is success"
        }
        failure{
            echo "this section runs when pipeline is failure"
        }
    }
}