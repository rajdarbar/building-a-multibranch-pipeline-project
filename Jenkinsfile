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
                  activeChoiceReactiveParam('choice2') {
                      description('select your choice')
                      choiceType('RADIO')
                      groovyScript {
                          script("if(choice1.equals('aaa')){return ['a', 'b']} else {return ['aaaaaa','fffffff']}")
                          fallbackScript('return ["error"]')
                      }
                      referencedParameter('choice1')
                  }
    }
    
    stages {
        
        stage('Build') {
            steps {
                sh 'echo "Hello world!"'
            }
        }
    }
}
