pipeline {
    agent { docker { image 'python:3.10.7-alpine' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh 'export FLASK_APP=flaskr'
                sh 'FLASK_ENV=development'
                sh 'mkdir -p src/app'
                sh 'cp -r ./!(src) ./src/app/'
                sh 'cd src/app'
                sh 'pip install --editable .'

            }
        }
    }
}
