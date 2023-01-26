pipeline {
    agent { docker { image 'python:3.10.7-alpine' } }
    stages {
        stage('build') {
            steps {
                withEnv(["HOME=${env.WORKSPACE}"]) {
                    sh 'python --version'
                    sh 'python --version'
                    sh 'export FLASK_APP=flaskr'
                    sh 'export FLASK_ENV=development'
                    sh 'export FILES=$(ls)'
                    sh 'mkdir test'
                    sh 'cd test && pwd && pip3 install virtualenv' 
                    sh 'virtualenv venv && . venv/bin/activate && pip install --editable . && flask init-db'
                    sh 'mkdir -p src/app' 
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
