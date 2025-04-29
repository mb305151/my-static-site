pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
		git branch: 'main', url: 'https://github.com/mb305151/my-static-site.git'

            }
        }

        stage('Build') {
            steps {
                sh 'echo "No build step needed for static HTML."'
            }
        }

        stage('Deploy') {
            steps {
                // czyści katalog docelowy i kopiuje nowe pliki
                sh '''
                    sudo rm -rf /var/www/html/*
                    sudo cp -r * /var/www/html/
                '''
            }
        }
    }
}
