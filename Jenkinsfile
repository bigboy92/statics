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
        stage('Upload to AWS') {
            steps{
                withAWS(region:'us-west-2', credentials:'aws-static') {
                    s3Upload(file:'index.html', bucket:'jenkins-buck')
                    sh 'echo "uploaded files to s3"'
                }
            }
        }
  
    }
}
