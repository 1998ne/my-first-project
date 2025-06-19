pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git url: 'https://github.com/1998ne/my-first-project.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                echo 'Building project...'
                sh 'ls -la'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying index.html...'
                sh '''
                    sudo cp -r * /var/www/html/
                    sudo systemctl restart apache2
                '''
            }
        }
    }
}
