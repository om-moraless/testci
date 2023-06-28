pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                  zip zipFile: 'sample_app.zip',
                  archive: false,
                  dir: '',
                  exclude: 'build/'
                  archiveArtifacts 'sample_app.zip'
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
