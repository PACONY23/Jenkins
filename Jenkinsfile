
pipeline {
    agent { label 'principal' }
    environment {
        appName = "variable" 
    }
    stages {
        stage("paso 1") {
            steps {
                script {
                    bat "echo hola mundo"
                }
            }
        }
    }
    post {
        always {
            deleteDir()
            bat "echo fase always"
        }
        success {
            bat "echo fase success"
        }
        failure {
            bat "echo fase failure"
        }
    }
}


