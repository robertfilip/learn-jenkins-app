pipeline {
    agent any

    stages {
        stage('Build') {
            agents{
                docker {
                    image 'node:18-alpine'
                    reuseNode true 
                }
            }
            steps {
                sh '''
                ls -a
                node --version
                npm --version
                npm ci
                npm run build
                ls -a

                '''
            }
        }
    }
}
