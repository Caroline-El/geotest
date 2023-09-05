pipeline{
    agent any
    stages{
        Stage('first stage'){
            steps{
                sh 'echo hello'
            }
        }
        stage('clean artifact'){
            steps{
                sh 'echo hi'
            }
        }
    }
}