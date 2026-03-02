pipeline {
    agent any

    stages {
        stage('Fetch') {
            steps {
                echo 'Fetching from Repo....'
                git 'https://github.com/aanchalg1007/hellojava.git'
            }
        }
        stage('build') {
            steps {
                echo 'building the Program'
                bat 'Javac hello.java'
            }
        }
        stage('Execute') {
            steps {
                echo 'Executing....'
                bat 'java hello'
            }
        }
    }
    post{
        success{
            echo 'Pipeline built successfully'
        }
        failure{
            echo 'Pipeline failed'
        }
    }
}
