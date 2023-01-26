pipeline {
    agent { docker { image 'python:3.10.7-alpine' } }
    stages {
        stage('build') {
            steps {
                bash 'python --version'
                sh 'python --version'
                sh 'export FLASK_APP=flaskr'
                sh 'export FLASK_ENV=development'
                sh 'mkdir -p src/app'
                bash 'shopt -s extglob'
                sh 'pwd'
                sh 'cp !(src) src/app'
                sh 'cd src/app'
                sh 'pwd'
                sh 'ls'
//                 sh 'cp ../..'
//                 sh "chmod +x -R ${env.WORKSPACE}"
//                 sh 'pip3 install --user --editable .'
//                 sh 'flask init-db'

            }
        }
    }
}
