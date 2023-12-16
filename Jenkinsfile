pipeline {
    agent {
        node {
            label 'docker-agent-alpine'
            }
      }
    triggers {
        pollSCM 'H* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                cd web
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                cd web
                ls
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}