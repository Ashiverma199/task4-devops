pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/your-username/devops-project.git', branch: 'main'
            }
        }
        stage('Install') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Run') {
            steps {
                sh 'python src/main.py'
            }
        }
        stage('Docker Build') {
            steps {
                sh 'docker build -t devops-project .'
            }
        }
    }
}
