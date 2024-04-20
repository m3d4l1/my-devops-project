pipeline {
    agent any

    stages {
        stage('Récupération du code source') {
            steps {
                // Récupération du code depuis Git
                git 'https://url_de_votre_depot_git'
            }
        }
        stage('Affichage de la date système') {
            steps {
                // Affichage de la date système
                script {
                    def date = sh(script: 'date', returnStdout: true).trim()
                    println "La date système est : ${date}"
                }
            }
        }
    }

    post {
        success {
            echo 'Le pipeline a été exécuté avec succès!'
        }
        failure {
            echo 'Le pipeline a échoué.'
        }
    }
}
