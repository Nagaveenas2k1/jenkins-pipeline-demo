pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/Nagaveenas2k1/jenkins-pipeline-demo.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    dockerImage = docker.build("jenkins-pipeline-demo:latest")
                }
            }
        }
        stage('Test App') {
            steps {
                sh 'docker run --rm -d -p 5000:5000 --name test-app jenkins-pipeline-demo:latest'
                // Optionally add HTTP test here; for a real project, add integration tests.
                sh 'sleep 5'
                sh 'curl --fail http://localhost:5000'
                sh 'docker stop test-app'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment would take place here (push image to a registry or deploy to server)'
            }
        }
    }
}

