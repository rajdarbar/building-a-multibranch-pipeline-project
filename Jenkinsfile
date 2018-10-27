pipeline {
    agent any
    parameters {
        booleanParam(defaultValue: true, description: '', name: 'userFlag')
          choice(
        name: 'myParameter',
        choices: "Option1\nOption2",
        description: 'interesting stuff' )
        activeChoiceParam(
            name : 'CHOICE1' ,
            filterable : true,
            choiceType : 'SINGLE_SELECT',
            groovyScript : {
                script('["choice1", "choice2"]')
                fallbackScript('"fallback choice"')
            }
        )
    }
    
    stages {   
        stage('build') {
            
            steps {
                sh 'echo "Hello world!"'
            }
        }
    }
}
