pipeline {
    agent 'any'

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install' 
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true 
            }
        }
    stage('Deploy') {
            steps {
                echo 'Deploying packages' 
            }
        }
    }
}
