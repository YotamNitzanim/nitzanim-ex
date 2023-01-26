pipeline {
    agent { docker { image 'python:3.10.7-alpine' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh 'export FLASK_APP=flaskr'
                sh 'export FLASK_ENV=development'
                sh "chmod +x -R ${env.WORKSPACE}"
                sh 'pip3 install --user --editable .'
                sh 'flask init-db'

            }
        }
    }
}
