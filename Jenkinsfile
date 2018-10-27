pipeline {
    agent any
    parameters {
        booleanParam(defaultValue: true, description: '', name: 'userFlag')
       
    }
    
    stages {   
        stage('build') {
            script {
                 activeChoiceParam('CHOICE-1') {
            description('Allows user choose from multiple choices')
            filterable()
            choiceType('SINGLE_SELECT')
            groovyScript {
                script('["choice1", "choice2"]')
                fallbackScript('"fallback choice"')
            }
            defaultValue: need_debug_build(currentBuild)
        }
            }
            steps {
                sh 'echo "Hello world!"'
            }
        }
    }
}
