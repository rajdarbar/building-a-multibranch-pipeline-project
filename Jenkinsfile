pipeline {
    agent any
    parameters {
        booleanParam(defaultValue: true, description: '', name: 'userFlag')
          choice(
        name: 'myParameter',
        choices: "Option1\nOption2",
        description: 'interesting stuff' )
       
    }
    
    stages {   
        stage('build') {
            
            steps {
                sh 'echo "Hello world!"'
            }
        }
    }
}
