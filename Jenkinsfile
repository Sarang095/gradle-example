pipeline {
    agent any

    tools {
        gradle 'GRDL9'
    }

    stages {
        stage('Checkout Code'){
            steps{
            checkout scm
            }
        }
        stage('Build') {
            steps {
                sh 'gradle clean build'
            }
        }

        stage('Archive Artifact') {
            steps {
                archiveArtifacts artifacts: 'build/libs/*.jar'
            }
        }
    }
}
