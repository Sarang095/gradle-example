pipeline {
    agent any

    tools {
        gradle 'GRDL9'
    }

    stages {
        stage('Checkout Code'){
            steps{
            git 'https://github.com/andyjduncan/gradle-example.git'
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
