pipeline {
    agent any
    parameters {
        booleanParam(defaultValue: true, description: '', name: 'userFlag')
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello world!"'
            }
        }
    }
}
