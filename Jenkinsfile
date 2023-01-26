pipeline {
    agent { docker { image 'python:3.8.2' } }
    environment {
        FLASK_APP = 'flaskr'
        FLASK_ENV = 'development'
    }
    stages {
        stage('build') {
            steps {
                withEnv(["HOME=${env.WORKSPACE}"]) {
                    sh 'python --version'
                    sh 'python --version'
                    sh 'export FLASK_APP=flaskr'
                    sh 'export FLASK_ENV=development'
                    sh 'export PATH=$PATH:/home/ubuntu/.jenkins/workspace/app-pipeline_main/.local/bin'
                    sh 'pip install --editable .'
                    sh 'printenv'
                    sh 'nohup python -m flask init-db'
                    sh 'flask run --host=0.0.0.0'
                   
                }

            }
        }
    }
}
