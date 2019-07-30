pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multilines shell steps works too"
                    ls -lah
                '''
            }
        }
  
    }
}
