pipeline {
    agent any
    environment {
        
        name= 'Shivani'
    }
    parameters{
        string(name:'person',defaultValue:'Shivkanya',description:"Who are you?")
        booleanParam(name:'isMale',defaultValue:true ,description:"")
        choice(name: 'City', choices: ['Beed', 'Pune', 'Mumbai'], description: 'Choose a city.')
    }

    stages {
        stage('Run a Command') {
            steps {
              sh '''
              ls
              pwd
              date
              cal 2025
              
              '''
            }
        }
           stage('Environment Variables') {
               environment {
                   username = 'Doiphode Shiv'
               }
            steps {
                sh 'echo "${BUILD_ID}" '
                sh 'echo "${name}" '
                sh 'echo "${username}" '
            }
        }
           stage('Parameter') {
            steps {
                echo 'deploy on test'
                sh 'echo "${name}" '
                sh 'echo "${person}" '
            }
        }
        stage('continue ?') {
            input{
                message "Should we continue?"
                ok "Yes we Should"
            }
            steps {
                echo 'deploy on prod'
            }
        }
        
    }
}
