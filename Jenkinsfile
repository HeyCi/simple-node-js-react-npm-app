pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
    environment { 
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo "npm install qui marche pas"'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "test qui marche pas non plus"'
            }
        }
        stage('Deliver') { 
            steps {
                sh 'echo "delivery idem"'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh './jenkins/scripts/kill.sh'
            }
        }
    }
}
