pipeline {
    agent any
    stages {
        stage ("code clone"){
            steps {
                echo "code clone ho gya"
                git url : "https://github.com/VedTambe/django-notes-app-trainwithshubham.git" , branch:"main"
            }
        }
        stage ("code test") {
            steps {
                echo "code test ho gyaa"
            }
        }
        stage ("code build") {
            steps {
                echo "code build ho gyaa"
                sh "docker build -t noteapp:latest ."
            }
        }
        stage ("project run") {
            steps{
                echo "project deploy ho gyaa"
                sh "docker run -d -p 8000:8000 noteapp:latest"
            }
        }
    }
}
