pipeline{
    agent any
    tools{
        maven 'M2_HOME'
    }
    stages{
        stage('maven clean'){
            steps{
                sh 'mvn clean'
            }
        }
        
        stage('maven install'){
            steps{
                sh 'mvn install'
            }

        }
         stage('maven package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('upload.artifact'){
            steps{
                sh 'nexusArtifactUploader artifacts: [[artifactId: 'bioMedical', classifier: '', file: 'target/bioMedical-0.0.2-SNAPSHOT.jar', type: 'jar']], credentialsId: '17414518-9fa4-4434-bd03-50c5c5d10503', groupId: 'qa', nexusUrl: '198.58.119.40:8081/repository/', nexusVersion: 'nexus3', protocol: 'http', repository: 'Carol-repo', version: '0.0.2'
            }
        }
        }
    }
