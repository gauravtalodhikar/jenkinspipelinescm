pipeline {
    agent any

    stages {
        stage('stage-1') {
            steps {
                sh "sudo yum install httpd -y"
            }
        }
        stage('stage-2') {
            steps {
                sh "sudo systemctl start httpd"
            }
        }
        stage('stage-3') {
            steps {
                sh "sudo echo 'Hey Httpd' > /var/www/html/index.html"
            }
        }
        stage('stage-4') {
            steps {
                sh "sudo systemctl restart httpd"
        }
        }
        stage('stage-5') {
            steps {
                sh "sudo systemctl status httpd"
            }
        }
    }
}
