pipeline {
    agent {
        docker {
            image 'postman/newman'  
            args '--entrypoint=""'
        }
    }
    stages {
        stage('Check Newman Version') {
            steps {
                sh 'newman --version'
            }
        }
        stage('Run API Tests') {
            steps {
                // Utilisation du bon nom de fichier pour la collection
                sh 'newman run collections/commentaire.postman_collection.json '
            }
        }
    }
}
