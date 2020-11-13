pipeline {
    agent any
    environment {
        pourTous="blabla"
    }
    parameters {
        string (name: 'PERSON',defaultValue:'Mr JENKINS', description: 'Who should I say hello to?')
        text (name: 'BIOGRAPHY',defaultValue:'', description: 'Enter some information?')
        booleanParam (name: 'TOGGLE',defaultValue:true, description: 'Toggle this value')
        choice (name: 'CHOICE',choices: ['Afficher', 'Silent'], description: 'pick smthg')
        password (name: 'MDP',defaultValue:'SECRET', description: 'ENTER A PASSWORD')
    }
    stages {
        stage('Build') {
            environment {
                PourCeStage ="blabla"
             }
            steps {
                echo 'Building...' //
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                echo "${PourCeStage}"
             }
        }
        stage('Test') {
            steps {
                echo 'test' //
             }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy' //
             }
        }
        stage('WH') {
            steps {
                echo 'toto' //
            }
        }
        stage('TestParam'){
            when {
                //si choix=one
                expression { params.CHOICE== 'Afficher' }
                    }
            steps {
                    echo "Hello ${params.PERSON}"
                    echo "${params.BIOGRAPHY}"
                    echo "${params.TOGGLE}"
                    echo "MDP ${params.MDP}"
               
                }
            
        }

    }

}
        




