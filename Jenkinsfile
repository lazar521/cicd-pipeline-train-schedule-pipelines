pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Execute the Gradle build
                    sh './gradlew build --no-daemon'
                }
            }
        }
        stage('Archive Artifacts') {
            steps {
                script {
                    // Archive the trainSchedule.zip artifact
                    archiveArtifacts artifacts: 'dist/trainSchedule.zip', allowEmptyArchive: true
                }
            }
        }
    }
}
