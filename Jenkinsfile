pipeline {
    agent { docker { image 'python:3.10.7-alpine' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh 'export FLASK_APP=flaskr'
                sh 'export FLASK_ENV=development'
                sh 'chmod -R 777 ./local'
                sh 'chmod -R 777 /var/lib/jenkins/workspace'
                sh 'pip3 install --editable .'
                sh 'flask init-db'

            }
        }
    }
}
