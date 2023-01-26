pipeline {
    agent { docker { image 'python:3.10.7-alpine' } }
    environment {
        FLASK_APP = 'flaskr'
        FLASK_APP    = 'development'
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
                    sh 'pip install flask' 
                    sh 'flask init-db'
                    sh 'pwd'
                    sh 'cp -r ./{LICENSE,MANIFEST.in,README.MD,README.md,README.rst,codefresh.yml,docker-flask-codefresh.jpg,flaskr,flaskr.egg-info,instance,requirements.txt,setup.cfg,setup.py,tests} ./src/app'
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
}
