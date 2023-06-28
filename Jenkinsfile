pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
              echo 'Build..'
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
                 script {
                  zip zipFile: 'testci_app.zip',
                  archive: false,
                  dir: 'app',
                  exclude: '**/build/*'
                  archiveArtifacts 'testci_app.zip'
                }
            }
        }
    }
}
