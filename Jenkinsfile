pipeline {
    agent any

    stages {
        stage("cloning") {
            steps {
                git url: 'https://github.com/gowtham123K/eleven.git', branch: 'main'
            }
        }

        stage("dependency") {
            steps {
                bat '''
                    C:\\Users\\gowth\\AppData\\Local\\Programs\\Python\\Python313\\python.exe -m venv venv
                    call venv\\Scripts\\activate
                    python -m pip install --upgrade pip
                    pip install pytest
                '''
            }
        }

        stage("testing") {
            steps {
                bat '''
                    call venv\\Scripts\\activate
                    pytest Test_add.py
                '''
            }
        }

        stage("deploy") {
            steps {
                bat '''
                    call venv\\Scripts\\activate
                     C:\\Users\\gowth\\AppData\\Local\\Programs\\Python\\Python313\\python.exe hi.py
                '''
            }
        }
    }
}
