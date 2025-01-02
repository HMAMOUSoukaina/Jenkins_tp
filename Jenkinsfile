pipeline {
    agent any // Exécute sur n'importe quel agent Jenkins disponible
    stages {
        stage('Build') { // Étape de compilation
            steps {
                echo 'Building the application...' // Affiche un message
                sh 'javac HelloWorld.java' // Compile le fichier Java
            }
        }
        stage('Test') { // Étape de test
            steps {
                echo 'Running tests...'
                sh 'java HelloWorld' // Exécute le fichier compilé
            }
        }
        stage('Deploy') { // Étape de déploiement
            steps {
                echo 'Deploying the application...'
            }
        }
    }
    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline execution failed.'
        }
    }
}
