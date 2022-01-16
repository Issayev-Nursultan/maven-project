pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh 'localMaven clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/*.war'
                }
            }
        }
    }
}
