pipeline {
    agent any
    parameters {
        booleanParam(defaultValue: true, description: '', name: 'userFlag')
        activeChoiceParam('choice1') {
                      description('select your choice')
                      choiceType('RADIO')
                      groovyScript {
                          script("return['aaa','bbb']")
                          fallbackScript('return ["error"]')
                      }
                  }
      
    }
    
    stages {   
        stage('build') {
            steps {
                sh 'echo "Hello world!"'
            }
        }
    }
}
