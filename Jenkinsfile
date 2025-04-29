pipeline {
    agent {
        label 'AGENT-1'
    }
    options{
        timeout(time: 10, unit: 'MINUTES')
    }   
    stages {
        stage('Build') {
            steps {
                sh 'echo This is Build'
                //sh 'sleep 10'
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
            deleteDir()
        }
        success{
            echo "This section run when pipeline is success"
        }
        failure{
            echo "this section runs when pipeline is failure"
        }
    }
}