pipeline {
    agent { docker { image 'python:3.10.7-alpine' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh 'export FLASK_APP=flaskr'
                sh 'export FLASK_ENV=development'
                sh 'python3 -m venv env'
                sh 'source ./env/bin/activate'
                sh 'pip3 install --editable .'
                sh 'flask init-db'

            }
        }
    }
}
